---
type: template
subtype: instagram-carousel
status: confirmed
surface_mode: cream
voice_register: A
established_by: references/carousels/2026-04-30-gripe.md
canvas: 1080x1350
aspect_ratio: 4:5
slides_canonical: 3
arc: cover-body-closing
related:
  - brand/01-colors.md
  - brand/02-typography.md
  - brand/03-logo.md
  - CHANGELOG.md
---

# Template — Announcement Carousel (cream mode)

The cream-bg / charcoal-type variant. Used for **time-sensitive** or **directional** content: seasonal announcements (flu season), urgent service availability, schedule changes, calls to act now.

Established by the 3-slide "ÉPOCA DA GRIPE" carousel of 2026-04-30.

## When to use

- A timely, time-bound message (flu season, holiday schedule, urgent availability).
- A direct call to act ("we're here, schedule now").
- Anything that benefits from high-contrast, attention-getting typography without bright colors.

**Don't use** for service intros, atmospheric content, or team posts. Stay in greige mode for those.

## Surface

- Background: `--color-cream-bg` (`~#E8E2D4`), full-bleed, subtle paper grain.
- Type color: `--color-charcoal` (`~#1A1A1A`), near-black.
- The contrast is much higher than greige mode — the carousel reads as **directional / important**.

## Three-slide structure

| Slide | Function | Type weight | Notes |
|---|---|---|---|
| 1 — Cover | Topic + scope | Headline + subhead | Headline names the season/topic; subhead names the service relevance. CTA pill at bottom names the offerings. |
| 2 — Body | The reasoning | Body + bullet list | Explains why it matters, lists what's available. Bold inline for service names. |
| 3 — Closing | Call to action | Headline + body | Final urgent line + booking instruction. |

## Slide specs

### Slide 1 — Cover

```
┌───────────────────────────────────┐
│           [WORDMARK]              │  ← top-center
│                                   │
│                                   │
│        HEADLINE                   │  ← centered, sentence-case
│        HEADLINE                   │
│                                   │
│        Subhead two lines          │  ← centered, smaller
│        in regular weight          │
│                                   │
│                                   │
│   [ Service A | Service B ]      │  ← centered pill, low position
└───────────────────────────────────┘
```

- **Wordmark**: top-center, charcoal.
- **Headline**: large, all-caps, centered. Two-line treatment with first line shorter than second is acceptable. Set in the brand's single display sans family — the all-caps + cream-on-charcoal + tighter tracking treatment is what gives the cover its cleaner grotesque feel. (See `CHANGELOG.md` ADR-0002.)
- **Subhead**: directly under headline, smaller, regular weight, all-caps, centered.
- **CTA pill**: outlined pill at bottom-center with two service labels separated by a `|`. Wider than the regular swipe-arrow pill.

### Slide 2 — Body

```
┌───────────────────────────────────┐
│                                   │
│              Setup line one       │  ← right-aligned, top-right
│              Setup line two       │
│              Setup line three     │
│                                   │
│                                   │
│  Reinforcement line with **bold** │  ← left-aligned, mid-low
│  service names, garantindo:       │
│                                   │
│  • Bullet one                     │
│  • Bullet two                     │
│  • Bullet three                   │
│                                   │
│                                   │
│           [WORDMARK]              │  ← bottom-center
└───────────────────────────────────┘
```

- **Wordmark**: bottom-center.
- **Setup paragraph**: top, right-aligned. States the context.
- **Reinforcement paragraph**: middle/lower, left-aligned. Restates the offer with bold inline on service names.
- **Bullet list**: under the reinforcement paragraph, plain `•` bullets, left-aligned, regular weight. 3 items is the observed length — keep it tight.

### Slide 3 — Closing

```
┌───────────────────────────────────┐
│                                   │
│  HEADLINE TWO LINES              │  ← top-left, large, sentence-case
│  HEADLINE TWO LINES              │
│                                   │
│                                   │
│           Sub-statement,          │  ← right-aligned, mid-low
│       smaller and quiet.          │
│                                   │
│                                   │
│           [WORDMARK]              │  ← bottom-center
└───────────────────────────────────┘
```

- **Wordmark**: bottom-center.
- **Headline**: top-left, large, sentence-case. The emotional hook (`A sua saúde não espera, nós também não.`).
- **Sub-statement**: mid-low, right-aligned, smaller. The instruction to act (`Agende a sua consulta connosco, estamos prontos para o ajudar.`)
- No CTA pill on this slide — the closing copy *is* the CTA.

## Voice notes

- Register A (formal third person), but allowed slightly more direct than service intros.
- Bold inline emphasis on **service names** is the key typographic device.
- One direct closing imperative, no exclamation in this carousel (compare with the dumbbell-CTA post, which does use one). Confirm whether the brand wants exclamation reserved for register-B / fitness content.

## Provisional / open

- Whether the cream surface uses a subtler texture or no texture at all. Visible grain is much fainter than the greige variant.
- Whether 3 slides is the canonical length, or whether announcement carousels can run longer.
