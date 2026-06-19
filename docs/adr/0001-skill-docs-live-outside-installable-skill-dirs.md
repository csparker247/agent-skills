# Skill docs live outside installable skill directories

## Context

This repo is a collection of agent skills, installed with
`npx skills add csparker247/agent-skills`. The installer bundles a skill's directory
(`skills/{skill}/`) into the end user's environment. At the time of writing the repo
held one skill, `peer-reviewer`, but it is built to grow to many.

Two structural questions followed from that:

1. Is the repo a single bounded context, or many? Two skills share no domain language —
   `peer-reviewer`'s glossary (Persona, Rubric, Evaluator) means nothing to a future
   skill. They are independent contexts.
2. Where do internal dev docs (glossaries, ADRs) live? The conventional answer is to
   co-locate them with the code they describe — but co-locating them inside
   `skills/{skill}/` would ship them to every install, polluting the user's environment
   with our internal decision records.

## Decision

- **The repo is a multi-context collection.** A root [`CONTEXT-MAP.md`](../../CONTEXT-MAP.md)
  is a pointer index to each skill's context. There is no repo-wide glossary unless a
  genuinely shared vocabulary emerges across skills.
- **Dev docs live outside the installable skill directory, mirrored under `docs/`.**
  Each skill's glossary is `docs/{skill}/CONTEXT.md` and its decisions live in
  `docs/{skill}/adr/`. Only `skills/{skill}/` is installed, so no internal doc ships.
- **ADR numbering is local to each context.** `docs/{skill}/adr/` and the repo-wide
  `docs/adr/` each start at `0001`; the path disambiguates them.

## Considered options

- *Single root context with namespaced terms* — rejected: forces unrelated skills to
  share one glossary; gets unwieldy as skills are added.
- *Co-locate docs inside `skills/{skill}/`* (the usual convention) — rejected: those
  files would be bundled into every install. The install boundary outweighs the
  convenience of co-location.
- *One global ADR counter across all contexts* — rejected: couples unrelated skills
  (you'd scan every folder to pick the next number) for no benefit.

## Consequences

- Docs are not co-located with the code they describe, so the link between a skill and
  its docs is by convention (`skills/{skill}/` ↔ `docs/{skill}/`) rather than proximity.
  `CONTEXT-MAP.md` makes the mapping explicit.
- Adding a skill means adding a `CONTEXT-MAP.md` row and a `docs/{skill}/` folder.
- The installed skill stays clean — only runtime files (`SKILL.md`, `references/`,
  `README.md`) ship.
