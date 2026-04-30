# Changelog

System-level decisions for the Clínica Serrano design system. Each entry is an Architecture Decision Record (ADR): the question that was open, the decision taken, and the reasoning preserved so future changes can be evaluated against the original intent.

Format: ADRs are append-only. If a decision is later reversed, add a new ADR that supersedes the old one rather than editing history.

---

## ADR-0001 — Canonical brand name: `Clínica Serrano`

**Date:** 2026-04-30
**Status:** Accepted
**Supersedes:** —

### Context

Across the observed Instagram corpus, the brand name appeared in two orderings:

- `Clínica Serrano` — the natural Portuguese clinic-naming construction (noun + qualifier), and how patients refer to the clinic conversationally.
- `Serrano Clínica` — a rhetorical inversion observed mid-sentence in three captions (philosophy post, exame médico desportivo carousel, materiais & memorabilia carousel).

The wordmark itself reads `SERRANO CLÍNICA` because the Didone serif puts visual weight on the surname while the sans qualifier reads as a quiet descriptor. This is typographic emphasis, not naming order.

The system needed a canonical form to use in headers, meta tags, schema.org markup, the future website domain, legal copy, and first-mention in any caption.

### Decision

**`Clínica Serrano` is the canonical brand name.** The inversion `Serrano Clínica` is deprecated.

### Consequences

- All future copy uses `Clínica Serrano` regardless of sentence position.
- Existing captions that used the inversion are flagged as legacy artifacts in their reference files; they should be rewritten on next refresh but the historical records are preserved.
- The wordmark stays as `SERRANO CLÍNICA` — a logo is not a sentence.
- `voice/tone.md` documents the rule explicitly under "Canonical brand name."

### Reasoning

1. Portuguese clinic naming follows noun + qualifier (`Clínica Lemos`, `Hospital de São João`, `Clínica da Luz`). `Clínica Serrano` matches this convention; `Serrano Clínica` does not.
2. Patients and referrers say *"vou à Clínica Serrano,"* never the reverse. The canonical form should match real-world usage.
3. The wordmark's visual order is an aesthetic decision (emphasis on the surname); the spoken/written name is a separate thing and must be explicit.
4. `Serrano Clínica` works rhetorically *because* it inverts the natural order — that's a stylistic device available to copywriters in specific moments, but not the brand's name.

---

## ADR-0002 — Single display sans family

**Date:** 2026-04-30
**Status:** Accepted
**Supersedes:** —

### Context

The cream-mode "ÉPOCA DA GRIPE" cover slide appeared to use a cleaner geometric grotesque (Söhne / Inter / Aktiv-Grotesk family) rather than the warmer rounded display sans seen everywhere else in the corpus. Body type on the same carousel hovered between the two impressions.

The open question was whether the brand:

1. Intentionally used **two sans families** — rounded for atmospheric content, grotesque for announcements — and the system should add a `font.family.grotesque` token, or
2. Used **one family** and the cover's grotesque appearance was an artifact of all-caps + cream-on-charcoal + tighter tracking.

### Decision

**The brand uses one display sans family across all contexts.** The grotesque appearance on cream-mode covers is treated as an optical effect of rendering (all-caps, high contrast, tighter tracking), not a second family.

### Consequences

- `tokens/tokens.json` does not gain a `font.family.grotesque` slot.
- `brand/02-typography.md` closes the "second sans" question and documents the rounded display sans as the single family for all contexts.
- `templates/instagram-announcement-carousel.md` removes the conditional ("set in a clean grotesque if the brand confirms…") and instructs the standard family with the all-caps + cream treatment.
- `references/carousels/2026-04-30-gripe.md` records the optical-effect explanation.
- Future designers commissioning announcement assets do not need to license a second typeface.

### Reasoning

1. The brand's typographic identity *is* the rounded humanist sans. Replacing it on announcements would dilute identity at the moment the brand most wants to be recognized.
2. The surface mode (greige vs cream) already does the contrast/intent signalling. Typography reinforcing that signal is redundant and risks losing brand voice.
3. Two sans families means more licensing cost, more designer onboarding, and more ways for the system to drift.
4. All-caps + cream-on-charcoal + tighter tracking *can* and *does* make a rounded humanist sans optically read more grotesque. The same family at lowercase / on greige / with looser tracking reads warmer and rounder.
5. **Reversibility:** if the original designer ever produces evidence that two families were licensed deliberately (with a clear rule for when each applies), this ADR can be superseded. The burden of proof is on confirming, not on assuming.

---

## ADR-0003 — Register B uses `você`-imperative; `tu` is retired

**Date:** 2026-04-30
**Status:** Accepted
**Supersedes:** —

### Context

The brand's lifestyle/fitness register (Register B) appeared in two grammatical forms across observed captions:

- **`tu` form** (informal, peer-to-peer) — gym-space post: *"…onde tens a privacidade necessária para te focares a 100% na tua recuperação ou performance."*
- **`você`-imperative** (formal-but-direct) — treino personalizado CTA: *"Comece hoje mesmo e dê ao seu corpo o cuidado que ele merece. Marque já a sua avaliação!"*

`voice/tone.md` flagged the drift as inconsistency. The system needed one form so that future copywriters do not re-introduce the split.

### Decision

**Register B uses `você`-imperative across all feed posts.** The `tu` form is retired from the brand's voice.

### Consequences

- `voice/tone.md` rewrites the Register B section to document `você`-imperative as the canonical form and explicitly disallows `tu`.
- The treino personalizado CTA caption becomes the canonical Register B model.
- The gym-space post's caption is flagged as a legacy artifact; it should be rewritten on next refresh as: *"Criámos um espaço de treino, onde tem a privacidade necessária para se focar a 100% na sua recuperação ou performance."*
- Stories and Reels — if/when the brand uses them — may run a separate, looser register since they are ephemeral; feed posts never.

### Reasoning

1. The brand's overall voice is **calm, restrained, clinical**. Register A is third-person impersonal. The two registers should sit on a spectrum, not jump scales — and `tu` is a much bigger jump from Register A than `você`-imperative is.
2. A medical clinic addressing health/training services has authority context. `você`-imperative respects that asymmetry without being cold; `tu` collapses the patient–practitioner distance in a way the rest of the brand voice never does.
3. `tu` in PT-PT is region-sensitive (Norte vs Sul). Matosinhos (Norte) accepts it more readily, but the audience for a private clinic skews wider. `você`-imperative is neutral across the country.
4. The `você`-imperative caption holds together cleanly across **multiple sentences**. The `tu` caption is one sentence — it has never been tested in longer form. Forms that read fine in one sentence often unravel at three.
5. Consistency is more valuable than the marginal warmth of `tu`. A brand drifts looser when registers mix.

---

## How to add a new ADR

1. Pick the next ADR number (sequential, never reused).
2. Use the heading format: `## ADR-NNNN — Short title`.
3. Required sections: Date, Status (Accepted / Superseded by ADR-XXXX), Supersedes, Context, Decision, Consequences, Reasoning.
4. ADRs are **append-only**. If a decision is reversed, write a new ADR that supersedes the old one and update the old one's `Status` field — do not delete or rewrite the original.
5. Cross-link from any file the ADR affects (e.g. `See CHANGELOG.md ADR-0001`).
