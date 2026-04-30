---
type: template
subtype: instagram-slide
status: confirmed
surface_mode: greige
voice_register: A
established_by: references/carousels/2026-04-30-services.md
canvas: 1080x1350
aspect_ratio: 4:5
related:
  - brand/00-foundations.md
  - brand/01-colors.md
  - brand/02-typography.md
  - brand/03-logo.md
  - tokens/templates.json
---

# Template — Multi-Service Overview Slide

The slide pattern used **only** for multi-service overview carousels — the format where each slide names a different specialty. Established by the 8-slide services carousel of 2026-04-30.

Other carousel formats have their own templates:
- `instagram-announcement-carousel.md` — cream-mode time-sensitive carousels.
- `instagram-deep-dive-carousel.md` — single-service deep-dive with photo cover.

## Canvas

- **Aspect ratio**: 4:5 (Instagram portrait carousel).
- **Working size**: 1080 × 1350 px.
- **Safe area**: stay within ~80 px of every edge.

## Zones

Reading the canvas top-to-bottom, the slide has four fixed zones:

```
┌───────────────────────────────────┐
│                       [WORDMARK] │  ← Zone 1: top-right wordmark
│                                   │
│                                   │
│                                   │
│  HEADLINE                         │  ← Zone 2: large left-aligned headline
│  HEADLINE                         │     (1–3 lines, breaks naturally)
│                                   │
│                  Description body │  ← Zone 3: right-aligned body
│                  description body │     directly under headline,
│                  description body │     ~50% canvas width
│                                   │
│                                   │
│                       [→ CTA  ]  │  ← Zone 4: bottom-right arrow pill
└───────────────────────────────────┘
```

## Zone specs

### Zone 1 — Wordmark

- Position: top-right.
- Distance from top edge ≈ distance from right edge ≈ ~6% of canvas width.
- Color: `--color-ink`.
- Size: small (see `brand/03-logo.md` for size relation rule).

### Zone 2 — Headline

- Position: left-aligned, sitting roughly at the **vertical optical center** of the canvas, breaking slightly above center on shorter titles.
- Left margin: ~6–8% of canvas width.
- Right edge: free — let the headline wrap when it reaches the body column.
- Type: display sans, see `brand/02-typography.md`.
- Color: `--color-ink`.
- Wrapping: natural word boundaries, no forced breaks, no hyphenation. 2- and 3-line titles are normal.
- Casing: sentence case.

### Zone 3 — Body description

- Position: directly below the headline, separated by a generous gap (~one headline line-height).
- **Right-aligned**, anchored to the right edge of the safe area.
- Column width: ~50% of canvas width.
- Type: same family as headline, much smaller, regular weight.
- Length budget: 2–4 lines. Anything longer means the copy needs cutting, not the type shrinking.

### Zone 4 — CTA pill

- Position: bottom-right corner of the safe area.
- Shape: outlined pill (rounded rectangle), 1px stroke in `--color-ink`.
- Content: a right-pointing arrow (`→`), centered, no text label.
- Width: ~14% of canvas width. Height ≈ 30% of width.
- Function: signals "swipe to next slide." Present on every slide of a multi-slide carousel, including the last (observed across all 8).

## Variations observed

Across the 8 slides, only two things vary:
- The headline text and its line-count.
- The body description text.

Everything else — wordmark position, body alignment, CTA pill, paper texture — is identical. **This consistency is the system.** Future slides should not introduce new layout variations without a deliberate reason.

## When to break the template

The template is a **service-introduction slide** specifically. Other carousel intents — testimonial, team intro, before/after, opening-hours — will need their own templates derived from these foundations. Don't force unrelated content into this layout.

## Provisional

This template was derived from a single carousel. If subsequent carousels show variation (e.g. cover slide vs. detail slides, or different CTA copy), update this file and note the variation history at the bottom.
