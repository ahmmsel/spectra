# Spectra Recipes — tokens + rules per core

Use this when writing `SPECTRA.md`. Start from the CORE recipe, then apply MODIFIERS as token overrides only.

## How to apply CORE + MODIFIERS + DOMAIN

1. CORE sets: palette shape, type roles, spacing/radius/shadow, layout grid, component treatment, motion feel, imagery style.
2. Each MODIFIER adjusts 1–2 token axes (e.g. `Pastel` lightens palette; `3D` adds depth/illustration; `Dark Glass` darkens surfaces + blur; `Leather` adds texture).
3. DOMAIN adds content notes (e.g. real-estate → property photography, map cards, filter density) without changing the visual system.
4. PALETTE (Step 4, see `palettes.md`) overrides the recipe's color tokens only — all other axes stay per CORE.

## Base recipe axes (fill for every SPECTRA.md)

- Colors: `--bg, --surface, --ink, --muted, --accent (+--accent-2), --border`
- Typography: display font + role, body font, mono/data font if needed; scale (e.g. 12/14/16/20/28/40/64)
- Spacing/radius/shadow: base unit (4 or 8pt), radius tokens, shadow tokens (none/soft/hard/glass)
- Layout: grid (12-col, asymmetric, dense, broken), max width, whitespace rhythm
- Components: buttons, cards, inputs, nav, tables/badges per core
- Motion: duration/easing + signature moves (none/subtle/bouncy/glitch/kinetic)
- Imagery: photo/illustration/icon treatment + do/don't

## Worked examples (copy the pattern, don't copy verbatim)

### Example A — Neo-Brutalism + Pastel + 3D + Education
- Colors: pastel bg `#FFF6E9`, ink `#111111`, accent `#7C5CFF`, hard border 2px black
- Type: grotesk display (Archivo/Space Grotesk), bold headlines, thick borders on headings
- Spacing: 8pt, radius 12px, shadow `4px 4px 0 #111`
- Layout: brutalist 12-col grid, chunky cards, sticker-like badges
- Components: hard-shadow buttons/cards, playful 3D illustrations, pastel fills
- Motion: snappy 150ms, hover translate (-2px) + shadow grow
- Imagery: 3D pastel illustrations, no stock gradients

### Example B — Skeuomorphism + Leather + Dark Luxury + Finance
- Colors: deep charcoal `#141210`, leather brown `#4A3428`, brass `#C9A227`, cream ink
- Type: serif display (Playfair/Georgia) + clean sans body + mono numerals
- Surfaces: leather/paper/metal textures, stitched borders, metallic toggles/gauges
- Components: instrument-like cards, dials, heavy buttons with inset highlights
- Motion: slow, weighted (300ms ease-out), gauge-like feedback
- Imagery: macro material shots, no flat icons

### Example C — Swiss + Monochrome + Editorial + Architecture
- Colors: paper `#FAFAF8`, ink `#111`, gray scale only, single red accent optional
- Type: grotesk (Inter/Helvetica Now), tabular numerals, asymmetric headline sizes
- Layout: strict 12-col asymmetric grid, huge whitespace, architectural photography full-bleed
- Components: hairline rules, underline links, minimal buttons, index-like lists
- Motion: near-none (150ms fades only)
- Imagery: B&W/monochrome architecture photos, generous captions

### Example D — Cyberpunk + Holographic + Chrome + AI
- Colors: near-black `#0A0A12`, neon `#00F0FF` + magenta `#FF2BD6`, chrome gradients
- Type: condensed display + mono data (JetBrains Mono/Space Mono)
- Layout: technical grid overlays, HUD frames, glow dividers
- Components: holographic badges, glowing CTAs, scanline panels, chrome pills
- Motion: glitch/flicker accents, 200ms neon hover glows
- Imagery: dark renders, holographic gradients, grid wireframes

## Modifier override cheat-sheet

| Modifier | Changes |
| -------- | ------- |
| Monochrome / B&W | Collapse palette to gray + one accent max |
| Pastel / Candy | Lighten + desaturate fills, keep ink dark |
| Dark / Dark Glass | Darken surfaces, add blur + translucent borders |
| Aurora / Holographic / Iridescent | Add gradient mesh / rainbow sheen on accents |
| 3D / Depth | Add extruded/soft 3D illustration + heavier shadow |
| Geometric / Grid-Heavy | Strengthen grid lines, tiles, blocking |
| Serif / Editorial | Swap display to serif, add captions/pull quotes |
| Glitch / Distortion | Add flicker/displacement motion accents (artistic only) |
| Leather/Paper/Metal/Wood | Add material texture tokens + inset highlights |
| Dense / Data-Driven | Tighten spacing, add tables/mono numerals |

Keep overrides to tokens — never let a modifier reintroduce a different core's layout.
