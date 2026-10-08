# Contributing to Spectra

## Editing the skill

`skills/spectra/` is the canonical source. `.claude/skills/spectra/` and `.agents/skills/spectra/` are verbatim mirrors — after any change, sync them:

```bash
cp -R skills/spectra/SKILL.md skills/spectra/references skills/spectra/assets .claude/skills/spectra/
cp -R skills/spectra/SKILL.md skills/spectra/references skills/spectra/assets .agents/skills/spectra/
diff -r skills/spectra .claude/skills/spectra && diff -r skills/spectra .agents/skills/spectra && echo SYNC_OK
```

Same for the command (canonical `commands/spectra/init.md` → `.claude/commands/spectra/`, `.agents/commands/spectra/`).

## Conventions

- Keep `SKILL.md` under 500 lines; put detail in `references/` and link to it.
- One CORE per project; modifiers stay composable and token-only (never a second layout system).
- Never invent new core names — add them to `references/catalog.md` and the matching `families/*.md` file first.
- `SPECTRA.md` output must always contain full tokens + rules, never a pointer-only file.

## Test before submitting

1. `/spectra init` with a niche (e.g. "real-estate") → check `SPECTRA.md` tokens render.
2. `/spectra init` with `skip` → browse families → pick core + modifiers.
3. Re-run in a project that already has `AGENTS.md` → marker line must not duplicate.
