# Status

Live dashboard of confirmed, provisional, and resolved items in the design system. This is curated by hand for now; will be auto-generated from frontmatter once tooling is in place.

Last updated: 2026-04-30

---

## 🔴 Inconsistencies (0)

No active contradictions. All previously flagged 🔴 items are resolved — see Resolved section below.

---

## 🟡 Provisional (12)

These are observation-derived and need confirmation against source files or stakeholder.

### Color & texture
- **Greige hex** (`#B0A695`) — sampled from Instagram exports. Sample from original Figma/PSD before locking. → `tokens/core.json`, `brand/01-colors.md:11`
- **Cream hex** (`#E8E2D4`) — same caveat. → `tokens/core.json`, `brand/01-colors.md:18`
- **Charcoal hex** (`#1A1A1A`) — same caveat. → `tokens/core.json`, `brand/01-colors.md:19`
- **Navy hex** (`#1F2435`) — same caveat. → `tokens/core.json`, `brand/01-colors.md:27`
- **Paper texture asset** — single scan vs. eight unique scans? Once confirmed, check into `brand/assets/paper-texture-greige.png`. → `brand/04-texture.md:42`
- **Cream surface texture** — confirm whether grain is subtler or absent on cream mode. → `templates/instagram-announcement-carousel.md`

### Typography
- **Wordmark serif identification** — likely Bodoni Moda / GT Super / Canela / Didot. Confirm with original designer. → `brand/02-typography.md:14-22`, `tokens/core.json`
- **Display sans identification** — likely TWK Lausanne / PP Editorial New / Söhne / Migra. Confirm with original designer. → `brand/02-typography.md:36-42`, `tokens/core.json`

### Logo
- Logomark / symbol variant for tight spaces (favicon, app icon). → `brand/03-logo.md:49`
- Horizontal vs. stacked version for narrow placements (only towel-stacked variant observed so far). → `brand/03-logo.md:50`
- Minimum legible size. → `brand/03-logo.md:51`
- Wordmark position rule (4 positions observed; deliberate system or ad-hoc?). → `brand/03-logo.md`, `brand/00-foundations.md`

---

## ⚪ Open questions (cataloged, not blocking)

Smaller open items that are nice-to-resolve but don't block production work.

- Whether `Dr.` / `Dra.` vs. first-name openers are role-based or stylistic. → `templates/team-portrait-post.md`
- Whether the balanced opening pair (`X por Y, Z por W`) is mandatory in team bios or only for senior figures. → `templates/team-portrait-post.md`
- Hashtag strategy (none observed in current corpus). → `voice/tone.md`
- Tone for replies/DMs (same calm voice or warmer/looser?). → `voice/tone.md`
- 📅 emoji policy — sanctioned, or one-off? → `templates/instagram-deep-dive-carousel.md`, `references/carousels/2026-04-30-exame-medico-desportivo.md`
- Nature of the CR7 / Nike connection — high-priority for marketing scope. → `brand/07-space-storytelling.md`
- Identity of the second senior clinician in the philosophy post. → `references/philosophy/2026-04-30-listening.md`
- Whether the navy is digital-permitted or textile-only. → `brand/01-colors.md`, `brand/06-applications.md`
- Whether photography is ever cropped square (1:1) for grid feed. → `brand/05-photography.md`
- Whether the brand uses Reels and whether the same photographic language carries over. → `brand/05-photography.md`

---

## 🟢 Confirmed (selected highlights)

Foundational rules verified across two or more references:

- Two-mode surface system (greige + cream) — confirmed by services + gripe carousels.
- Single display sans family across all contexts — see ADR-0002.
- Bold inline emphasis pattern — confirmed across services, gripe, and exame-medico-desportivo carousels.
- Hybrid surface (text-on-photo) permitted on action/motion only, never portraits — confirmed by deep-dive carousel.
- Wordmark "one position per carousel" rule — confirmed by services (top-right) and gripe (top-center cover, bottom-center body) carousels each holding their position internally.
- Caption pattern shapes: two-line poetic, bio framing, service CTA, philosophy — all confirmed by at least one reference.
- Canonical brand name `Clínica Serrano` — see ADR-0001.
- Register B uses `você`-imperative — see ADR-0003.

---

## ✅ Resolved (formerly 🔴)

Decisions logged in `CHANGELOG.md`:

- ADR-0001 — Canonical brand name: `Clínica Serrano` (was: ambiguous between `Clínica Serrano` and `Serrano Clínica`).
- ADR-0002 — Single display sans family (was: possible second sans on cream-mode covers).
- ADR-0003 — Register B uses `você`-imperative; `tu` retired (was: drift between `tu` and `você`-imperative inside Register B).

---

## Missing artifacts (planned)

- `templates/service-cta-post.md` — referenced by `references/ctas/2026-04-30-treino-personalizado.md` and `templates/space-photo-post.md`, but not yet written.
- `brand/assets/paper-texture-greige.png` — original scan to be checked in.
- `brand/assets/paper-texture-cream.png` — same.
- `brand/assets/wordmark-cream.svg`, `brand/assets/wordmark-charcoal.svg`, `brand/assets/wordmark-stacked.svg` — vector wordmarks for production use.
- `brand/assets/photography-moodboard.jpg` — 9-image grid showing the canonical photographic look.
- `templates/diagrams/*.svg` — SVG zone maps to replace the ASCII boxes inside template docs.
