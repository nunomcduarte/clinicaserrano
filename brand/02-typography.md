# Typography

Two typefaces, used with discipline:

1. A **modern Didone serif** — only inside the wordmark.
2. A **geometric display sans** — everything else.

## 1. Wordmark serif (display, restricted use)

**Where it appears:** the word `SERRANO` in the logo, top-right of every layout. Nowhere else.

**Style cues:** high-contrast Didone — vertical stress, hairline horizontals, fine bracketed serifs, all-caps. Reads luxury, editorial, fashion-house.

**Likely candidates** (until the original is confirmed):

- Bodoni 72 / Bodoni Moda
- Didot LT Std
- GT Super Display
- Canela Deck
- Recoleta (slightly more humanist alternative)

**Action:** ask the brand owner / original designer to confirm the licensed font. Do not guess in production assets.

## 2. Display sans (everything else)

**Where it appears:**
- Service names and post headlines (very large)
- Body descriptions (medium)
- The `CLÍNICA` portion of the wordmark (small all-caps)

**Style cues:** geometric sans with rounded terminals, double-story `a`, circular `o`, slightly wide proportions. Reads warm, modern, calm — not corporate or technical.

**Likely candidates:**

- TWK Lausanne / Lausanne Pan
- PP Editorial New (sans variant)
- Söhne / Söhne Breit
- Migra Sans
- FH Oscar
- GT Walsheim

**Action:** confirm with the original designer. If this needs an open-source alternative for web, **Inter Display** or **General Sans** are the closest free substitutes; **Manrope** is a budget choice if a rounded humanist feel is acceptable.

### Single sans family — resolved

The cream-mode "ÉPOCA DA GRIPE" cover slide initially appeared to use a cleaner grotesque rather than the warmer rounded display sans used elsewhere. **This is now resolved as an optical effect, not a second family.**

All-caps + cream-on-charcoal + tighter tracking optically transforms the rounded humanist sans into something that reads more grotesque. The same family at lowercase / on greige / with normal tracking reads as warmer and rounder. The brand uses **one display sans family across all contexts** — greige and cream alike, atmospheric and announcement alike.

Rationale:
- Two sans families would dilute the brand's typographic identity at the exact moment (announcements) where attention is most needed.
- The surface mode (greige vs cream) already does the contrast/intent signalling. Typography doesn't need to reinforce it.
- One license, one onboarding, one source of consistency.

See `CHANGELOG.md` ADR-0002 for the full reasoning.

## Type scale (provisional)

Pulled from the Instagram carousel — proportions, not absolute sizes:

| Role | Size relation | Weight | Tracking | Leading | Color |
|---|---|---|---|---|---|
| Display headline (service name) | ~12% of canvas height | Regular / Medium | Tight, near 0 | ~0.95 | `--color-ink` |
| Body description | ~3.5% of canvas height | Regular | Normal | ~1.25 | `--color-ink` |
| Wordmark `SERRANO` | ~2% of canvas height | Regular (serif) | Slight positive | — | `--color-ink` |
| Wordmark `CLÍNICA` | matched to `SERRANO` cap height | Light (sans) | Wider | — | `--color-ink` |

## Inline emphasis (bold)

Bold weight is used **inline** to emphasize key terms within otherwise regular-weight body copy. Observed examples:

> *Esta **avaliação** é essencial para garantir que está apto para a prática desportiva.*

> *Na **Clínica Serrano**, realizamos este processo de forma **completa e rigorosa**, seguindo todos os critérios exigidos.*

> *Por isso, reforçamos que temos disponibilidade para **Consultas Urgentes e ao Domicílio**, garantindo: …*

### Rules for bold

- **One to three** bold spans per slide. Three is already a lot — usually one or two.
- **Whole words or phrases.** Never partial words.
- **The brand name** (`Clínica Serrano`) gets bolded when it appears mid-sentence — a way to anchor the reader.
- **Service names** get bolded the first time they're introduced (e.g. `Consultas Urgentes e ao Domicílio`).
- **Outcomes / benefits / commitments** can be bolded for emphasis (`completa e rigorosa`).
- Don't bold filler verbs, prepositions, or generic adjectives.

### What bold is *not* for

- ❌ Not for full sentences (use hierarchy / size instead).
- ❌ Not for headlines (which are already display-sized; bolding would be redundant).
- ❌ Not for italics-style emphasis (the brand has no italic register; bold is the only inline emphasis).

## Headline rules

Observed across all 8 slides of the services carousel:

- **Always left-aligned**, sitting roughly on the vertical center but breaking slightly above it.
- **Wraps freely** — Serrano does not force titles onto a single line. A 2- or 3-line title is normal and aesthetic.
- **No hyphenation.** Words break only at natural word boundaries.
- **Sentence case**, not title case. ("Consultas ao domicílio", not "Consultas Ao Domicílio".)
- **Portuguese diacritics preserved** without ornament (no swashes, no italic alternates).

## Body rules

- Right-aligned, set in a column ~50% of the canvas width, anchored to the right edge of the safe area.
- Sits directly under the headline, separated by a generous gap (~one line of headline).
- Single paragraph, 2–4 lines. If it would run longer, the copy needs to be cut, not the type shrunk.
