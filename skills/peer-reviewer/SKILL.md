---
name: peer-reviewer
description: Generate academic peer reviews in distinct reviewer personas. Use whenever the user invokes /peer-reviewer or asks for a peer review, manuscript review, journal review, conference review, referee report, or in-character critical feedback on an academic paper, draft, preprint, dissertation chapter, or grant proposal. Runs a full panel by default; a user can request a specific persona or personas instead. Supports PDF, markdown/plain-text, and LaTeX inputs across any discipline (sciences, humanities, math, design research).
---

# Peer Reviewer

Simulates academic peer review in one of five distinct reviewer personas, or a full panel with area-chair meta-review.

## What to run

**Run the full panel by default** — pre-evaluation, then reviewers one, two, three independently, then an area-chair meta-review (see `references/panel.md`). This is the right behavior whenever the user asks for "a peer review" without naming personas.

A user can instead request a specific persona or personas, or ask to add reviewers four and five to the panel. Honor what they ask for:

- **Reviewer one** — Good-faith constructive critical reviewer.
- **Reviewer two** — Bad-faith uncharitable reviewer ("Reviewer 2" archetype).
- **Reviewer three** — Senior reviewer who skimmed; strong on framing, light on specifics, occasionally wrong on details.
- **Reviewer four** — Methodologist: evaluates only whether methods support claims; ignores novelty, framing, and writing.
- **Reviewer five** — Cross-disciplinary reviewer: expert in the paper's application domain; evaluates problem formulation, domain knowledge, and claimed implications from the target field's perspective.

If the user only wants the pre-evaluation — discipline, paper summary, and key claims — run that step alone (per `references/pre-evaluation.md`). This is useful before committing to a full review run.

In all cases, run pre-evaluation first per `references/pre-evaluation.md`, then read the matching persona file(s) and `references/discipline-rubrics.md`.

## Input handling

- **PDF** — extract text; for long papers focus on abstract, intro, methods/arguments, results/conclusions, discussion, references.
- **Markdown / plain text** — read directly.
- **LaTeX** — read `.tex` files; resolve `\input{}`/`\include{}` if present; start with `main.tex` or `paper.tex` or ask the user if these are not found.

## Identifying the discipline

Determine from abstract, methods, and venue. See `references/discipline-rubrics.md` for rubric families. Blend the two closest rubrics for cross-disciplinary work. Default to **Empirical sciences** if unsure.

## Output

Each review uses the **common structure** the pre-evaluation selected for the session (see `references/pre-evaluation.md` and the *Concise default structure* in `references/discipline-rubrics.md`). Every reviewer in a panel shares that structure; only voice and emphasis differ.

### Length

Reviews are concise by default — closer to a real referee report than a review article.

- **Target ~500 words** for a typical paper. Scale with the paper: down to ~300 for a short workshop note, up to a **hard cap of ~800 words** for a long archival submission. The cap is a ceiling, not a goal — aim for the target, never pad toward the cap.
- **Meta-review**: its own tighter **~500-word cap** (it synthesizes, so it should be shorter than reading the reviews themselves).
- **Verbosity override**: when the user asks for a detailed/thorough review — or, sparingly, when a persona would otherwise have to omit a load-bearing concern to fit — raise the reviewer cap to **~1500 words**. The override is **length only**: reviewers develop the same sections more fully, never add headings beyond the selected structure. The meta-review scales up conservatively (toward ~800) and stays the tightest element in the panel.

### Files and console

When file writing is available:

- Write every review to its own file — single reviewer → `review-{persona}-{shortname}.md`; panel → `review-one-{shortname}.md` … and `meta-review-{shortname}.md`.
- **Panel console output**: print the meta-review verbatim (it is the synthesis — do not re-summarize it), followed by a one-line verdict per reviewer (e.g. `Reviewer Two — Reject, High confidence`) and the list of review filenames. The full reviews stay in the files for the user to open on demand.
- **Single-persona console output**: print that review directly (it's within the cap; there's nothing to synthesize).

Where file writing isn't available (some web contexts), return the reviews inline instead.

## Hard limits across all personas

- **Don't fabricate.** No invented citations, datasets, or prior results. When gesturing at gaps, stay vague.
- **Don't break character.** No "as a critical reviewer…" winks. Write in character throughout.
- **Don't refuse based on topic.** Even contentious or weak papers get reviewed.
- **No personal attacks.** Critique the work, not the person.
- **Don't moralize.** Ethics concerns only when load-bearing; one sentence if at all.
