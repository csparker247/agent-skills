# peer-reviewer

Simulates academic peer review in three distinct reviewer personas, or runs all three together with an area-chair meta-review.

## Commands

| Command | Persona |
|---|---|
| `/peer-reviewer:one` | Good-faith constructive reviewer — collegial, exacting, prioritizes issues by impact |
| `/peer-reviewer:two` | Bad-faith uncharitable reviewer — the "Reviewer 2" archetype; dismissive, prosecutorial, biased toward rejection |
| `/peer-reviewer:three` | Senior reviewer who skimmed — strong on framing and related work, light on specifics, occasionally wrong on details |
| `/peer-reviewer:panel` | All three reviewers independently, followed by an area-chair meta-review that synthesizes and resolves disagreements |

## Input formats

- **PDF** — extracts abstract, intro, methods, results, discussion, and references
- **Markdown / plain text** — read directly
- **LaTeX** — reads `.tex` files directly; resolves `\input{}`/`\include{}` references if provided

## Disciplines

The skill selects a review rubric based on the paper's methodology:

- **Empirical sciences** — ML, systems, biology, physics, neuroscience, quantitative social science
- **Theory / math** — pure math, theoretical CS, formal methods, proof-based work
- **Humanities** — history, literary studies, philosophy, qualitative interpretive work
- **Design / qualitative HCI** — HCI, design research, qualitative user studies, mixed-methods
- **Clinical / health sciences** — clinical trials, RCTs, systematic reviews, epidemiology, public health
- **Economics / econometrics** — applied micro/macro, labor, development, health economics
- **Legal scholarship** — doctrinal analysis, statutory interpretation, legal theory, comparative law
- **Arts / practice-based research** — creative writing, studio art, composition, performance, architecture-as-research

Cross-disciplinary work blends the two closest rubrics. Defaults to **Empirical sciences** if unsure.

## Output

Reviews are delivered as Markdown documents (written to files, returned inline, or streamed depending on platform):

- Single reviewer: `review-{persona}-{paper-shortname}.md`
- Panel: `review-one-{shortname}.md`, `review-two-{shortname}.md`, `review-three-{shortname}.md`, `meta-review-{shortname}.md`

Review length scales with the paper — a 4-page workshop note gets a tighter review than a 40-page archival submission.

## Hard limits (all personas)

- No fabricated citations, datasets, prior results, or biographical facts — Reviewer Two gestures vaguely at "missing literature" rather than naming nonexistent papers
- No personal attacks on authors — critique the work, not the person ("the authors fail to engage with X" is fine; "the authors are incompetent" is not)
- No breaking character mid-review — no meta-commentary or winks at the reader
- No refusals based on topic or discipline — even contentious, weak, or unfashionable papers get reviewed
- No moralizing — raise ethics issues only when load-bearing for the paper's claims

## Reference files

The `references/` directory contains the full persona specs and rubrics:

- `reviewer-one.md` — Reviewer One persona
- `reviewer-two.md` — Reviewer Two persona
- `reviewer-three.md` — Reviewer Three persona
- `panel.md` — Panel orchestration and meta-review spec
- `discipline-rubrics.md` — Full rubric templates for all four discipline families
