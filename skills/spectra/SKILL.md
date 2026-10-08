---
name: spectra
description: Guided design-direction picker for websites and apps. Use whenever the user mentions /spectra init, design direction, design system, visual style, modifiers, SPECTRA.md, starting UI styling, or needs a consistent visual language before building UI.
---

# Spectra — Design Direction Skill

Help the user pick one **Core Design System** + optional **Modifiers** + **Color Palette** for their project, then lock it in as `SPECTRA.md` and wire it into their agent rules file.

Mental model (never let every row become an independent style):

```text
CORE DESIGN SYSTEM (visual rules)
        ↓
    + MODIFIERS (token overrides, composable, 0–3)
        ↓
    + PALETTE (recommended pick or guided custom)
        ↓
    + DOMAIN (free-text niche, e.g. real-estate, ecommerce, SaaS)
        ↓
    complete, consistent UI
```

## Workflow (`/spectra init`)

Follow these steps in order. Ask one question at a time. Keep lists numbered so the user can reply with a number.

### Step 1 — Niche (free-text, skippable)

Ask exactly this (free-text, no fixed list):

> "What are you building? Describe your niche/product in a few words (e.g. real-estate listings, fashion ecommerce, SaaS dashboard, restaurant site…). Type `skip` to browse all design families instead."

- If answered: store as `DOMAIN` and go to Step 2a (recommend).
- If `skip`: set `DOMAIN=General` and go to Step 2b (browse).

### Step 2a — Recommend (DOMAIN given)

1. Read `references/catalog.md` for the ~35 supported cores.
2. Rank the top 3–4 Core Systems that fit the DOMAIN. Use these heuristics, plus judgment:
   - Trust/finance/legal/medical → Swiss, Functionalism, Minimalism, Skeuomorphism (+Dark Luxury for premium finance)
   - Real-estate/architecture → Swiss (+Monochrome/Editorial), Modernist, Organic Modernism
   - Ecommerce/fashion → Editorial, Fashion Editorial, Luxury Minimalism, Memphis/Sticker (playful shops)
   - SaaS/dashboard/data → Functionalism, Material, Flat 2.0, Data-Dense, Terminal (dev tools)
   - Editorial/blog/media → Editorial, Magazine, Newspaper, Typography-First
   - AI/tech/futuristic → AI Futurism, Cyberpunk, HUD, Glassmorphism, Spatial UI
   - Playful/kids/education → Neo-Brutalism (+Pastel/3D), Claymorphism, Hand-Drawn, Doodle
   - Luxury/premium → Dark Luxury, Luxury Minimalism, Art Deco, Elegant Editorial
   - Retro/gaming → Y2K, Arcade, Pixel Art, Gaming UI, Vaporwave
3. Present as a numbered list with one-line rationale each, e.g.:
   `1. Swiss + Monochrome — strict grid, fits property photography`
   End with: `4. Browse all families instead`
4. User picks one → that is `CORE`. Go to Step 3.

### Step 2b — Browse (skipped niche)

1. List the 13 families from `references/catalog.md` (Minimal & Modern, Editorial & Typography, Tactile & Physical, Glass & Translucent, Experimental & Raw, Retro & Nostalgic, Futuristic & Technology, Playful & Expressive, Organic & Natural, Luxury & Premium, Industrial & Technical, Cultural & Historical, Gaming & Interactive).
2. User picks a family → read the matching `references/families/*.md` file and list its Core Systems.
3. User picks one → that is `CORE`. Go to Step 3.

### Step 3 — Modifiers (optional, composable)

1. Show the `Potential modifiers` row for the chosen CORE (from catalog/family file).
2. Ask: "Pick 0–3 modifiers (comma-separated numbers, or `none`). You may also combine cross-family, e.g. Leather + Dark Luxury."
3. Store as `MODIFIERS` (empty allowed). Modifiers only override tokens (palette, texture, depth, type flavor) — they never replace the core's layout/component rules. See `references/recipes.md`.

### Step 4 — Palette (recommended or custom)

1. Read `references/palettes.md`. Take the 3 curated palettes for the CORE's family, apply MODIFIER adjustments, and present as a numbered list with hex swatches + one-line vibe each, ending with `Custom` and `Default` options.
2. If the user picks a recommended palette (or `Default` = first listed): store as `PALETTE` with source `recommended` and go to Step 5.
3. If the user picks `Custom`: run the guided interview from `references/palettes.md` — Q1 primary → Q2 secondary (or `derive`) → Q3 background (`light`/`dark`/`follow core`) → Q4 accent (or `same`) → Q5 neutral temperature. Accept hex or plain color names (convert + confirm resolved hex). Then run validation (contrast check with fix offer, modifier-conflict warning) and show the final swatch table for explicit OK. Store as `PALETTE` with source `custom` and go to Step 5.

### Step 5 — Generate `SPECTRA.md`

1. Read `references/spectra-template.md` and `references/recipes.md` for the CORE (+MODIFIERS adjustments).
2. Write `./SPECTRA.md` in the project root (cwd where `/spectra init` was run — not inside the skill folder).
3. The file MUST contain full tokens + rules (colors, typography, spacing/radius/shadow, layout, components, motion, imagery) plus a pointer back to the skill reference, per `references/rules-wiring.md`. Never write a pointer-only file.
4. Overwrite only after confirming with the user if `SPECTRA.md` already exists.

### Step 6 — Wire into rules file (auto-detect + append)

Follow `references/rules-wiring.md`:

1. Detect in project root, first match wins: `AGENTS.md` → `CLAUDE.md` → `.cursorrules` / `.cursor/rules` → `.windsurf/rules` → `.github/copilot-instructions.md`.
2. If none exists, create `AGENTS.md`.
3. Append idempotently (skip if a `SPECTRA.md` marker already exists):
   `> Design direction: see ./SPECTRA.md — all UI work MUST follow its tokens, components, layout, motion, and imagery rules.`
4. Tell the user which file was updated/created.

### Step 7 — Confirm

Reply with: chosen `DOMAIN + CORE + MODIFIERS + PALETTE (name + source)`, files written (`SPECTRA.md`, rules file touched), and one sentence on what to do next (build UI following `SPECTRA.md`).

## Rules

- One CORE only per project. Modifiers are composable, max 3.
- Crystal / Translucent / Holographic are modifiers of Glassmorphism, not independent cores, unless the family file gives an explicit recipe.
- Never invent a new core name — pick from `references/catalog.md`.
- Keep `SKILL.md` lean; read family files only when needed.

## Reference index

| Need | Read |
| ---- | ---- |
| Full core + modifier list | `references/catalog.md` |
| Family detail | `references/families/*.md` |
| Token/component/layout/type/motion/imagery recipes | `references/recipes.md` |
| Recommended palettes + custom interview | `references/palettes.md` (`data/palettes.yaml` = machine-readable mirror) |
| Cores + modifiers, machine-readable | `data/cores.yaml` (mirror of `references/catalog.md`) |
| SPECTRA.md template | `references/spectra-template.md` |
| Rules-file wiring | `references/rules-wiring.md` |
