# Pre-evaluation

Runs before any reviewer. Reads the paper once and produces shared context so all reviewers work from the same discipline determination — without it, parallel agents may independently select different rubrics. In sequential execution it prevents redundant re-reading; in parallel execution it's required upfront.

## Output

Produce the following, then pass it as starting context to each reviewer:

- **Discipline**: which rubric family applies (from the table below); if cross-disciplinary, name the two closest and describe the blend
- **Shortname**: 2–3 word identifier used in output filenames
- **Venue**: stated or inferred journal, conference, or track
- **Summary**: 2–4 sentences — what the paper does, what it claims, and what kind of contribution it makes
- **Key claims**: 3–5 bulleted claims the reviewers should evaluate
- **Common structure**: the ordered section list every reviewer in this session will use. Take it from the matching row below (blend the two closest for cross-disciplinary work). This is selection, not invention — lightly tailor only if the paper plainly warrants it. Every reviewer adopts this same structure; only voice and emphasis vary.

## Rubric selection table

Pick the row whose methodology best matches the paper; default to **Empirical sciences** when unsure. Each reviewer then reads only the matching content guide in `rubrics/{file}.md` for *what* to evaluate.

| Discipline (`rubrics/{file}.md`) | When it applies | Common structure (before shared tail) |
|---|---|---|
| **Empirical sciences** (`empirical-sciences`) | experiments, measurements, data analysis: ML, systems, physics, bio, neuro, quant social science, epidemiology | Summary · Strengths · Weaknesses |
| **Theory / math** (`theory-math`) | proofs, formal methods, foundational ML theory | Summary · Significance · Correctness |
| **Humanities** (`humanities`) | argument, interpretation, sources: history, literary studies, philosophy, theology, art history | Summary · Argument · Evidence & engagement |
| **Design / qualitative HCI** (`design-qualitative-hci`) | HCI, design research, qualitative/mixed-methods user studies, ethnography | Summary · Framing & methods · Findings & implications |
| **Clinical / health sciences** (`clinical-health-sciences`) | human-subjects data, RCTs, systematic reviews, epidemiology, public health | Summary · Design & population · Outcomes & analysis · Reporting & ethics |
| **Economics / econometrics** (`economics-econometrics`) | causal identification: applied micro/macro, labor, development, public economics | Summary · Identification · Data & robustness |
| **Legal scholarship** (`legal-scholarship`) | legal argument, doctrinal analysis, statutory/constitutional interpretation | Summary · Doctrinal accuracy · Argument |
| **Arts / practice-based** (`arts-practice-based`) | artifact or practice as contribution: creative writing, studio art, composition, performance, film, architecture | Summary · The work · Research framing & contextualization |

## Shared tail

Every common structure ends with the same two sections — never re-spell this elsewhere, just reference it:

- **Recommendation**: one of {Accept | Minor revision | Major revision | Reject}, with a one-sentence justification.
- **Confidence**: one of {Low | Medium | High}, with one sentence on why.

The common structure fixes the *shape* of the session's reviews. Length lives in `SKILL.md`; the reviewers' per-persona voice rules live in the persona files.
