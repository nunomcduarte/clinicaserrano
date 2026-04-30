# Clínica Serrano — Design System

Living documentation of the visual and verbal identity of **Clínica Serrano**, a private medicine clinic in Matosinhos, Portugal.

This system is being reverse-engineered from the brand's existing public-facing assets (Instagram first) so that any future asset — social post, website, signage, document — can be produced consistently and on-brand.

## Repository structure

```
brand/                  Visual foundations (numbered for stable order)
  00-foundations.md     Single-page summary of the visual identity (start here)
  01-colors.md          Palette and tokens
  02-typography.md      The two typefaces and how they're used
  03-logo.md            Wordmark anatomy and placement
  04-texture.md         Paper background and how to reproduce it
  05-photography.md     Image style, light, framing, post-treatment
  06-applications.md    Physical brand surfaces (uniforms, towels, merch)
  07-space-storytelling.md  How the clinic uses memorabilia and materials as brand
  assets/               Source files (textures, vector wordmarks, moodboards) — TBD

voice/
  tone.md               Verbal identity — registers, vocabulary, caption patterns

templates/              Reusable layout patterns
  instagram-multi-service-slide.md      Service-introduction carousels (greige)
  instagram-announcement-carousel.md    Time-sensitive carousels (cream)
  instagram-deep-dive-carousel.md       Single-service deep-dives (hybrid)
  team-portrait-post.md                 Team member introductions (photo)
  space-photo-post.md                   Atmospheric / object posts (photo)

references/             Annotated source assets, organized by type
  carousels/            Multi-slide Instagram carousels
  portraits/            Team-member portraits
  spaces/               Interior / object photographs
  philosophy/           Values / philosophy declarations
  ctas/                 Service-led conversion posts

tokens/                 Machine-readable design tokens (3-layer)
  tokens.json           Index — points to the four layers below
  core.json             Layer 1 — raw primitives (color, font, space, radius)
  semantic.json         Layer 2 — aliases (surface modes, text roles, wordmark)
  components.json       Layer 3 — per-component (cta-pill, wordmark-block, etc.)
  templates.json        Layer 3 — per-template layouts (Instagram canvases, zones)

CHANGELOG.md            ADRs — system-level decisions, append-only
GLOSSARY.md             Canonical terms (surface modes, registers, arcs, etc.)
CONTRIBUTING.md         How to add references, templates, and tokens
STATUS.md               Live dashboard of confirmed / provisional / resolved items
README.md               This file
```

## How to read this system

1. **`brand/00-foundations.md`** — start here. One-page visual identity.
2. **`voice/tone.md`** — verbal identity. Half the brand.
3. **`GLOSSARY.md`** — canonical terms (surface modes, registers, carousel arcs).
4. **`STATUS.md`** — what's confirmed, what's provisional, what's been resolved.
5. **A specific template** (e.g. `templates/instagram-multi-service-slide.md`) when producing a new asset.
6. **A reference** (e.g. `references/carousels/2026-04-30-services.md`) to see how a real asset implements a template.

## How to contribute

See `CONTRIBUTING.md`. The short version:

- New observed asset → add a reference under `references/<subtype>/`.
- New reusable layout → add a template under `templates/`.
- New foundational rule → write an ADR in `CHANGELOG.md` and update affected files.
- New token value → add it to `tokens/core.json` first, then alias up.

## Status

The system has resolved its 🔴 inconsistencies (see `CHANGELOG.md` ADRs 0001–0003) and is now in a 🟡 *provisional but coherent* state. The blockers for promotion to 🟢 are:

- Confirming exact hex values from the original Figma/PSD.
- Identifying the two licensed typefaces (wordmark serif + display sans).
- Producing the missing `templates/service-cta-post.md` and the asset files in `brand/assets/`.

See `STATUS.md` for the full punch list.
