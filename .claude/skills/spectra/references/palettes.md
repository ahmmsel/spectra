# Spectra Palettes — recommended palettes + custom interview

Use in Step 4 (after CORE + MODIFIERS are locked). Each palette fills the color tokens in `SPECTRA.md` (`--bg, --surface, --ink, --muted, --accent, --accent-2, --border`).

## How to present

Pick the 3 palettes for the CORE's family below, apply MODIFIER adjustments, then present as a numbered list with hex swatches + one-line vibe, e.g.:

```text
1. Paper & Ink — bg #FAFAF8, ink #111111, accent #E03E2D — warm paper, one red punch. Best for: Swiss, Minimalism, Editorial
2. Cool Mono — bg #F4F6F8, ink #101418, accent #2563EB — crisp, SaaS-like. Best for: Functionalism, Swiss, Data-Dense
3. Warm Sand — bg #F7F2EA, ink #1C1917, accent #B45309 — earthy, calm. Best for: Minimalism, Organic Modernism
4. Custom — I'll guide you through picking your own colors
5. Default — just use palette 1
```

User picks one number. `Default` = palette 1, no further questions.

## Modifier adjustments (apply before presenting)

| Modifier | Adjustment |
| -------- | ---------- |
| Dark / Dark Glass / Dark Luxury | Flip to dark-bg variant: bg → near-black of same hue family, surface +8% lightness over bg, ink → warm/cool white, keep accents (brighten if contrast < 4.5:1) |
| Monochrome / B&W / Black & White | Collapse to gray ramp + keep at most ONE accent; drop accent-2 |
| Pastel / Candy / Soft | Lighten bg + surface toward tinted white, desaturate accents ~30% |
| Aurora / Holographic / Iridescent / Neon / Chrome | Keep bg dark, set accent + accent-2 to a duo-tone gradient pair (e.g. cyan + magenta) |
| Warm / Warm Gray / Earthy / Leather / Wood | Shift neutrals warm (bg/surface/ink toward yellow-red axis) |
| Cool / Cool Gray | Shift neutrals cool (toward blue axis) |
| High-Contrast / High Contrast | Push bg↔ink to extremes (near-white vs near-black), accent saturated |
| Gold / Brass / Luxury | Accent → metallic gold `#C9A227`, bg deep charcoal, ink cream |

If two modifiers conflict (e.g. `Pastel` + `Dark`), ask the user which wins for the background, then apply the other to accents only.

## Curated palettes (3 per family, hex-complete)

Format: `bg / surface / ink / muted / accent / accent-2 / border`.

### Minimal & Modern

1. **Paper & Ink** — best for Swiss, Minimalism, Editorial
   `#FAFAF8 / #FFFFFF / #111111 / #6B7280 / #E03E2D / #111111 / #E5E5E0`
2. **Cool Mono** — best for Functionalism, Swiss, Data-Dense
   `#F4F6F8 / #FFFFFF / #101418 / #5B6470 / #2563EB / #0EA5E9 / #DDE3EA`
3. **Warm Sand** — best for Minimalism, Organic Modernism, Bauhaus
   `#F7F2EA / #FFFFFF / #1C1917 / #78716C / #B45309 / #1C1917 / #E7DFD3`

### Editorial & Typography

1. **Newsprint** — best for Newspaper, Magazine, Typography-First
   `#FBFAF7 / #FFFFFF / #16130E / #6E675C / #B91C1C / #16130E / #E3DED4`
2. **Fashion Contrast** — best for Fashion Editorial, Editorial, Art Direction
   `#0E0D0B / #1A1815 / #F5F1E8 / #A39E93 / #D4AF37 / #F5F1E8 / #2E2A24`
3. **Gallery White** — best for Editorial, Poster, Magazine
   `#FFFFFF / #F5F4F0 / #111111 / #737373 / #4F46E5 / #111111 / #E5E5E5`

### Tactile & Physical

1. **Leather & Brass** — best for Skeuomorphism, Industrial UI
   `#141210 / #241D16 / #F3EAD8 / #A89880 / #C9A227 / #8C6A1F / #3A3129`
2. **Soft Clay** — best for Claymorphism, Soft UI
   `#FFF7F0 / #FFFFFF / #3F3A36 / #9C8F86 / #F472B6 / #8B5CF6 / #F3E2D3`
3. **Paper Craft** — best for Paper UI, Neumorphism
   `#F2EDE3 / #E9E2D3 / #2E2A24 / #857768 / #2F6B4F / #B45309 / #D8CFBD`

### Glass & Translucent

1. **Aurora Night** — best for Glassmorphism, AI Futurism
   `#0A0A12 / #12121C / #F2F4FF / #8B90A7 / #00F0FF / #FF2BD6 / #2A2A3D`
2. **Frosted Day** — best for Glassmorphism, Spatial UI
   `#EEF2F7 / #FFFFFF / #16202E / #5D6B7E / #4F46E5 / #06B6D4 / #D9E1EC`
3. **Liquid Chrome** — best for Liquid Glass, Spatial UI
   `#101014 / #1B1B22 / #F4F4F6 / #9BA0AE / #E8E8EC / #7C5CFF / #33333D`

### Experimental & Raw

1. **Brutal Paper** — best for Brutalism, Deconstructed
   `#FFFFFF / #F5F5F5 / #000000 / #525252 / #FF4D00 / #0000EE / #000000`
2. **Acid Pastel** — best for Neo-Brutalism, Maximalism
   `#FFF6E9 / #FFFFFF / #111111 / #6B6B6B / #7C5CFF / #00C2A8 / #111111`
3. **Xerox** — best for Anti-Design, Chaotic UI, Organic Brutalism
   `#EDEAE2 / #E0DCD2 / #1A1815 / #6E6A60 / #3D5A38 / #B91C1C / #1A1815`

### Retro & Nostalgic

1. **Vapor Sunset** — best for Vaporwave, Y2K
   `#12081F / #1E0F33 / #FDF4FF / #A78BCA / #FF71CE / #01CDFE / #3B1F5E`
2. **Terminal Phosphor** — best for Pixel Art, Web 1.0, Windows Classic
   `#0B0F0A / #131A12 / #D7FFD7 / #6B8F6B / #33FF33 / #FFB000 / #2A332A`
3. **Aero Gloss** — best for Frutiger Aero, Web 2.0, Retro Futurism
   `#EAF6FB / #FFFFFF / #0F2A3D / #5B7A90 / #0096DC / #7ED321 / #C4E2F0`

### Futuristic & Technology

1. **Cyber Grid** — best for Cyberpunk, Digital Grid
   `#0A0A12 / #13131F / #EDEFFF / #7C84A0 / #00F0FF / #FF2BD6 / #26263A`
2. **Tactical HUD** — best for HUD, Sci-Fi, Industrial Future
   `#0C1110 / #141C1A / #E6F2EC / #6E8579 / #34D399 / #F59E0B / #24302B`
3. **Lab Mono** — best for Terminal / CLI, Cyber Minimalism
   `#000000 / #0D0D0D / #E8E8E8 / #8A8A8A / #FFB000 / #E8E8E8 / #2A2A2A`

### Playful & Expressive

1. **Memphis Pop** — best for Memphis, Sticker UI
   `#FFF9F0 / #FFFFFF / #1F1B24 / #7A7484 / #FF5C8A / #00B8A9 / #1F1B24`
2. **Comic Halftone** — best for Comic UI, Pop Art
   `#FFFDF5 / #FFFFFF / #141414 / #6B6B6B / #E63B2E / #1E56C8 / #141414`
3. **Doodle Notebook** — best for Hand-Drawn, Doodle, Collage
   `#FCFBF4 / #FFFFFF / #2B2620 / #8A8177 / #2F6B4F / #D97706 / #2B2620`

### Organic & Natural

1. **Forest Floor** — best for Organic UI, Biophilic
   `#F6F4EC / #FFFFFF / #1E2A20 / #6B7A6D / #2F6B4F / #8A9A5B / #DDE3D5`
2. **Clay Warmth** — best for Earthy Minimalism, Organic Modernism
   `#FAF5EE / #FFFFFF / #292019 / #8A7A6B / #C05621 / #2F6B4F / #E5DACA`
3. **Wabi Stone** — best for Wabi-Sabi, Japanese Minimalism, Botanical
   `#F4F2ED / #EAE7DE / #2E2C28 / #857F74 / #7A2E2E / #2E2C28 / #D5D0C4`

### Luxury & Premium

1. **Noir & Gold** — best for Dark Luxury, Art Deco
   `#0D0C0A / #171412 / #F3EAD8 / #A89E8A / #C9A227 / #F3EAD8 / #33291C`
2. **Marble Serif** — best for Luxury Minimalism, Neo-Classical, Elegant Editorial
   `#FBFAF8 / #FFFFFF / #1A1815 / #7C746A / #1A1815 / #8C7B4B / #E6E1D8`
3. **Velvet Plum** — best for High Fashion, Premium Monochrome
   `#150F16 / #221822 / #F7EDF3 / #A68FA3 / #C08497 / #F7EDF3 / #3A2A3A`

### Industrial & Technical

1. **Blueprint** — best for Blueprint, Engineering
   `#0F2A52 / #14356A / #EAF1FF / #8FA3C7 / #F5A623 / #EAF1FF / #2A4A82`
2. **Hazard Utility** — best for Industrial, Control Panel, Utility UI
   `#F2F2F0 / #FFFFFF / #1C1C1C / #6B6B6B / #EAB308 / #1C1C1C / #1C1C1C`
3. **Carbon Data** — best for Data-Dense, Technical, Scientific
   `#101216 / #1A1E24 / #E8EBEF / #8B94A1 / #38BDF8 / #A78BFA / #2A3038`

### Cultural & Historical

1. **Ukiyo Wave** — best for Ukiyo-e Inspired, Art Nouveau
   `#F7F4EC / #FFFFFF / #22333B / #75808A / #1D6F8C / #C14436 / #DCD5C2`
2. **Construct Red** — best for Constructivism, Postmodernism
   `#F4F1EA / #FFFFFF / #111111 / #6B6B6B / #C8102E / #111111 / #111111`
3. **Mid-Century Warm** — best for Mid-Century Modern, Bauhaus
   `#FAF3E7 / #FFFFFF / #2A2118 / #8A7A64 / #D95D39 / #2F5D50 / #E0D3BE`

### Gaming & Interactive

1. **Neon Arena** — best for Gaming UI, Esports UI
   `#0A0D14 / #131826 / #F2F5FF / #7E8AA3 / #22D3EE / #A3E635 / #232C44`
2. **RPG Parchment** — best for RPG UI, Fantasy UI
   `#F1E8D2 / #E4D5B5 / #2B2118 / #7A6A54 / #8C2F2F / #2F5D50 / #4A3A28`
3. **CRT Arcade** — best for Arcade UI, Sci-Fi Gaming
   `#080A10 / #10141D / #D8F3DC / #5C7A64 / #FF2E88 / #00E5FF / #232B38`

## Custom interview (user picked `Custom`)

Ask one question at a time. Accept hex (`#0EA5E9`) or plain names (`deep teal`, `warm cream`) — convert names to hex yourself and always show the resolved hex for confirmation.

- **Q1 — Primary / brand color:** "What's your primary brand color? (hex like `#4F46E5` or a name like 'deep indigo')"
- **Q2 — Secondary color:** "And a secondary/support color? (hex, a name, or `derive` and I'll pick a harmonious one)"
- **Q3 — Background:** "Light or dark background? (`light` / `dark` / `follow core` to use the {{CORE}} default)"
- **Q4 — Accent / action color:** "What color should buttons, links and key actions use? (hex, a name, or `same` to reuse the primary)"
- **Q5 — Neutral temperature:** "Should grays lean warm, cool, or neutral? (`warm` / `cool` / `neutral`)"

### Validation (before generating)

1. **Contrast:** check primary-on-bg, ink-on-bg, accent-on-bg against a ~4.5:1 bar for text. If a pair fails, warn with the approximate ratio and propose the minimal fix (darken/lighten one side one step), then ask to `accept fix` or `revise`.
2. **Modifier conflict:** if MODIFIERS include `Monochrome / B&W / Black & White` and the custom palette has 2+ distinct hues, or `Pastel` with fully saturated picks, warn and ask to confirm the combination or drop/adjust.
3. **Showdown:** present the final swatch table (`bg / surface / ink / muted / accent / accent-2 / border`) and get an explicit OK before writing `SPECTRA.md`.

### Derivation rules

- `derive` secondary → complementary or analogous hue to primary at same saturation band.
- `follow core` background → use the CORE recipe's default bg lightness.
- surface → bg shifted 3–6% toward ink; muted → ink at ~55% desaturated; border → bg/ink midpoint at low emphasis; accent-2 → secondary, or primary shifted 40° hue if no secondary.
- Warm/cool/neutral → push bg, surface, ink, muted, border along that temperature axis.
