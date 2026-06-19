# Pre-evaluation

Runs before any reviewer. Reads the paper once and produces shared context so all reviewers work from the same discipline determination — without it, parallel agents may independently select different rubrics. In sequential execution it prevents redundant re-reading; in parallel execution it's required upfront.

## Output

Produce the following, then pass it as starting context to each reviewer:

- **Discipline**: which rubric family from `discipline-rubrics.md` applies; if cross-disciplinary, name both rubrics and describe the blend
- **Shortname**: 2–3 word identifier used in output filenames
- **Venue**: stated or inferred journal, conference, or track
- **Summary**: 2–4 sentences — what the paper does, what it claims, and what kind of contribution it makes
- **Key claims**: 3–5 bulleted claims the reviewers should evaluate

