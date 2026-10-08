# Spectra — Design Direction Skill

Pick a consistent visual language for your website or app **before** you build UI: one **Core Design System** + optional **Modifiers**, locked into a `SPECTRA.md` file that every agent in the project must follow.

Run `/spectra init`, answer what you're building (or `skip`), pick a direction and modifiers — done.

## How it works

```text
CORE DESIGN SYSTEM (visual rules)
        ↓
    + MODIFIERS (composable token overrides, 0–3)
        ↓
    + DOMAIN (your niche, free-text: real-estate, ecommerce, SaaS…)
        ↓
    SPECTRA.md → full tokens + layout + component + type + motion + imagery rules
```

`/spectra init` will:

1. Ask what you're building (free-text, `skip` to browse everything).
2. Recommend 3–4 core systems for your niche, or let you browse all 13 families (~35 cores: Swiss, Neo-Brutalism, Glassmorphism, Editorial, Cyberpunk, Dark Luxury, …).
3. Let you pick 0–3 modifiers (e.g. `Pastel + 3D`, `Leather + Dark Luxury`).
4. Generate `./SPECTRA.md` in your project root — full design tokens and rules, not just a pointer.
5. Auto-wire it into your rules file (`AGENTS.md` → `CLAUDE.md` → Cursor/Windsurf/Copilot instructions, creating `AGENTS.md` if none exists).

## Install

**Claude Code:** copy (or symlink) `.claude/skills/spectra` and `.claude/commands/spectra` into your project's `.claude/` directory.

**OpenCode / generic agents:** copy (or symlink) `.agents/skills/spectra` and `.agents/commands/spectra` into your project's `.agents/` directory — or use `skills/spectra` + `commands/spectra`, which is the canonical, runtime-agnostic source both mirrors are copied from.

**Cursor / Windsurf / Copilot:** use the canonical `skills/spectra/SKILL.md` as the skill definition however your tool consumes skills; the generated `SPECTRA.md` reference is appended to your rules file automatically.

## Repo layout

```text
skills/spectra/                 # canonical source (runtime-agnostic)
  SKILL.md                      # interview workflow + routing (<500 lines)
  references/
    catalog.md                  # all ~35 cores + modifiers
    families/01–13_*.md         # full per-family tables
    recipes.md                  # token/component/layout/type/motion/imagery recipes
    spectra-template.md         # SPECTRA.md template
    rules-wiring.md             # rules-file auto-detect + append logic
  assets/
.claude/skills/spectra/         # mirror for Claude Code (kept in sync with canonical)
.claude/commands/spectra/       # /spectra init for Claude Code
.agents/skills/spectra/         # mirror for agent runtimes (kept in sync)
.agents/commands/spectra/
commands/spectra/               # canonical command definition
```

When editing the skill, edit `skills/spectra/` first, then copy the change into both mirrors (see `CONTRIBUTING.md`).

## Examples

- Neo-Brutalism + Pastel + 3D → education platform
- Skeuomorphism + Leather + Dark Luxury → premium finance app
- Swiss + Monochrome + Editorial → architecture studio site
- Cyberpunk + Holographic + Chrome → AI product

## Contributing

See `CONTRIBUTING.md`.

## License

MIT — see `LICENSE`.
