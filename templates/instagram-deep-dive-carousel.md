---
type: template
subtype: instagram-carousel
status: confirmed
surface_mode: hybrid
voice_register: A
established_by: references/carousels/2026-04-30-exame-medico-desportivo.md
canvas: 1080x1350
aspect_ratio: 4:5
slides_canonical: 3
arc: hook-stake-trust
related:
  - brand/02-typography.md
  - brand/03-logo.md
  - brand/05-photography.md
  - templates/instagram-multi-service-slide.md
---

# Template — Service Deep-Dive Carousel

A carousel focused on **a single service**, structured to motivate booking. Combines a photo-led hero cover with greige-mode body slides.

Established by the 3-slide "Início de época desportiva?" carousel (Exame Médico Desportivo) of 2026-04-30.

## When to use

- Highlighting one specific service in depth (vs. the multi-service overview format).
- Tying a service to a season or moment ("início de época desportiva", "regresso às aulas", etc.).
- When there's a natural narrative arc: hook → why it matters → what we deliver.

## Three-slide structure

| Slide | Surface | Function |
|---|---|---|
| 1 — Hero cover | Photography + text overlay | Hook the reader with motion + a question |
| 2 — Why it matters | Greige + cream type | Establish the stakes / value of the service |
| 3 — What we deliver | Greige + cream type | The clinic's commitment / methodology |

## Slide 1 — Hero cover (photography + overlay)

The only slide in the system observed so far that places **typography directly on a photograph**.

### Photography rules for this slide

- **Action / motion / atmospheric** subjects only. Running legs, hands at work, an athlete moving, an instrument in use. **Never** a portrait or candid clinical scene.
- **Motion blur is welcome** — it both motivates the topic (movement = sport) and creates a soft surface for type to live on.
- **Warm grade** — same as the rest of the photographic system (see `photography.md`). The photo must feel like it belongs in this brand, not a stock injection.
- **Dimmed/muted color** so that white text reads cleanly on top. If the photo is too bright, it competes with the type.

### Layout

```
┌───────────────────────────────────┐
│  HEADLINE QUESTION                │  ← top-left, large, in cream/white
│  HEADLINE QUESTION                │
│  Subhead explaining the topic.    │  ← directly under, smaller
│  Subhead second line.             │
│                                   │
│                                   │
│         [photograph fills         │
│          full bleed below]        │
│                                   │
│                                   │
│  [WORDMARK]              [→ CTA] │  ← wordmark bottom-left, pill bottom-right
└───────────────────────────────────┘
```

- **Headline**: posed as a **question** ("Início de época desportiva?"). The question primes the reader to swipe for the answer.
- **Subhead**: directly under the headline, names the service in plain language ("O Exame Médico Desportivo é obrigatório para atletas federados.").
- **Wordmark**: bottom-left, in cream. Smaller than usual.
- **CTA pill**: bottom-right, swipe-arrow.

## Slides 2–N — Body slides (greige mode)

Standard greige + cream-type slides. See `instagram-multi-service-slide.md` for layout fundamentals; the differences here are:

- **Wordmark sits bottom-left** (not top-right), to keep the CTA arrow alone in the bottom-right.
- **Bold inline emphasis** is used on key terms (`Esta **avaliação** é essencial...`, `Na **Clínica Serrano**, ...de forma **completa e rigorosa**...`).
- Body copy is **left-aligned and large** — closer to a headline scale than the service-intro body. Each slide carries one statement that fills the upper-left quadrant.

```
┌───────────────────────────────────┐
│                                   │
│  Statement that fills             │  ← top-left, large, left-aligned
│  the upper-left in regular        │
│  weight with **bold** emphasis    │
│  on key terms.                    │
│                                   │
│                                   │
│                                   │
│                                   │
│  [WORDMARK]              [→ CTA] │
└───────────────────────────────────┘
```

## Pacing across the carousel

The 3-slide observed structure works like a small persuasive arc:

1. **Hook** (cover): ask a question that the target reader (federated athlete) can't ignore.
2. **Stake** (slide 2): establish that the service is *essential* — not a recommendation.
3. **Trust** (slide 3): explain that *we* do it rigorously, with the brand name bolded.

Future deep-dives can follow this arc with different beats (e.g. hook → testimony → how it works → outcome). The constant is: **the cover hooks, the body builds, the closing reassures.**

## Caption (off-slide)

The caption observed for the desportivo carousel uses Register A but pivots to a soft Register-B imperative at the end:

> *Início da época desportiva?*
> *O exame médico desportivo é um passo obrigatório para ser um atleta federado.*
> *Na Clínica Serrano, garantimos uma avaliação rigorosa e completa, para que entre em campo com a máxima segurança.*
>
> *Não deixe para a última hora. Garanta que está apto para o seu próximo desafio!*
>
> *📅 Agende o seu exame por mensagem direta.*

> Note: the original observed carousel used the now-deprecated `Serrano Clínica` inversion (see `references/carousels/2026-04-30-exame-medico-desportivo.md`). The example above shows the corrected canonical form. See `CHANGELOG.md` ADR-0001.

Pattern:

1. Repeat the cover question.
2. State the stake.
3. State the clinic's commitment.
4. (Soft urgency) Don't delay.
5. (Concrete CTA) Direct booking instruction.

The 📅 emoji at the start of the booking line is **the first emoji observed in the brand** anywhere in this system. Worth confirming whether emojis are now in scope, or whether this was a one-off.

## Provisional / open

- Whether deep-dive carousels can run beyond 3 slides.
- Whether the cover photo always has motion/blur or whether other action treatments are allowed.
- The 📅 emoji — one-off or new pattern?
