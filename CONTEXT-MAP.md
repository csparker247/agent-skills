# Context map

This repo is a *collection* of independent agent skills. Each skill is its own
bounded context with its own glossary — terms do not carry across skills. This file
is a pointer index, not a glossary itself.

## Skills

| Skill | Glossary | Decisions |
| --- | --- | --- |
| [`peer-reviewer`](skills/peer-reviewer/) | [`docs/peer-reviewer/CONTEXT.md`](docs/peer-reviewer/CONTEXT.md) | [`docs/peer-reviewer/adr/`](docs/peer-reviewer/adr/) |

## Repo-wide decisions

Decisions that span the whole repo (not any single skill) live in
[`docs/adr/`](docs/adr/).

## Conventions

- A skill ships from `skills/{skill}/`; only that directory is installed.
- Its documentation lives outside the skill, mirrored under `docs/{skill}/`
  (glossary at `docs/{skill}/CONTEXT.md`, decisions in `docs/{skill}/adr/`), so dev
  docs are never bundled into an install. See [`docs/adr/0001`](docs/adr/0001-skill-docs-live-outside-installable-skill-dirs.md).
- ADR numbering restarts per context: `docs/{skill}/adr/` and `docs/adr/` each have
  their own `0001` sequence.
