# Le due direzioni

Ogni tavola appartiene a una sola direzione, e una direzione non si mescola mai con l'altra dentro lo stesso carosello.

Indice:
- Direzione chiara — blu notte e acciaio
- Direzione scura — ambra su grafite
- Come si sceglie
- Esempio completo, direzione chiara
- Esempio completo, direzione scura

---

## Direzione chiara — blu notte e acciaio

Il chiaro domina. Legge come una pagina di bilancio ben impaginata, e per un pubblico manifatturiero quel registro è più credibile di un fondo scuro.

| Ruolo | Valore |
|---|---|
| Fondo | `#F5F5F2` avorio caldo, piatto |
| Titolo e testo primario | `#101B2D` blu notte |
| Testo secondario e descrizioni | `#8A94A0` grigio acciaio |
| Accento unico | `#2E5C8A` blu acciaio |
| Filetti e bordi | blu notte al 30% di opacità |
| Firma in basso a sinistra | `#101B2D` |
| Freccia | `#2E5C8A` |
| Dicitura "Generated with AI" | `#8A94A0` |

Blocco FONDAMENTI da incollare:

```
Editorial poster, print-quality graphic design, vertical 4:5, 1080 x 1350 px.
A designed page. Not a photograph, not a collage, not a UI mockup.

FOUNDATIONS: flat solid background warm off-white #F5F5F2 across the entire frame,
absolutely uniform - no gradient, no vignette, no tint, no warm cream cast, no
green cast, no cool blue cast, no darkening at any edge. Every corner exactly the
same value as the centre. Very fine even paper grain, uniform across the whole
canvas. Light surface dominates, at least 65% of the frame. Headline and primary
type midnight blue #101B2D. Secondary and descriptive text steel grey #8A94A0.
Single accent steel blue #2E5C8A, on one headline line and the accent rule only -
nothing else takes the accent. Hairline rules midnight blue at 30% opacity, thin
and quiet. Icon and connector strokes uniform weight 1.4 px. No other colour
anywhere. Typography Poppins geometric sans only: headline uppercase, extra bold,
tight leading, CENTRED; subline regular weight, small; micro-labels uppercase,
small, wide letter-spacing. Side margins 65 px, top margin 81 px, bottom margin
108 px, nothing crosses them.
```

---

## Direzione scura — ambra su grafite

Grafite piatto, non nero caldo: il nero caldo produce una dominante marrone negli angoli e le ultime righe spariscono. L'ambra resta l'unico accento.

| Ruolo | Valore |
|---|---|
| Fondo | `#1C1D20` grafite, piatto |
| Titolo e testo primario | `#F2EEE7` avorio caldo |
| Testo secondario e descrizioni | `#9B9792` attenuato |
| Accento unico | `#E8A33D` ambra |
| Filetti e bordi | ambra al 30% di opacità |
| Tratto delle icone | ambra pieno, 1.4 px |
| Firma in basso a sinistra | `#9B9792` |
| Freccia | `#E8A33D` |
| Dicitura "Generated with AI" | `#9B9792` |

Blocco FONDAMENTI da incollare:

```
Cinematic poster, print-quality graphic design, vertical 4:5, 1080 x 1350 px.

FOUNDATIONS: flat solid background #1C1D20 across the entire frame, absolutely
uniform - no gradient, no vignette, no brown or warm falloff in any corner, no
radial glow, no darkening toward the edges. The bottom right corner is exactly the
same value as the centre. Very fine even film grain, uniform across the whole
canvas. Primary headline text warm off-white #F2EEE7. Secondary and descriptive
text muted #9B9792. Single accent amber #E8A33D, on one headline line only.
Hairline rules and dividers amber #E8A33D at 30% opacity, thin and quiet. Icon
strokes amber #E8A33D at full opacity, uniform stroke weight 1.4 px. No other
colour anywhere. Typography Poppins geometric sans only: headline uppercase, extra
bold, tight leading, CENTRED; subline regular weight, small; micro-labels
uppercase, small, wide letter-spacing. Side margins 65 px, top margin 81 px,
bottom margin 108 px, nothing crosses them.
```

**Avvertenza sulla direzione scura**: ambra su fondo scuro è già l'accostamento di mezzo settore AI. Non è un veto, ma è il motivo per cui vale la pena guardarla nel flusso accanto alla chiara prima di adottarla come direzione principale.

---

## Come si sceglie

Non si sceglie a occhio su un monitor. Si producono tre tavole per direzione con contenuti veri, si guardano sul telefono dentro il flusso in mezzo ad altri contenuti, e si tiene quella che regge in anteprima.

Come regola pratica: la chiara invecchia meglio e si confonde meno con gli altri operatori del settore; la scura ha più presa immediata nel flusso ma somiglia a più cose.

---

## Esempio completo, direzione chiara

Copertina, tre righe di titolo, render isometrico.

```
[FONDAMENTI direzione chiara]

EXACT LAYOUT on a 1080 x 1350 canvas:

y=81: one hairline horizontal rule across the full column width from x=65 to
x=1015, with a small uppercase micro-label "CANTIERE" at the left and "01 / 03" at
the far right, both in steel grey.

y=250 to 580, centred, three lines, reading exactly:
"UN PROFILO"
"CHE NON"
"VENDE."
Lines one and two in midnight blue. Line three, and only line three, in steel blue
#2E5C8A.

y=630: one short horizontal accent rule, 90 px wide, steel blue, centred.

y=690, centred, one line of body text in steel grey, reading exactly:
"Se funziona lo mostro. Se non funziona lo dico."

y=760 to 1150: A SOFT 3D ISOMETRIC RENDER, centred. [descrizione degli oggetti]
Matte clay surfaces, unpolished, powdery, no gloss, no chrome, no reflections. One
soft diffused light from the upper left, gentle ambient occlusion, long
low-contrast shadows falling onto the off-white background. Thin steel blue
connector lines at 1.4 px. Like an architectural model photographed on paper. No
text on the render.

[BOTTOM ROW dal SKILL.md, con firma #101B2D, freccia #2E5C8A, dicitura #8A94A0]

COMPOSITION: strict vertical symmetry on a centred axis. Three elements only: the
text block, the 3D render, the bottom row. Wide calm margins, generous empty
off-white space between every block. Print-like, quiet, precise.

[AVOID + dark background, black background]
```

---

## Esempio completo, direzione scura

Tavola centrale, elenco a righe, nessun render.

```
[FONDAMENTI direzione scura]

EXACT LAYOUT on a 1080 x 1350 canvas:

y=81: one hairline horizontal rule in amber at 30% opacity across the full column
width from x=65 to x=1015, with "CANTIERE" at the left and "02 / 03" at the far
right, both muted grey.

y=190 to 340, centred, two lines, reading exactly:
"COSA FA"
"OGNI PEZZO."
Line one in warm off-white. Line two in amber #E8A33D.

y=400, centred, one line of body text in muted grey, reading exactly:
"Nessun pezzo decide da solo."

y=480 to 1180: seven rows stacked vertically, evenly spaced, each row containing
left to right: a small amber monoline icon at 1.4 px stroke, one uppercase
off-white word, and one short line of muted grey text. Each row separated from the
next by a thin amber hairline at 30% opacity. The rows read exactly:
[sette righe, parola maiuscola + trattino + frase breve]

[BOTTOM ROW dal SKILL.md, con firma #9B9792, freccia #E8A33D, dicitura #9B9792]

COMPOSITION: one single column, left-aligned rows on a centred block, wide calm
margins, deep space between rows. No 3D scene on this plate, no photograph, no
cards, no boxes. Flat, quiet, legible.

[AVOID + light background, white background]
```
