# Discipline-specific review rubrics

Pick the rubric whose methodology best matches the paper. When unsure, default to **Empirical sciences**. When the paper crosses fields (digital humanities, computational social science, applied ML in a specific scientific domain), blend the two closest rubrics — don't force a bad fit.

Every rubric ends with:

- **Comments to authors** — freeform prose (1–4 paragraphs, depending on persona and paper length). This is where the persona's voice is most visible.
- **Recommendation**: one of {Accept, Minor revision, Major revision, Reject}
- **Confidence**: {Low, Medium, High}

The structured sections above are written in the persona's voice but stay concrete and professional. Voice asymmetries (e.g., Reviewer Two's terseness, Reviewer Three's gestural vagueness on technical sections) are described in each persona file — apply them here.

---

## Empirical sciences

For ML, systems, empirical CS, physics, biology, neuroscience, quantitative social science, epidemiology, and similar fields where claims rest on experiments, measurements, or data analysis.

```markdown
# Review: {paper title}

## Summary
2–4 sentences in the reviewer's own words: what the paper does and what it claims.

## Strengths
Bulleted, each 1–3 sentences. Prioritized — most important first.

## Weaknesses
Bulleted, prioritized by impact (unsupported claims > methodological gaps > missing baselines/controls > clarity).

## Technical soundness
Are the methods appropriate to the questions? Are statistics correct? Are baselines and controls adequate? Are confounds addressed?

## Empirical evaluation
Are the experiments sufficient to support the claims made? Are ablations present where the contribution warrants them? Is the evaluation set appropriate? Are results reported with adequate detail (variance, multiple seeds, error bars)?

## Clarity and presentation
Writing, figures, notation, structure. Brief unless there are real issues.

## Reproducibility
Is there enough information (code, data, hyperparameters, environment) for an informed reader to reproduce the work? Where information is missing, is it because of legitimate constraints (proprietary data) or oversight?

## Questions for the authors
Numbered, focused. The kind of questions whose answers would change your assessment.

## Comments to authors
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```

---

## Theory / math

For pure math, theoretical CS, formal methods, proof-based work, foundational ML theory.

```markdown
# Review: {paper title}

## Summary
Statement of the main results in the reviewer's own words. Be precise — readers of theory reviews care about the exact statements.

## Significance
Do these results matter? To whom? Do they open new directions, close standing open problems, or extend known results? Be specific about what the result enables.

## Originality
Genuinely new ideas, or technical extension of prior work? Both can be valid — be explicit which.

## Correctness
Have you spot-checked the key lemmas? Are the proofs complete and rigorous? Are there places where the proof is unclear, hand-wavy, or appears to gap?

## Exposition
Are definitions clean? Are examples illuminating? Are proofs readable? Is the paper structured to help a reader work through the argument?

## Relationship to prior work
Does the paper engage with the right literature? Are key precedents cited? Are the differences from prior work clearly articulated?

## Questions for the authors
Numbered, focused on technical content.

## Comments to authors
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why, including whether you verified the proofs]
```

---

## Humanities

For history, literary studies, philosophy, theology, art history, qualitative interpretive work, and other fields where contribution is made through argument, interpretation, and engagement with primary or secondary sources.

```markdown
# Review: {paper title}

## Summary
The paper's thesis and central argument, in the reviewer's own words.

## Argument
Is the central argument clear, well-structured, and defended? Are the moves in the argument valid and well-supported? Where is the argument strongest, and where does it depend on assumptions the reader is asked to grant?

## Evidence and sources
Are primary and secondary sources used appropriately and accurately? Are there obvious gaps in source coverage? Is the use of sources fair to their context, or selective in ways that distort?

## Engagement with scholarship
Does the paper situate itself in the field's ongoing conversations? Are key interlocutors engaged, or only nominally cited? Are there scholarly debates the paper enters that it should acknowledge more directly?

## Methodology
Where relevant — archival, hermeneutic, comparative, philological, theoretical. Is the methodological approach appropriate to the questions? Are its limits acknowledged?

## Style and presentation
Prose quality, organization, citation practices, accessibility to the intended readership.

## Questions for the author
Numbered. The kinds of questions a thoughtful reader would press the author on.

## Comments to author
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```

---

## Design / qualitative HCI

For HCI, design research, qualitative user studies, mixed-methods empirical work, ethnography, applied research where the contribution is in articulating a problem, designing an artifact or intervention, or surfacing findings from participants.

```markdown
# Review: {paper title}

## Summary
The research questions and what the paper found / built / argued.

## Motivation and framing
Is the problem well-motivated? Is the scope clear? Does the paper articulate why this work matters and to whom?

## Methodology
Is the method appropriate for the research questions? Participants (recruitment, sample, fit to question)? Procedures (data collection, instrument design)? Analysis (coding process, theme generation, validity practices)?

## Findings
Are findings clearly presented and grounded in the data? Where claims go beyond the data, is that signaled? Are quotes and examples illustrative rather than load-bearing in places they shouldn't be?

## Discussion and implications
Does the paper convincingly draw implications for design, theory, or practice? Are the implications proportionate to the evidence?

## Reflexivity and limitations
Does the paper acknowledge its own limits — sample, setting, researcher positionality where relevant?

## Questions for the authors
Numbered, focused.

## Comments to authors
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```

---

## Clinical / health sciences

For clinical trials, RCTs, systematic reviews, meta-analyses, epidemiology, public health, health services research, and medical education — fields where claims rest on human subjects data and reporting standards are codified.

```markdown
# Review: {paper title}

## Summary
Study design, population, intervention or exposure, primary outcome, and main finding in 2–4 sentences.

## Research question and framing
Is the question clearly stated and clinically or scientifically meaningful? Is the study design appropriate to the question?

## Study design
Appropriateness of design to question. Trial registration where applicable. Adequacy of blinding, randomization, and allocation concealment.

## Population and sampling
Eligibility criteria, recruitment, sample size justification, and representativeness. Does the population support the claimed generalizability?

## Intervention or exposure
Fidelity, adequacy of comparator, dose/duration where relevant.

## Outcomes
Are primary and secondary outcomes pre-specified and clinically meaningful? Is measurement valid? Are patient-centered outcomes included where relevant?

## Statistical analysis
Appropriateness of methods, handling of missing data, multiplicity, and effect sizes with confidence intervals (not p-values alone).

## Reporting standards
Does the paper follow applicable guidelines (CONSORT, PRISMA, STROBE, etc.)? Are deviations justified?

## Ethics and safety
IRB approval, informed consent, adverse event reporting, data safety monitoring where applicable.

## Questions for the authors
Numbered, focused.

## Comments to authors
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```

---

## Economics / econometrics

For applied microeconomics, macroeconomics, labor, development, health, and public economics — fields where the central contribution often turns on the credibility of a causal identification strategy.

```markdown
# Review: {paper title}

## Summary
Research question, identification strategy, data source, and main result in 2–4 sentences.

## Contribution
New identification strategy, new data, new context, or new theory? Is the contribution clearly articulated relative to the literature?

## Identification strategy
What is the causal claim, and how is it identified? Are identifying assumptions credible and tested? Key design-specific checks: IV (strong first stage, defensible exclusion restriction); RDD (no manipulation at threshold); DiD (parallel trends plausible and tested); structural (assumptions transparent, model well-motivated).

## Data
Sources, sample construction, variable definitions, measurement error, and appropriateness to the research question.

## Robustness
Stability across specifications, bandwidth choices, or sample restrictions. Placebo and falsification tests. Standard errors appropriate for the data structure (clustering, heteroskedasticity).

## Economic magnitude
Are effect sizes economically meaningful? Are welfare or distributional implications discussed?

## Relationship to prior literature
How do estimates compare to existing work? Are discrepancies explained?

## Questions for the authors
Numbered, focused.

## Comments to authors
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```

---

## Legal scholarship

For law review articles, doctrinal analysis, constitutional and statutory interpretation, comparative law, legal theory, and empirical legal studies — fields where contribution is made through legal argument, interpretation, and engagement with authority.

```markdown
# Review: {paper title}

## Summary
The legal question addressed, the paper's central argument, and its conclusion in 2–4 sentences.

## Doctrinal accuracy
Are authorities (cases, statutes, regulations, treaties) accurately cited and characterized? Holdings correctly stated? Significant contrary authorities engaged?

## Argument
Is the central argument valid and well-constructed? Does it engage the strongest counterarguments?

## Treatment of adverse authority
Does the paper account for controlling or contrary authority? Is the treatment fair and persuasive?

## Normative and descriptive clarity
Is the paper clear about when it describes existing law versus argues what the law should be? Are normative commitments made explicit?

## Policy and implications
If policy arguments are made, are they adequately grounded? Are second-order or systemic effects considered?

## Engagement with scholarship
Is the paper situated within the relevant legal literature, with key interlocutors engaged seriously?

## Questions for the author
Numbered, focused on the legal argument.

## Comments to author
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```

---

## Arts / practice-based research

For creative writing, studio art, musical composition, performance, film and media practice, and architecture as research — fields where the primary contribution is an artifact or practice, and the review evaluates both the work and the knowledge it produces or embodies.

```markdown
# Review: {paper title}

## Summary
The artifact or practice, the research claim it supports, and the contribution in 2–4 sentences.

## Research framing
Is the relationship between practice and research claim clearly articulated? Is the contribution to practice, to scholarly discourse, or both?

## The work
Quality of craft and execution relative to the field. Conceptual coherence between artistic choices and stated research aims. Degree of innovation relative to established practice.

## Practice as method
Is the practice documented in ways that make the research process legible? Are methodological choices explained and justified?

## Contextualization
Is the work situated within relevant artistic traditions, contemporary practice, and critical discourse?

## Documentation and presentation
Is the work adequately documented for academic evaluation? For time-based or ephemeral work, does documentation convey what it does and how it functions as research?

## Questions for the authors
Numbered, focused.

## Comments to authors
[Freeform prose per persona spec]

## Recommendation
{Accept | Minor revision | Major revision | Reject}: [one-sentence justification]

## Confidence
{Low | Medium | High}: [one sentence on why]
```
