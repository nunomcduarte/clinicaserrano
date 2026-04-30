# Color

The palette is intentionally tiny. Two **surface modes** (greige + cream/light) each have a foreground and a background; one **auxiliary** color appears on physical merchandise. No bright accents, no category palettes.

## Tokens

### Greige mode (default — premium, atmospheric, service intros)

| Token | Approx. value | Role | Notes |
|---|---|---|---|
| `--color-paper` | `#B0A695` (warm greige) | Background, full-bleed | Always overlaid with paper grain texture; the visible color shifts ±5% depending on grain density |
| `--color-ink` | `#F2EBDD` (warm off-white / cream) | Headlines, body, logo, UI strokes | Never pure white — there's a perceptible warmth |

### Cream mode (announcements, urgency, alerts)

| Token | Approx. value | Role | Notes |
|---|---|---|---|
| `--color-cream-bg` | `#E8E2D4` (provisional) | Background | Cream/off-white. Subtler grain than the greige variant — almost a flat fill but with a faint paper texture. |
| `--color-charcoal` | `#1A1A1A` (provisional, near-black) | Headlines, body, logo, UI strokes | Reads as black on the cream surface but has slight warmth. Not pure `#000`. |

The two modes are not mixed within a single carousel. Pick one per piece of content based on intent (atmosphere → greige; attention → cream).

### Auxiliary (textiles only)

| Token | Approx. value | Role | Notes |
|---|---|---|---|
| `--color-navy` | `#1F2435` (deep navy, provisional) | Textile applications | Observed on rolled hand towels with cream wordmark embroidery. Not used on digital surfaces in any post observed so far. |

⚠️ **Hex values are estimates from screenshots.** Before locking these into `tokens.json`, sample directly from a source file (Figma, original PSD/AI) or from the highest-resolution Instagram export. The greige in particular is sensitive to JPEG compression and Instagram's color profile.

## Contrast

`#F2EBDD` on `#B0A695` lands around **3.4:1 contrast** — below WCAG AA for body text at small sizes. The brand is choosing aesthetic softness over accessibility-grade contrast. This is fine for marketing surfaces but is a constraint to flag for:

- Anything that needs to be legible at small sizes (footnotes, prices, legal).
- The future website, where AA compliance matters more than on Instagram.

For those cases, either:
- Use the ink color at larger sizes only, or
- Introduce a darker secondary ink (e.g. `#3A332A`) for body copy on web.

## What's missing (to confirm)

- Is there a darker variant — for example, an ink-toned background for premium/quiet posts?
- Is there a true white surface (e.g. for documents, letterhead, the website's content areas)?
- Is the navy promoted to a digital brand color, or kept for textiles only?
- Are there any accent tones reserved for specific contexts (warning, success, category tags)?

These should be answered as more posts and surfaces come in.
