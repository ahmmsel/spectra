# /spectra init

Run the Spectra design-direction interview, then lock the result into `SPECTRA.md`.

Invoke the `spectra` skill and follow its Workflow (`Step 1 → Step 7`):

1. Ask for the niche (free-text, `skip` allowed).
2. Recommend 3–4 core systems if a niche was given, otherwise browse the 13 families.
3. Ask for 0–3 modifiers (composable, `none` allowed).
4. Offer 3 recommended palettes for the chosen direction (+ `Custom` guided color interview, or `Default`). See `references/palettes.md`.
5. Generate `./SPECTRA.md` in the project root from `references/spectra-template.md` + `references/recipes.md` — full tokens + rules, never pointer-only. Confirm before overwriting.
6. Auto-detect the rules file (`AGENTS.md` → `CLAUDE.md` → `.cursorrules`/`.cursor/rules` → `.windsurf/rules` → `.github/copilot-instructions.md`, else create `AGENTS.md`) and append the `SPECTRA.md` marker idempotently.
7. Confirm: domain + core + modifiers + palette, files written.
