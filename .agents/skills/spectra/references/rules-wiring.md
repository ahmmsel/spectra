# Rules-file wiring

After writing `./SPECTRA.md`, wire it into the project's agent rules file so every future agent run follows it.

## Detection order (first match wins)

1. `AGENTS.md`
2. `CLAUDE.md`
3. `.cursorrules` or `.cursor/rules`
4. `.windsurf/rules`
5. `.github/copilot-instructions.md`
6. None found → create `AGENTS.md`

## Append block (idempotent)

Check first: if the target file already mentions `SPECTRA.md`, do nothing.

Otherwise append:

```md
> Design direction: see ./SPECTRA.md — all UI work MUST follow its tokens, components, layout, motion, and imagery rules.
```

## Report

Tell the user which file was created/updated, e.g.:
- "Wired into existing AGENTS.md"
- "No rules file found — created AGENTS.md with SPECTRA.md reference"
