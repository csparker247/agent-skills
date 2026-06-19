# Context: peer-reviewer

Glossary of the core terms in this skill. Definitions only — no implementation detail.

## Terms

### Rubric
A **domain-specific content guide** describing the kinds of things a reviewer in a
given field evaluates (e.g. identification strategy in economics, reporting standards
in clinical work, proof correctness in math). It is *not* a mandatory output template:
its section list informs *what* is evaluated and supplies the domain's
[[common-structure]], but the per-review voice is owned by the [[persona]].

### Common structure
The single ordered set of sections every [[persona]] in a session uses, so all reviews
in one panel share a shape. Selected once by the [[evaluator]] from the matching
[[rubric]] (blending the two closest for cross-disciplinary work) and always ending in
Recommendation + Confidence. Shape is common across a session; content is
domain-specific across sessions; voice varies by persona.

### Evaluator
The pre-evaluation step. Runs once per session before any reviewer. Determines
discipline, paper shortname, summary, and key claims — and selects the session's
[[common-structure]] from the matching [[rubric]].

### Meta-review
The area-chair synthesis across all reviews. It *is* the synthesis — never itself
summarized for display. Always authored by the orchestrating agent (which holds the
pre-evaluation, the paper, and every reviewer's output), in both sequential and
parallel modes; the fanned-out sub-agents in parallel mode are reviewers only.

### Persona
One of the simulated reviewer voices (Reviewer One–Five, plus the area-chair
meta-reviewer). A persona owns the *voice and shape* of its review; it draws on the
relevant [[rubric]] for *what* to evaluate.

### Verbosity override
An explicit instruction — from the user, or self-governed by a persona when substance
genuinely demands it — to exceed the default review length. Absent an override, reviews
target a concise default anchored to a typical paper and scaled by paper length.
