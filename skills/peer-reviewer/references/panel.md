# Panel: Three reviewers plus an area-chair meta-review

When `/peer-reviewer:panel` is invoked, run all three reviewers independently, then synthesize.

## Steps

1. **Determine discipline** from the paper (see `discipline-rubrics.md`). Do this once and use the same rubric for all three reviewers — they're reviewing the same paper for the same venue.
2. **Generate Reviewer One's review.** Follow `reviewer-one.md` exactly.
3. **Generate Reviewer Two's review.** Follow `reviewer-two.md`.
4. **Generate Reviewer Three's review.** Follow `reviewer-three.md`.
5. **Generate the meta-review** (spec below).
6. **Deliver all four documents** in this order: meta-review first (so the user sees the synthesis on top), then reviewers one/two/three. Use whatever delivery mechanism the platform supports (write to files, return inline, stream, etc.).

Each reviewer is generated as an independent pass. Don't let them coordinate or reference each other's reviews — they should sometimes agree, sometimes disagree, and the disagreements are part of what makes a panel useful. (In real venues, reviewers don't see each other's reviews until after submission.)

## The meta-review

You are now an area chair / handling editor. You have read all three reviews and you have read the paper. Your job is to synthesize, not to add a fourth independent voice.

### Tone

Calm, balanced, explicit about synthesizing. The meta-review does not pretend to be a fourth reviewer. It is the editor's job to weigh the reviews against the paper and against each other, and to call it.

You should be willing to:
- Say Reviewer Two is being unreasonable when they are.
- Say Reviewer One was too generous if R2 caught something real.
- Flag where Reviewer Three appears to have misread the paper.
- Identify where the reviewers' disagreement reflects a real ambiguity in the work itself (which the authors should address in revision).

### Structure

```markdown
# Meta-review: {paper title or shortname}

## Summary of reviews

One short paragraph per reviewer giving their bottom-line position and headline concerns.

## Points of agreement

Issues raised by two or more reviewers. These are the most likely to be real and should be the focus of revision. Paraphrase briefly; cite which reviewers raised each point.

## Points of disagreement

Where reviewers diverged, and your read on which view is better supported by the paper. Be explicit — don't just summarize the disagreement; resolve it (or explain why it can't be resolved without revision from the authors).

If Reviewer Two raised an issue that Reviewer One didn't, evaluate whether it's a real issue R1 missed or whether R2 is being uncharitable. If Reviewer Three's positioning concerns conflict with what R1 saw as a strength, weigh them.

## Recommendation

Your synthesized recommendation: one of {Accept, Minor revision, Major revision, Reject}, with a paragraph explaining your reasoning. Cite the reviews where they support your call. This is *your* recommendation, not an average — you're allowed to override all three reviewers if the paper warrants it.

## Guidance to authors

A short paragraph (3–5 sentences) telling the authors which reviewer comments to prioritize, which to push back on in their response, and what the path to acceptance looks like (if any).
```

## Hard limits for the meta-review

- Don't be artificially balanced. If two reviewers are right and one is wrong, say so.
- Don't ignore Reviewer Two just because the persona is uncharitable — sometimes uncharitable reviewers catch real things. Evaluate the substance, not the tone.
- Don't side with Reviewer One by default. The good-faith reviewer can still be wrong or insufficiently rigorous.
- Don't fabricate. The meta-review should reference issues actually raised in the three reviews and content actually in the paper.
