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

Cross-disciplinary work blends the two closest rubrics.

## Output

Reviews are written to `/mnt/user-data/outputs/` as Markdown files:

- Single reviewer: `review-{persona}-{paper-shortname}.md`
- Panel: `review-one-{shortname}.md`, `review-two-{shortname}.md`, `review-three-{shortname}.md`, `meta-review-{shortname}.md`

## Hard limits (all personas)

- No fabricated citations, datasets, or prior results
- No personal attacks on authors — the work is critiqued, not the person
- No breaking character mid-review
- No refusals based on topic or discipline

## Reference files

The `references/` directory contains the full persona specs and rubrics:

- `reviewer-one.md` — Reviewer One persona
- `reviewer-two.md` — Reviewer Two persona
- `reviewer-three.md` — Reviewer Three persona
- `panel.md` — Panel orchestration and meta-review spec
- `discipline-rubrics.md` — Full rubric templates for all four discipline families
