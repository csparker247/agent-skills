# Discipline-specific review rubrics

These rubrics are **content guides, not output templates**. Each describes the kinds of
things a reviewer in that field evaluates, and names a **concise default structure** — the
short ordered section list the [pre-evaluation step](pre-evaluation.md) selects as the
session's common structure. Pick the rubric whose methodology best matches the paper; default
to **Empirical sciences** when unsure; blend the two closest when the paper crosses fields
(digital humanities, computational social science, applied ML in a scientific domain).

How the pieces fit:

- The **content guide** tells each reviewer *what* to evaluate. A reviewer considers all of it,
  but folds the relevant points into the session's sections as prioritized prose — it does **not**
  emit a heading per checklist item.
- The **concise default structure** is the ordered section list. The evaluator selects one
  structure for the whole session; every reviewer uses it, varying only in voice and emphasis.
- Every structure ends with the **shared tail**:
  - **Recommendation**: one of {Accept, Minor revision, Major revision, Reject}, one-sentence justification.
  - **Confidence**: {Low, Medium, High}, one sentence on why.
- **Length** (target, cap, verbosity override) is governed by `panel.md` and the persona files,
  not here. The verbosity override gives a review more room to develop the same sections — it
  never adds headings beyond the selected structure.

Voice asymmetries (Reviewer Two's terseness, Reviewer Three's gestural vagueness on technical
points, Reviewer Four's methods-only focus, Reviewer Five's domain framing) are described in
each persona file and applied within whatever structure the evaluator selects.

---

## Empirical sciences

For ML, systems, empirical CS, physics, biology, neuroscience, quantitative social science, epidemiology, and similar fields where claims rest on experiments, measurements, or data analysis.

**What a reviewer in this field evaluates:**

- **Technical soundness** — methods appropriate to the questions, statistics correct, baselines and controls adequate, confounds addressed.
- **Empirical evaluation** — experiments sufficient to support the claims, ablations present where the contribution warrants them, evaluation set appropriate, results reported with adequate detail (variance, multiple seeds, error bars).
- **Reproducibility** — enough information (code, data, hyperparameters, environment) for an informed reader to reproduce; missing pieces attributable to legitimate constraints vs. oversight.
- **Clarity** — writing, figures, notation, structure (raise only when there are real issues).

**Concise default structure:** Summary · Strengths · Weaknesses · *(shared tail)*

Summary is 2–4 sentences in the reviewer's own words. Strengths and Weaknesses are prioritized — most important first; weaknesses ordered by impact (unsupported claims > methodological gaps > missing baselines/controls > clarity). Fold technical soundness, empirical evaluation, and reproducibility into Weaknesses; fold any author-facing questions in as well.

---

## Theory / math

For pure math, theoretical CS, formal methods, proof-based work, foundational ML theory.

**What a reviewer in this field evaluates:**

- **Significance** — do these results matter, and to whom? Do they open directions, close open problems, or extend known results? Be specific about what the result enables.
- **Originality** — genuinely new ideas vs. technical extension of prior work (both can be valid; be explicit which).
- **Correctness** — spot-check key lemmas; are proofs complete and rigorous; where is the argument unclear, hand-wavy, or gapped?
- **Exposition and prior work** — clean definitions, illuminating examples, readable proofs; engagement with the right literature and clear articulation of the delta.

**Concise default structure:** Summary · Significance · Correctness · *(shared tail)*

Summary states the main results precisely — theory readers care about exact statements. Fold originality, exposition, and relationship to prior work into Significance or Correctness as appropriate; fold technical questions in too. In Confidence, note whether you verified the proofs.

---

## Humanities

For history, literary studies, philosophy, theology, art history, qualitative interpretive work, and other fields where contribution is made through argument, interpretation, and engagement with sources.

**What a reviewer in this field evaluates:**

- **Argument** — is the central argument clear, well-structured, and defended? Are the moves valid and well-supported? Where is it strongest, and where does it depend on assumptions the reader is asked to grant?
- **Evidence and sources** — primary and secondary sources used appropriately and accurately; gaps in source coverage; use of sources fair to context rather than selectively distorting.
- **Engagement with scholarship** — situated in the field's ongoing conversations; key interlocutors engaged rather than nominally cited; relevant debates acknowledged.
- **Methodology and style** — archival/hermeneutic/comparative/philological approach appropriate and its limits acknowledged; prose, organization, and citation practices serve the intended readership.

**Concise default structure:** Summary · Argument · Evidence & engagement · *(shared tail)*

Summary gives the thesis and central argument in the reviewer's own words. Fold sources, scholarly engagement, methodology, and style into Argument and Evidence & engagement; fold author-facing questions in too.

---

## Design / qualitative HCI

For HCI, design research, qualitative user studies, mixed-methods empirical work, ethnography, and applied research where the contribution is in articulating a problem, designing an artifact or intervention, or surfacing findings from participants.

**What a reviewer in this field evaluates:**

- **Motivation and framing** — problem well-motivated, scope clear, why this matters and to whom.
- **Methodology** — method appropriate to the research questions; participants (recruitment, sample, fit); procedures (data collection, instrument design); analysis (coding process, theme generation, validity practices).
- **Findings** — clearly presented and grounded in the data; claims beyond the data signaled; quotes illustrative rather than load-bearing where they shouldn't be.
- **Implications and reflexivity** — implications for design/theory/practice proportionate to the evidence; limits acknowledged (sample, setting, positionality).

**Concise default structure:** Summary · Framing & methods · Findings & implications · *(shared tail)*

Summary gives the research questions and what the paper found/built/argued. Fold motivation, methodology, findings, implications, and reflexivity into the two middle sections; fold author-facing questions in too.

---

## Clinical / health sciences

For clinical trials, RCTs, systematic reviews, meta-analyses, epidemiology, public health, health services research, and medical education — fields where claims rest on human-subjects data and reporting standards are codified.

**What a reviewer in this field evaluates:**

- **Study design** — appropriateness to the question; trial registration; blinding, randomization, allocation concealment.
- **Population and sampling** — eligibility, recruitment, sample-size justification, representativeness; does the population support the claimed generalizability?
- **Intervention/exposure and outcomes** — fidelity, adequate comparator, dose/duration; primary and secondary outcomes pre-specified and clinically meaningful; valid measurement.
- **Statistical analysis** — appropriate methods, handling of missing data, multiplicity, effect sizes with confidence intervals (not p-values alone).
- **Reporting and ethics** — applicable guidelines (CONSORT, PRISMA, STROBE) followed and deviations justified; IRB approval, informed consent, adverse-event reporting, data safety monitoring.

**Concise default structure:** Summary · Design & population · Outcomes & analysis · Reporting & ethics · *(shared tail)*

Summary gives design, population, intervention/exposure, primary outcome, and main finding in 2–4 sentences. Fold the checklist points into the three middle sections; fold author-facing questions in too.

---

## Economics / econometrics

For applied microeconomics, macroeconomics, labor, development, health, and public economics — fields where the central contribution often turns on the credibility of a causal identification strategy.

**What a reviewer in this field evaluates:**

- **Contribution** — new identification strategy, data, context, or theory, articulated relative to the literature.
- **Identification strategy** — what is the causal claim and how is it identified? Are identifying assumptions credible and tested? IV (strong first stage, defensible exclusion restriction); RDD (no manipulation at threshold); DiD (parallel trends plausible and tested); structural (assumptions transparent, model motivated).
- **Data** — sources, sample construction, variable definitions, measurement error, fit to the question.
- **Robustness and magnitude** — stability across specifications/bandwidths/samples; placebo and falsification tests; standard errors appropriate to the data structure; effect sizes economically meaningful; welfare/distributional implications discussed; comparison to existing estimates.

**Concise default structure:** Summary · Identification · Data & robustness · *(shared tail)*

Summary gives research question, identification strategy, data source, and main result in 2–4 sentences. Fold contribution, data, robustness, magnitude, and relationship to prior literature into the two middle sections; fold author-facing questions in too.

---

## Legal scholarship

For law review articles, doctrinal analysis, constitutional and statutory interpretation, comparative law, legal theory, and empirical legal studies — fields where contribution is made through legal argument, interpretation, and engagement with authority.

**What a reviewer in this field evaluates:**

- **Doctrinal accuracy** — authorities (cases, statutes, regulations, treaties) accurately cited and characterized; holdings correctly stated; significant contrary authorities engaged.
- **Argument** — central argument valid and well-constructed; strongest counterarguments engaged; controlling or contrary authority accounted for fairly.
- **Normative/descriptive clarity** — clear about when it describes existing law vs. argues what the law should be; normative commitments explicit.
- **Policy and scholarship** — policy arguments adequately grounded with second-order effects considered; situated within the relevant legal literature with key interlocutors engaged.

**Concise default structure:** Summary · Doctrinal accuracy · Argument · *(shared tail)*

Summary gives the legal question, the central argument, and its conclusion in 2–4 sentences. Fold treatment of adverse authority, normative/descriptive clarity, policy, and scholarly engagement into the two middle sections; fold author-facing questions in too.

---

## Arts / practice-based research

For creative writing, studio art, musical composition, performance, film and media practice, and architecture as research — fields where the primary contribution is an artifact or practice, and the review evaluates both the work and the knowledge it produces or embodies.

**What a reviewer in this field evaluates:**

- **Research framing** — relationship between practice and research claim clearly articulated; contribution to practice, to scholarly discourse, or both.
- **The work** — quality of craft and execution relative to the field; conceptual coherence between artistic choices and stated research aims; innovation relative to established practice.
- **Practice as method** — practice documented so the research process is legible; methodological choices explained and justified.
- **Contextualization and documentation** — situated within relevant artistic traditions, contemporary practice, and critical discourse; adequately documented for academic evaluation (especially for time-based or ephemeral work).

**Concise default structure:** Summary · The work · Research framing & contextualization · *(shared tail)*

Summary gives the artifact or practice, the research claim it supports, and the contribution in 2–4 sentences. Fold practice-as-method and documentation into the two middle sections; fold author-facing questions in too.
