# Per-discipline rubric files selected via a pre-evaluation table

## Context

[ADR-0001](0001-concise-reviews-with-evaluator-selected-common-structure.md) made the
rubrics content guides rather than output templates, but left them in a single
`references/discipline-rubrics.md` (~1670 words, 8 disciplines). The skill instructs
readers to load that whole file on every run, even though only **one** discipline applies
to a given paper — so ~1480 words are read and discarded each run. On a full panel this is
the single largest source of wasted tokens, dwarfing every other reference file.

The waste is structural, not prose: the file is read whole because it lives whole.

## Decision

Split the rubric material **by consumer**, so each step loads only what it needs:

- **A compact selection table** in `pre-evaluation.md`: one row per discipline =
  `name | matching cue | concise default structure`. The **evaluator** reads only this to
  pick the discipline *and* set the session's common structure — it never touches rubric
  prose. The default structure lives **only** here (single source of truth).
- **One content-guide file per discipline** under `references/rubrics/` (e.g.
  `empirical-sciences.md`), holding only the "what a reviewer in this field evaluates"
  guide. Each **reviewer** reads only the one matching file (~120 words). A
  cross-disciplinary paper reads the two closest files.
- **The shared tail** (`Recommendation {Accept|Minor|Major|Reject}` /
  `Confidence {Low|Medium|High}`) is defined once in `pre-evaluation.md` and referenced
  elsewhere, rather than re-spelled in every persona and `panel.md`.

Net per-run load: the evaluator step drops 1670 → ~150 words; each reviewer reads ~120
words instead of carrying the whole file.

## Considered options

- *Keep one file, read it whole* — the status quo; rejected as the dominant per-run waste.
- *Keep one file, read only a line range* — rejected: line ranges drift as the file is
  edited, and the reader can't know the range without reading the file first.
- *Put default structures only in the rubric files, not the table* — rejected: the evaluator
  would then have to open rubric prose just to learn the structure, defeating the table.

## Consequences

- A future contributor sees 8 small files plus a table instead of one rubric document; this
  ADR records that the fragmentation is deliberate and re-merging would re-bloat every run.
- The selection table and the per-discipline files must stay in sync on discipline names.
- The blended cross-disciplinary case reads two files — still far below the old whole-file load.
