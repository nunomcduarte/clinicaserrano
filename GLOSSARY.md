# Glossary

Canonical terms used across the Clínica Serrano design system. New contributors should read this before going deeper.

---

## Surface modes

The system has three surface modes. Every asset declares which mode it lives in.

### Greige mode
Default. Premium, atmospheric, service-introduction content. Warm greige paper background with cream foreground type. Full-bleed paper texture. See `brand/01-colors.md` and `brand/04-texture.md`.

### Cream mode
Time-sensitive, urgent, directional content. Cream/off-white background with charcoal foreground type. Subtler grain than greige. The brand's way of signalling **attention** without resorting to bright colors. See `brand/01-colors.md` and `templates/instagram-announcement-carousel.md`.

### Photographic mode
The third surface. Warm, low-key, available-light photography — never clinical-stock. Type is generally **not** overlaid on photographic surfaces, with one exception (see Hybrid surface). See `brand/05-photography.md`.

### Hybrid surface
A photograph fills the canvas with a headline overlaid. Permitted only on **action / motion / atmospheric** photography — never on portraits or candid clinical scenes. Established by the deep-dive carousel template. See `templates/instagram-deep-dive-carousel.md`.

---

## Voice registers

### Register A
The default voice. Formal, third-person, impersonal. Used for clinical services, philosophy, team credentials, and "about us" content. No exclamation marks. Sentences favor noun-led openings. See `voice/tone.md`.

### Register B
The motivational voice. Used sparingly for gym, training, performance, and direct-CTA posts. Uses **`você`-imperative** form (`comece`, `dê`, `marque`). Allows one exclamation per post on the final imperative.

The **`tu` form is retired** from the brand's voice (see `CHANGELOG.md` ADR-0003). Earlier captions that used `tu` are legacy artifacts.

---

## Carousel arcs

The brand uses three named arcs for multi-slide carousels:

### Multi-service overview
Every slide is the same template (one service per slide). No cover, no closing. Established by the 8-slide services carousel. See `templates/instagram-multi-service-slide.md`.

### Cover-body-closing arc
Three distinct layouts in sequence: cover (topic + scope), body (reasoning + bullets), closing (CTA). Used for announcement carousels. See `templates/instagram-announcement-carousel.md`.

### Hook-stake-trust arc
A persuasive 3-slide arc: hero photo with question (hook) → why-it-matters statement (stake) → clinic's commitment (trust). Used for deep-dive carousels. See `templates/instagram-deep-dive-carousel.md`.

---

## Components

### Wordmark
The two-part `SERRANO CLÍNICA` mark on a single baseline. Didone serif paired with light all-caps sans. The mark is the pair — neither word is used alone. Stacked variant exists only on physical textiles. See `brand/03-logo.md`.

### CTA pill
Outlined pill button. Two variants:

- **Swipe-arrow** — bottom-right of multi-slide carousels, contains a `→` glyph, signals "swipe."
- **Tap-target** — wider variant on cover slides, contains two service labels separated by `|`.

### Bullet list
Plain `•` markers, max three items, used in announcement body slides. Tight by design.

### Headline block
The combined headline + body copy unit on typographic slides. Headline left-aligned, body right-aligned at ~50% column width, separated by ~one line-height of headline.

---

## Inline emphasis

The brand has no italic register. **Bold** is the only inline emphasis device.

Rules: 1–3 bold spans per slide; whole words only; the brand name when mid-sentence; service names on first introduction; outcomes/commitments. Never on filler verbs, prepositions, or full sentences. See `brand/02-typography.md`.

---

## Status flags

Used in file frontmatter and in-line:

- **🟢 confirmed** — verified against source files or stakeholder.
- **🟡 provisional** — derived from observation, needs source confirmation.
- **🔴 inconsistent** — the system contradicts itself; resolve before next asset. (As of `STATUS.md`, all 🔴 items have been resolved.)

The `legacy_form` field in frontmatter records cases where a published asset used a now-deprecated rule (e.g. the `tu` form in the gym-space caption). The asset is preserved verbatim as historical record; the deprecation is logged.

---

## Names

### Canonical brand name
**Clínica Serrano.** Used in every caption, paragraph, and sentence position. The inversion `Serrano Clínica` is deprecated (see `CHANGELOG.md` ADR-0001).

### Wordmark
Always rendered as `SERRANO CLÍNICA` — the typographic emphasis on the surname is a logo-level design choice. The logo is not a sentence.

### Utente
PT-PT term for "user / patient / client" in healthcare. Brand prefers this over `paciente` or `cliente`.
