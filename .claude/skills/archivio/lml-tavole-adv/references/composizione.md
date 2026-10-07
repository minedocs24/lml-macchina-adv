# Come si compone il prompt — tavola pubblicitaria

Il prompt si scrive **in inglese**, il testo dentro l'immagine resta **in italiano**. Ordine dei blocchi, sempre lo stesso:

1. FONDAMENTI (da `direzioni.md`, con la tela cambiata al formato)
2. LAYOUT con le coordinate
3. RIGA DI CHIUSURA
4. AVOID

Si genera con `Higgsfield:generate_image`, modello `nano_banana_pro`, `aspect_ratio` secondo il formato.

---

## Blocco LAYOUT — 9:16, immagine madre

Da adattare al contenuto, non alla forma. Le quote sono fisse.

```
LAYOUT. Canvas 1080 x 1920 px. Side margins 96 px. Nothing above y=270 - the top
14% is covered by the platform interface. Nothing below y=1248 - the bottom 35%
is covered by the platform interface. All critical content inside the central
80% of the width: between x=108 and x=972. Nothing important near the left or
right edge.

HEADLINE: uppercase, extra bold, tight leading, CENTRED, occupying the band
between y=480 and y=960. Exactly [N] lines, written verbatim:
line 1 "..."
line 2 "..."
line 3 "..."
Line [N] takes the accent colour. No other element takes the accent.

RENDER: below the headline, between y=1000 and y=1200. Never behind the text.

ASK LINE: one single line, regular weight, small, centred, baseline at y=1230.
Written verbatim: "..."

Total words on the whole canvas: under 20.
```

## Blocco RIGA DI CHIUSURA — 9:16

```
BOTTOM ROW. Canvas 1080 x 1920 px, left margin 96 px.
"LML TECHNOLOGIES": uppercase, baseline at y=1180, starting flush at x=96 from
the left edge. Small size, regular weight, MODERATE uniform letter-spacing.
No arrow. No plate number. No page counter. No micro-label anywhere in the frame.
No horizontal rule at the top or at the bottom.
```

## Le quote degli altri due formati

**4:5 — 1080 × 1350.** Margini laterali 65, alto 81, basso 108. Titolo fra y=270 e y=608. Render fra y=650 e y=900. Riga della richiesta a y=1150. Firma a y=1242.

**1:1 — 1080 × 1080.** Margini 100 su ogni lato. Titolo fra y=216 e y=540. Render fra y=580 e y=820. Riga della richiesta a y=900. Firma a y=980.

Gli altri due formati **si rigenerano**, non si ritagliano: un ritaglio a macchina spezza il titolo.

---

## Le varianti dentro un blocco

Si cambia **una cosa per volta**. La promessa mai: quella è l'angolo.

| Variante | Cosa cambia | Cosa resta |
|---|---|---|
| A | titolo | render, direzione, impaginazione |
| B | render | titolo, direzione, impaginazione |
| C | direzione (chiara ↔ scura) | titolo, render, impaginazione |

Tre varianti per blocco sono un buon punto di partenza. Se una regge, le successive partono da quella.

---

## Checklist

### Prima di generare
- [ ] C'è il brief di produzione
- [ ] Il titolo nasce da una frase della voce, citata
- [ ] La promessa sta nella colonna "sì"
- [ ] Nessuna parola della lista "da evitare"
- [ ] Nessuna lettera accentata
- [ ] Sotto le 20 parole in tutto
- [ ] Test attributi personali: tolto il prodotto, il titolo non dice al lettore com'è messo

### Dopo aver generato
- [ ] Parole giuste, lettera per lettera
- [ ] Una sola riga con l'accento
- [ ] Nessuna freccia, nessun numero di tavola, nessuna rubrica, nessuna firma personale
- [ ] Firma: LML Technologies
- [ ] La richiesta c'è, una riga sola
- [ ] 9:16: niente sopra y=270, niente sotto y=1248, niente fuori da x=108-972
- [ ] Fondo piatto, nessuna dominante negli angoli
- [ ] Nessun volto, nessun logo, nessuno schermo leggibile
- [ ] Render opaco

### I due controlli che contano
- [ ] **A grandezza di miniatura, sul telefono:** il titolo si legge?
- [ ] **Di sfuggita:** cosa si vede per primo? Se non è il titolo o il punto focale, si rifà.

### Consegna
- [ ] Tre formati: 9:16, 4:5, 1:1
- [ ] Nome file `data_settore_blocco_creativita_formato_versione`
- [ ] Riga con modello e seme
- [ ] Frase della voce da cui nasce il titolo
- [ ] Riga della colonna "sì" che autorizza la promessa
