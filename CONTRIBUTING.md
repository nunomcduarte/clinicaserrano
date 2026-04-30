# Contributing

How to add to the Clínica Serrano design system without breaking it.

## Before you change anything

1. Read `brand/00-foundations.md`. It's the single-page summary of the visual identity.
2. Read `voice/tone.md`. The verbal identity is half the brand.
3. Read `GLOSSARY.md`. The system has named concepts (surface modes, registers, arcs); using the right vocabulary keeps the docs coherent.
4. Skim `CHANGELOG.md`. ADR entries record decisions you should not silently reverse.

## File layout

```
brand/        Visual foundations (numbered for stable order on GitHub)
voice/        Verbal identity
templates/    Reusable layout patterns
references/   Annotated source assets, organized by type
tokens/       Machine-readable design tokens (3-layer: core → semantic → components/templates)
CHANGELOG.md  ADRs — system-level decisions
GLOSSARY.md   Canonical terms
STATUS.md     Confirmed / provisional / resolved items
```

## Adding a new reference

References document a real, observed asset (a published Instagram post, a printed piece, a clinic surface). One file per asset.

### Filename

`references/<subtype>/YYYY-MM-DD-<slug>.md`

Where `<subtype>` is one of: `carousels`, `portraits`, `spaces`, `philosophy`, `ctas`. Add a new subtype directory only if the asset doesn't fit any existing one.

### Required frontmatter

```yaml
---
type: reference
subtype: carousel | portrait | space | philosophy | cta
status: confirmed | provisional | inconsistent
date_observed: YYYY-MM-DD
template: <path to template, or null if standalone>
surface_mode: greige | cream | photographic | hybrid
voice_register: A | B | mixed
slides: <number>          # carousels only
related:
  - <path to related doc>
legacy_form:              # optional — only if the asset uses a deprecated rule
  field: <what>
  was: <how it was>
  reason: <pointer to ADR>
---
```

### Required sections

- `## Caption` — verbatim quote of the published copy. Preserve original even if it uses deprecated forms (flag in `legacy_form` instead of editing).
- `## Image notes` or `## Slide transcript` — what's actually in the asset.
- `## What this post established for the system` — the rules and patterns this asset originated or confirmed.
- `## Open questions raised` — anything you couldn't resolve from the asset alone.

## Adding a new template

Templates describe **reusable layout patterns**, not specific assets. Add a template only after at least one reference proves the pattern works.

Filename: `templates/<descriptive-slug>.md` (no numbering — templates are equal siblings).

Required frontmatter:

```yaml
---
type: template
subtype: instagram-slide | instagram-carousel | instagram-single
status: confirmed | provisional
surface_mode: greige | cream | photographic | hybrid
voice_register: A | B | mixed
established_by: <path to the reference that established this pattern>
canvas: 1080x1350
aspect_ratio: 4:5
slides_canonical: <number>     # carousels only
arc: <named arc>               # carousels only — see GLOSSARY.md
related:
  - <path>
---
```

Required sections:

- `## When to use` — the criteria for picking this template over alternatives.
- `## Canvas` and zone diagrams (ASCII for now; SVG planned).
- `## Provisional / open` — what still needs confirmation.

## Modifying tokens

Tokens are split across four files in `tokens/`:

| File | What goes here |
|---|---|
| `core.json` | Raw primitives — color hex, font sizes, space units. No semantic meaning. |
| `semantic.json` | Aliases that give meaning — surface modes, text roles, wordmark anatomy. References core. |
| `components.json` | Per-component tokens — cta-pill, wordmark-block, bullet-list. References semantic. |
| `templates.json` | Per-template layouts — Instagram canvases, zones, slide structures. References semantic and components. |

**Rule:** never add a raw value to a higher layer. If you need a new color, add it to `core.json` first, then alias it in `semantic.json`, then reference it from components or templates.

## Making a brand-level decision

If you need to change a foundational rule (canonical name, color palette, typography choice, voice register), write an **ADR** in `CHANGELOG.md`. ADRs are append-only and document:

- Context (what was open)
- Decision (what was chosen)
- Consequences (what changes in the system)
- Reasoning (why)

Do not silently change a rule — write the ADR, update affected files, and cross-link from each affected file back to the ADR.

## Cross-references

Reference other system files using their relative path from the repo root, e.g. ``See `brand/02-typography.md` `` or ``See `CHANGELOG.md` ADR-0001``. When a file is renamed or moved, update every cross-reference in a single pass.

## Status conventions

- 🟢 **confirmed** — verified against source files or stakeholder.
- 🟡 **provisional** — derived from observation, needs source confirmation.
- 🔴 **inconsistent** — the system contradicts itself. Block production work until resolved.

Add new provisional / inconsistent items to `STATUS.md` so they're visible from the index.

## What not to do

- Don't add tokens that duplicate existing primitives.
- Don't introduce new typefaces or colors without an ADR.
- Don't edit the published caption inside a reference file — it's a historical record. Flag deviations via `legacy_form` instead.
- Don't create a new template from a single observed asset — wait for the pattern to recur, or document the asset as a reference and mark the template as `status: provisional`.
- Don't write documentation that describes what the code does — describe **why** the rule exists. The how is in the asset.
