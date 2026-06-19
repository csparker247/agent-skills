# Panel: Reviewers plus an area-chair meta-review

**Default panel**: reviewers one, two, three. Add reviewers four or five when the user asks for them.

## Execution modes

**Sequential** (default): run steps 0–3 in order in a single context. Pre-evaluation output is available to each reviewer through shared conversation context.

**Parallel**: run step 0 first. Once pre-evaluation is complete, run each reviewer concurrently — each as a separate agent with the pre-evaluation output (including the session's common structure) in its prompt. The fanned-out agents are **reviewers only**; the orchestrating agent collects their outputs and writes the meta-review itself — it already holds the pre-evaluation, the paper, and every review, so no separate meta-review agent is needed. Parallel execution requires a platform that supports concurrent agents. Sequential is the right default when token efficiency matters or the platform doesn't support it.

## Steps

0. **Pre-evaluate** the paper per `pre-evaluation.md`. Produce discipline, shortname, venue, summary, key claims, and the session's **common structure**. This runs once regardless of execution mode.
1. **Generate each reviewer's review** independently, following their persona file and the common structure from step 0. Reviewers do not coordinate or reference each other — they should sometimes agree and sometimes disagree, and the disagreements are part of what makes a panel useful.
2. **Generate the meta-review** (spec below), authored by the orchestrating agent.
3. **Deliver** per the console/file rules in `SKILL.md`: write each review to a file, then print the meta-review verbatim plus a one-line verdict per reviewer and the filenames.

## The meta-review

You are the area chair. You've read all reviews and the paper. Synthesize — don't add another independent reviewer voice. Keep it tight: stay within the meta-review cap in `SKILL.md` (the synthesis should be shorter than reading the reviews themselves).

```markdown
# Meta-review: {shortname from pre-evaluation}

## Summary of reviews
One sentence per reviewer: bottom-line position and headline concern.

## Points of agreement
Issues raised by two or more reviewers. Most likely real; should drive revision. Cite which reviewers.

## Points of disagreement
Where reviewers diverged — and your resolution. Don't just describe the disagreement; resolve it (or explain why only the authors can). Weigh reviewer scope: R2 may be uncharitable vs. catching something real; R3 may have skimmed past something R1 caught; R4's methods concerns are their specialty; R5's domain concerns may be outside the other reviewers' competence to assess.

## Recommendation
{Accept | Minor revision | Major revision | Reject}. Paragraph explaining reasoning. This is your call, not an average — you can override any reviewer if the paper warrants it.

## Guidance to authors
3–5 sentences: which comments to prioritize, which to push back on, what the path to acceptance looks like.
```

## Hard limits

- Don't be artificially balanced. Two right and one wrong — say so.
- Don't ignore R2 just because the persona is uncharitable. Evaluate substance, not tone.
- Don't default to R1. The good-faith reviewer can still be wrong.
- Don't fabricate. Reference only issues actually raised and content actually in the paper.
