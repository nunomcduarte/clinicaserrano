# Voice & Tone

Verbal identity, derived from the carousel intro and the 8 service descriptions.

## Language

**Portuguese (Portugal).** Not Brazilian. Watch for the giveaways:

- `deslocação` (not `deslocamento`)
- `personalizado / personalizada` agreement
- `pré e pós-parto` written with the hyphen
- ç and accents always preserved (`saúde`, `condição`, `ajustadas`)

## Voice attributes

The brand sounds:

- **Calm** — sentences are short to medium. No urgency in clinical/service comms.
- **Warm but clinical** — uses human words like `conforto`, `proximidade`, `bem-estar` but anchors them to clinical actions like `avaliação`, `diagnóstico`, `tratamento`.
- **Promise-led, not procedure-led** — each service is described by what it does *for the patient*, not by which equipment or method is used. Even the laser-therapy service leads with "alívio de desconfortos" before naming the technique.
- **Confident without bragging** — no superlatives ("o melhor", "líderes"), no exclusivity claims, no marketing puff.

## Two registers

The brand operates in two voices, applied by post type:

### Register A — formal, third-person, impersonal (default)

The voice for clinical services, philosophy, the team's professional credentials, and "about us" content.

- Treats the reader at a respectful distance — uses third person or impersonal `se`.
- No exclamation marks.
- Sentences favor noun-led openings.

> *Cuidados médicos contínuos, focados na prevenção, diagnóstico e tratamento de doenças em todas as fases da vida.*

### Register B — `você`-imperative, motivational (lifestyle/fitness)

The voice for the gym, training, performance, and direct-CTA posts. Used sparingly.

- Addresses the reader with the **`você`-imperative form** (`comece`, `dê`, `marque`, `garanta`). Holds the respectful authority of Register A while shifting from third-person observation to direct address.
- Allows **one exclamation per post**, placed on the final imperative.
- Verbs lead more often than nouns.
- The `tu` form (`tens`, `te focares`, `tua`) is **not** in the brand's voice. Earlier captions that used it are legacy artifacts and should be rewritten on next refresh.

> *Comece hoje mesmo e dê ao seu corpo o cuidado que ele merece. Marque já a sua avaliação!*

**Don't mix registers within a single post.** A team member's bio doesn't switch from third-person to direct address halfway through. A gym CTA doesn't pivot to formal third-person at the end.

See `CHANGELOG.md` ADR-0003 for the reasoning behind retiring `tu`.

## Sentence shape

Carousel intro pattern (2 sentences):

> *Cada pessoa é única, e cada cuidado também.*
> *Por isso, reunimos especialidades que se complementam para promover equilíbrio, força e bem-estar.*

The first line states a value. The second line connects that value to what the clinic does. This **value → action** rhythm is worth preserving in future intros.

Service description pattern (1 sentence, 2–4 lines):

> *[Action / care type]* + *[for whom or in what situation]* + *[outcome / benefit].*

Example:

> *Avaliação e acompanhamento* | *de atletas e praticantes de atividade física,* | *com foco na prevenção de lesões, otimização do desempenho e recuperação funcional.*

Other observed structures:

- `Cuidados médicos contínuos, focados na X, Y e Z.`
- `Apoio médico personalizado para X, com Y, ajudando Z.`
- `Sessões de exercício físico orientadas por X, ajustadas a Y, para Z.`

The constants are: a noun-led opening, a who/what-for clause, an outcome clause. Aim for that shape on any future service or feature description.

## Vocabulary that fits

Across the 8 slides, the recurring words form the brand's working vocabulary:

| Theme | Words used |
|---|---|
| Care | cuidados, acompanhamento, apoio, orientação |
| Personalization | personalizado, individualizado, ajustado, adaptado |
| Outcome | bem-estar, equilíbrio, força, autonomia, condição, recuperação, prevenção |
| Method | avaliação, diagnóstico, tratamento, sessão, estratégia |
| Setting | domicílio, conforto, proximidade, clínica |

**Use these words.** New copy should pull from this list before reaching for synonyms.

## Vocabulary to avoid

- ❌ "Excelência", "líder", "referência", "premium" — boastful claims.
- ❌ "Soluções", "experiência única", "jornada" — corporate marketing-speak.
- ❌ Anglicisms that have a clean PT equivalent (`coaching` → `acompanhamento`, `wellness` → `bem-estar`, `check-up` → `avaliação`).
- ❌ Emojis. Hashtag-stuffing. Multiple exclamation marks.
- ❌ Fear-based framing ("não corra riscos", "antes que seja tarde").

## Caption structures

Captions follow one of four shapes depending on post intent:

### 1. Two-line poetic (carousels, space photography)

```
[1 line — value or sensory statement]
[1 line — what the clinic does / why it matters]
```

Examples:
> *Cada pessoa é única, e cada cuidado também.*
> *Por isso, reunimos especialidades que se complementam para promover equilíbrio, força e bem-estar.*

> *Ambientes que respiram leveza, profissionais que inspiram confiança.*
> *É neste equilíbrio que o bem-estar acontece.*

### 2. Bio framing (team-member portraits)

A three-beat structure:

```
[Opening line — a short, lyrical "person + something" pairing]
[Credentials paragraph — registry number, qualifications, training, mentors]
[Philosophy paragraph — what they believe / how they practice]
```

Example, Dr. Serrano:
> *Médico por vocação, desportista por paixão.*
>
> *O Dr. António Filipe Serrano (Ordem dos Médicos n° 60829) alia a experiência clínica à vivência prática do desporto, olhando para a saúde como um equilíbrio entre corpo e mente.*
>
> *Especialista em Medicina Geral e Familiar, com pós-graduação em Medicina Desportiva e pós-graduação em Medicina Estética, dedica-se a cuidar com rigor, empatia e presença.*

The opening line is **always a balanced pair** — two roles, two passions, two sides of one person. It sets the human before the credentials. Future bios should preserve this rhythm.

### 3. Service CTA (lifestyle/fitness posts)

Slightly longer, in Register B (informal). Three beats:

```
[What the service is / what makes it different]
[How it's done / who supports the patient]
[Direct call to action, ending with an exclamation]
```

Example:
> *Na nossa clínica, o treino é totalmente personalizado…*
> *…Cada passo é acompanhado por profissionais de saúde, com rigor, para que alcance resultados reais.*
> *Comece hoje mesmo e dê ao seu corpo o cuidado que ele merece. Marque já a sua avaliação!*

### 4. Philosophy (statement posts)

Multi-paragraph, formal, declarative. Used to articulate the clinic's values.

```
[Opening — a single sentence that names the value]
[Body — 2–3 short paragraphs that elaborate]
[Closing — a one-line CTA, calm and instructional, no exclamation]
```

Example:
> *Antes do tratamento, começamos por ouvir.*
>
> *Na Serrano Clínica, acreditamos que um bom diagnóstico começa com atenção aos detalhes e tempo dedicado a cada utente. Aqui, não tratamos apenas sintomas, cuidamos de pessoas.*
>
> *Cada utente merece tempo, atenção e acompanhamento personalizado.*
>
> *Marque a sua consulta*

### Canonical brand name

The canonical name is **Clínica Serrano**, written in that order, in every caption, every paragraph, every sentence position. This follows the Portuguese natural construction for clinics (noun + qualifier: *Clínica Lemos*, *Hospital de São João*) and matches how patients refer to it conversationally.

The inversion **Serrano Clínica** is **deprecated**. Several earlier captions used it mid-sentence ("Na Serrano Clínica, ..."); those are legacy artifacts and should be rewritten on next refresh. Future copy must use `Clínica Serrano` regardless of sentence position.

The wordmark itself stays as `SERRANO CLÍNICA` — the typographic emphasis on the surname is a logo-level design choice, not a sentence. The logo is a logo; the name is a name.

See `CHANGELOG.md` ADR-0001 for the reasoning.

## Open questions

- Whether there's a hashtag strategy or none at all (none observed in the captions seen so far).
- Tone for replies/DMs — same calm voice, or warmer/looser?
- Whether educational/explanatory posts (e.g. "what is laserterapia mamilar?") follow the philosophy structure or get their own format.
