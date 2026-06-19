# Concise reviews with an evaluator-selected common structure

## Context

The peer-reviewer skill's only length guidance was "length scales with the paper," and
each persona's output structure came from an 8–11 section discipline rubric template.
On a ~30-page paper this produced ~2500 words per reviewer — review-article length,
well beyond a real referee report — with the same concern restated across the Weaknesses,
Empirical evaluation, Questions, and Comments sections.

## Decision

Reviews are concise by default and share one structure per session:

- **Anchored length with a hard cap.** ~300-word floor, ~500-word target for a typical
  paper, ~800-word hard cap for long archival submissions. Uniform across all personas.
  A **verbosity override** (user-requested, or persona-self-governed only when omitting a
  load-bearing concern would mislead) raises the cap to ~1500 words — *length only*, never
  re-expanding structure. The meta-review gets its own ~500-word cap and scales conservatively.
- **Rubrics become content guides, not output templates.** A rubric describes what a
  reviewer in that field evaluates and names that domain's concise default structure; it no
  longer dictates the headed sections of the output.
- **The evaluator (pre-evaluation) selects one common structure** from the matching rubric
  (blending the two closest for cross-disciplinary work) and all reviewers in the session
  adopt it. Shape is common within a session; content is domain-specific across sessions;
  voice varies by persona.

## Considered options

- *Word budget alone, keep all rubric sections* — rejected: 9 headed sections can't compress
  below ~500 words, so structure beats the budget (the original failure mode).
- *Each persona owns its own structure* — rejected: the user wants every reviewer in one
  panel to share a shape; per-persona structure breaks that and is harder to synthesize.
- *Evaluator derives structure freely each run* — rejected: nondeterministic across reruns,
  harder to test against fixture papers. Selecting from the rubric keeps same-paper-same-shape.

## Consequences

- A hard cap binds the model far better than a soft "aim for ~500"; the ~500 target keeps
  reviews from defaulting to the ceiling.
- Console shows the meta-review verbatim plus a one-line verdict per reviewer; full reviews
  are written to files. The meta-review is always authored by the orchestrating agent, which
  already holds the pre-evaluation, paper, and collected reviews (no extra agent in parallel mode).
