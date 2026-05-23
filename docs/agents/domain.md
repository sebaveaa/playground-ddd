# Domain Docs

How the engineering skills should consume this repo's domain documentation when exploring the codebase.

## Before exploring, read these

- `CONTEXT.md` at the repo root.
- `docs/adr/` for architecture decisions relevant to the area being changed.

If these files don't exist yet, proceed silently.

## File structure

This repo is configured as a single-context repo:

```
/
|- CONTEXT.md
|- docs/adr/
`- src/
```

## Use the glossary's vocabulary

When naming domain concepts, prefer the terms defined in `CONTEXT.md`.

## Flag ADR conflicts

If a proposal or change contradicts an existing ADR, surface that explicitly instead of silently overriding it.
