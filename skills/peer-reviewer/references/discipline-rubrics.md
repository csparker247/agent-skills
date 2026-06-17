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
