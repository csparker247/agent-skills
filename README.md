# Skills

This repository contains custom skills designed to be installable with `npx`.

## Installing a skill (generic)

Use `npx` with the skill package name:

```bash
npx <skill-package-name>@latest
```

Example:

```bash
npx @your-scope/my-skill@latest
```

If the skill supports arguments, append them after the package name:

```bash
npx <skill-package-name>@latest --help
```
