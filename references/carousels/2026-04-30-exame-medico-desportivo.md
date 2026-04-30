---
type: reference
subtype: carousel
status: confirmed
date_observed: 2026-04-30
template: templates/instagram-deep-dive-carousel.md
surface_mode: hybrid
voice_register: A
slides: 3
related:
  - brand/05-photography.md
  - brand/02-typography.md
  - CHANGELOG.md
---

# Reference — Carousel: Exame Médico Desportivo

**Format:** 3-slide Instagram carousel, 4:5 portrait
**Function:** Service deep-dive — the federated-athlete medical exam, tied to the start of the sports season
**Template established:** `templates/instagram-deep-dive-carousel.md`

## Caption

> *Início da época desportiva?*
> *O exame médico desportivo é um passo obrigatório para ser um atleta federado.*
> *Na Serrano Clínica, garantimos uma avaliação rigorosa e completa, para que entre em campo com a máxima segurança.*
>
> *Não deixe para a última hora. Garanta que está apto para o seu próximo desafio!*
>
> *📅 Agende o seu exame por mensagem direta.*

## Slide transcript

### Slide 1 — Hero cover (photography + text overlay)

- **Background photograph:** running legs in motion blur, white socks and shoes, on a wood floor. Cropped tight; the runner's identity is anonymous (legs only).
- **Headline (top-left, cream/white):** **Início de época desportiva?**
- **Subhead (directly under headline):** *O Exame Médico Desportivo é obrigatório para atletas federados.*
- **Wordmark:** bottom-left, cream.
- **CTA pill:** bottom-right, swipe-arrow.

This is the **first observed slide in the system that places type directly on a photograph.** The treatment works because the photo is action/motion, not portrait — and the headline is posed as a question that motivates swiping.

### Slide 2 — Stake

- Greige-mode body slide.
- Top-left, large left-aligned headline: *Esta **avaliação** é essencial para garantir que está apto para a prática desportiva.*
- Bold inline on `avaliação`.
- Wordmark: bottom-left.
- CTA pill: bottom-right.

### Slide 3 — Trust

- Greige-mode body slide.
- Mid-right, large body statement: *Na **Serrano Clínica**, realizamos este processo de forma **completa e rigorosa**, seguindo todos os critérios exigidos.*
- Bold inline on `Serrano Clínica` and `completa e rigorosa`.
- Wordmark: bottom-left.
- CTA pill: bottom-right.

## What this carousel established for the system

- **The deep-dive carousel template** with hook → stake → trust as a 3-slide arc.
- **Photography-with-text-overlay as a permitted hybrid surface** — only on action/atmospheric/motion-blur shots, never on portraits.
- **Bold inline emphasis as the standard typographic device** for highlighting key terms in body copy.
- **Wordmark bottom-left + CTA pill bottom-right** as the layout when both must coexist on the same slide.
- **Question-headline cover** as a swipe-driver: framing the first slide as a question primes the reader to look for the answer.
- **The 📅 emoji** appears in the booking line of the caption — first emoji observed in the system. Worth confirming whether this is now sanctioned or a one-off.

## Notable patterns

- **The carousel arc is deliberately persuasive.** This is the most overtly conversion-oriented carousel observed so far — it's an ad in the brand's voice. The quietness of the body slides keeps it from feeling salesy, but the structure (hook → urgency → reassurance) is unmistakable.
- **The caption mirrors the slides.** Question → stake → trust → urgency → CTA — same arc, in copy form. The slide structure and the caption structure are aligned. Future deep-dives should preserve this alignment.
- **The brand name** appears bolded in slide 3 — first observed use of bolding the brand name mid-sentence. A worthwhile small-print device for trust building. (The slide and caption used the now-deprecated inversion `Serrano Clínica`; future versions must use `Clínica Serrano` per `CHANGELOG.md` ADR-0001.)

## Open questions raised

- The 📅 emoji — sanctioned, or an outlier?
- "Início de época desportiva" — is this carousel timed to a specific federation season-start moment (typically September in PT)? If so, it should be re-runnable annually with minimal editing.
- Whether the system permits **other types of action photography** as cover hero (training scenes, treatment-in-progress, tools-in-use) or whether it stays narrowly with running/movement.
