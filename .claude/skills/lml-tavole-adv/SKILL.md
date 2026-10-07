---
name: lml-tavole-adv
description: Genera le immagini statiche delle inserzioni Meta di LML Technologies — un solo messaggio per immagine, leggibile a colpo d'occhio sul telefono, nei tre formati 4:5, 1:1 e 9:16, firmate LML Technologies e non con il profilo personale di Ivan. Usa SEMPRE questa skill quando l'utente chiede una grafica, un'immagine o una creatività statica PER UNA INSERZIONE o una campagna, quando parte da un brief di produzione del pacchetto inserzione, o quando dice "la statica della campagna", "l'immagine dell'inserzione", "la creatività C2", "una grafica per la pubblicità". NON usare questa skill per i caroselli e i post del profilo personale di Ivan Arpino: quelli restano a lml-tavole-social, che non va mai modificata. Si ferma all'immagine approvata; il caricamento su Meta lo fa la skill di scrittura sicura.
---

# Tavole pubblicitarie — immagini per le inserzioni

**Versione 1.0 — 13 settembre 2026.** Variante pubblicitaria di `lml-tavole-social`, che resta invariata e continua a governare i caroselli del profilo personale. La copia dell'originale da cui questa nasce è in `references/tavole-social-originale-v1.md`. La palette è in `references/direzioni.md`, copiata identica: **i colori non cambiano fra profilo e inserzione.**

## Perché una skill separata

L'originale fa caroselli per il profilo personale di Ivan. Tre cose, lì, sono incompatibili con un'inserzione, e sono scritte nero su bianco nell'originale stesso:

| | Carosello del profilo | Inserzione |
|---|---|---|
| Firma | `IVAN ARPINO →` in basso | **LML Technologies** |
| Etichetta in alto | rubrica del profilo (`CANTIERE`, `OBBLIGHI`) | **nessuna**: chi la vede non segue il profilo |
| Freccia di continuità | sì, porta alla tavola dopo | **no**: non c'è una tavola dopo |
| Numero di tavola `01 / 03` | sì | **no** |
| Inviti | «niente pulsanti d'azione, niente inviti a scrivere» | **la richiesta ci vuole** |
| Formato | 4:5 e basta | **4:5, 1:1 e 9:16** |
| Chi guarda | chi ci segue | chi non ci conosce |
| Quante se ne fanno | tre per carosello | **molte, per trovare quella che regge** |

Cosa resta identico, perché funziona: la palette e i blocchi di fondamenti delle due direzioni, Poppins e nient'altro, una sola riga del titolo con il colore d'accento, il render opaco mai lucido, le difese contro le lettere sbagliate, il divieto di loghi e volti, e — soprattutto — **rigenerare sempre da zero invece di incatenare correzioni.**

## I fatti che governano un'immagine pubblicitaria

Verificati a settembre 2026. Da riverificare ogni sei mesi.

**1. Un messaggio per immagine.** Un'immagine che prova a dire tre cose non ne dice nessuna. Per noi: un momento, una promessa. Non l'elenco delle cose che ARYA sa fare.

**2. Sul video hai tre secondi, sulla statica un'occhiata.** La gerarchia deve essere brutale: l'occhio cade sul punto focale, poi sul titolo, poi sulla richiesta, poi sul marchio. **In quest'ordine.** Il fallimento più comune è la democrazia visiva, dove immagine, titolo e marchio hanno lo stesso peso e chi guarda non ne sceglie nessuno.

**3. Il marchio è l'ultimo, non il primo.** Vale per le immagini quanto per i video.

**4. Sulla statica il contrasto fa il lavoro che nel video fa il movimento.** Un forte contrasto di luminosità fra il soggetto e il fondo è quello che ferma il pollice. La direzione chiara, con il blu notte sull'avorio, lo ha già.

**5. La statica non è il fratello povero del video.** Su feed Facebook e Instagram la statica costa meno per clic nelle campagne che chiedono un'azione; il video vince sui Reels. E costa molto meno produrla, quindi se ne possono fare tante — che è quello che serve davvero, perché la creatività che funziona si trova provando, non scegliendo.

**6. I formati, e le zone coperte dall'interfaccia:**

| Formato | Dove | Attenzione |
|---|---|---|
| **4:5** (1080×1350) | feed | nessuna interfaccia sopra: serve solo aria ai bordi. Rende un po' più del quadrato |
| **1:1** (1080×1080) | ovunque, ripiego universale | Marketplace, colonna destra, Messenger |
| **9:16** (1080×1920) | storie e Reels | **l'interfaccia copre il 14% in alto e fino al 35% in basso.** È il formato più stretto |

Da marzo 2026 storie e Reels hanno una zona sicura unica: **una sola immagine verticale disegnata per i Reels va bene su entrambi.** Il contrario no.

**Sui telefoni più stretti (20:9) Meta ritaglia i lati** senza chiedere. Quindi nel 9:16 niente di importante vicino ai bordi laterali: tutto nell'80% centrale.

**Regola di progetto: si disegna il 9:16 come immagine madre**, con tutto il contenuto nella fascia centrale sicura, e da lì si ricavano 4:5 e 1:1. Non si parte dal 4:5 e si allunga.

**7. Poca scritta.** La vecchia regola del 20% non c'è più, ma le immagini cariche di testo vengono mostrate meno lo stesso. E in generativo, meno parole vuol dire meno lettere sbagliate: la regola dell'originale vale doppio qui.

## Prima di cominciare — leggi sempre

1. **Il brief di produzione** dentro `inserzioni/<settore>/<blocco>.md`: gancio, promessa ammessa, prova nella forma consentita, cosa prova questa creatività. **Se non c'è, fermati.**
2. `settori/<settore>.md` — la colonna "sì".
3. `voce/<settore>/` — le frasi esatte, da cui nasce il titolo.
4. `.agents/customer-language.md` — parole da usare e da evitare.
5. `references/direzioni.md` — i fondamenti della direzione scelta.
6. `regole-adv.md` §5.1, §18, §23.

**Non si sceglie l'argomento.** Nell'originale la skill può partire da `argomenti.md`: qui l'argomento è l'angolo in campo, già deciso.

## Cosa entra e cosa esce

**Entra:** settore, blocco, quale creatività (C1, C2, C3), direzione (chiara o scura).

**Esce:** tre file immagine (9:16, 4:5, 1:1) in `inserzioni/<settore>/`, più una riga con modello e seme usati. Senza quella, la serie non si riproduce.

---

## L'impaginazione

Quattro elementi, in quest'ordine di peso. **Nient'altro.**

**1 — Il titolo.** È il gancio. Fa il lavoro che nel video fanno i primi tre secondi.

- Da cinque a otto parole. Maiuscolo, extra bold, interlinea stretta.
- **Una sola riga prende il colore d'accento.** Regola dell'originale, non negoziabile.
- Nasce da una frase della scheda voce, e la cita nel file di consegna.
- Passa il **test degli attributi personali**: togli il prodotto e rileggi. Se dice al lettore qualcosa su di lui, si riscrive.
- Niente lettere accentate: si riscrive per evitarle.

**2 — Il render, o il fermo immagine.** Sotto il titolo, mai dietro. Testo sopra una fotografia è la cosa che fa sembrare l'immagine un post fatto al volo — vale ancora di più quando si sta pagando per mostrarla.

**3 — La richiesta.** Una riga, sotto. Dice l'azione e cosa succede: si apre WhatsApp, risponde qualcuno. **Questo è l'elemento che nell'originale è vietato e qui è obbligatorio.**

**4 — Il marchio.** In basso, piccolo, per ultimo.

### La riga di chiusura

Sostituisce quella del profilo. Coordinate sul 9:16 (1080×1920), tutte **dentro la zona sicura**, quindi sopra il 35% coperto dall'interfaccia:

```
BOTTOM ROW. Canvas 1080 x 1920 px, left margin 96 px, right margin 96 px.
Nothing below y=1248 - the bottom 35% is covered by the platform interface.
"LML TECHNOLOGIES": uppercase, baseline at y=1180, starting flush at x=96 from
the left edge. Small size, regular weight, MODERATE uniform letter-spacing.
No arrow. No plate number. No micro-label at the top of the frame.
```

- **Niente freccia**: indicherebbe una tavola che non esiste.
- **Niente filetto in alto con rubrica e numero**: sono segni del profilo, e chi vede l'inserzione non lo segue.
- **Niente "Generated with AI" scritto da noi.** Meta applica da sola l'etichetta alle immagini realistiche fatte con l'AI, e non si può togliere. Scriverlo anche dentro l'immagine vorrebbe dire dirlo due volte e togliere spazio al messaggio. Se l'immagine è un render astratto, l'etichetta di solito non compare: in quel caso **non si dichiara nulla di falso e non si simula niente di reale**, che è la regola che conta davvero.

Sul 4:5 e sull'1:1 la riga di chiusura si riposiziona ai margini di quel formato, con le stesse proporzioni.

## I tre formati

Si genera il **9:16** e si compongono gli altri due dalla stessa idea, rigenerando (mai ritagliando a macchina: il titolo si spezza).

| | 9:16 | 4:5 | 1:1 |
|---|---|---|---|
| Tela | 1080×1920 | 1080×1350 | 1080×1080 |
| Margini laterali | 96 px, **e niente di importante fuori dall'80% centrale** | 65 px | 100 px |
| Alto | niente sopra y=270 (14% coperto) | 81 px | 100 px |
| Basso | **niente sotto y=1248** (35% coperto) | 108 px | 100 px |
| Titolo | fra il 25% e il 50% dell'altezza | fra il 20% e il 45% | centrato |

## Come si fa il testo giusto

Regole dell'originale, valide e rafforzate: poche parole, niente accenti, maiuscolo nel titolo, stringhe esatte fra virgolette riga per riga, e **se esce storto si accorcia, non si rigenera uguale**.

La regola più importante resta quella: **si rigenera sempre tutta l'immagine da zero.** Ogni correzione su un'immagine già fatta ricalcola il fotogramma intero, il testo si ammorbidisce, e al terzo passaggio l'immagine è peggiore. Se servono tre correzioni, si riscrive il prompt con tutte e tre dentro e si genera una volta sola.

## Fare tante immagini, non una perfetta

La differenza più grossa con il profilo. Lì si fanno tre tavole e si curano. Qui **si producono varianti**, perché la creatività che regge si trova provando.

Dentro un blocco, le varianti cambiano **una cosa per volta**:
- lo stesso titolo con un render diverso;
- lo stesso render con un titolo diverso;
- la stessa impaginazione nelle due direzioni, chiara e scura.

**Non cambiano la promessa**: quella è l'angolo, e l'angolo è uno solo per blocco.

## Vincoli di contenuto

Quelli dell'originale, che valgono uguale e in più sono obblighi di legge e di regolamento:

- **Nessun logo reale, nessun marchio riconoscibile** — nemmeno quello di un gestionale che nominiamo.
- **Nessun volto, nessuna persona identificabile.**
- **Nessun testo leggibile dentro schermi o fotografie** del render. Uno schermo finto con una conversazione dentro sembrerebbe una conversazione vera: è la cosa che la §23 vieta.
- **Niente che possa passare per un cliente o un risultato reale.** Il generato è ambientazione, mai prova.
- **Niente cliché AI**: cervelli luminosi, circuiti, robot, ologrammi azzurri.
- **Niente numeri non misurati.**
- **Niente promesse fuori dalla colonna "sì".**

## Blocco AVOID

Quello dell'originale, con due aggiunte in coda per le inserzioni:

```
AVOID: real brand logos, recognisable trademarks, social media logos, app icons,
readable screen interfaces, dashboards, charts, screenshots, faces, people, hands,
emoji, watermark, gibberish text, misspelled words, scrambled letters, duplicated
words, extra characters, accented characters, sci-fi, holograms, circuit patterns,
robots, glowing brains, neon, glow, glossy plastic, chrome, reflections, harsh
shadows, lens flare, oversaturation, gradients, vignette, collage, overlapping
elements, text over the photograph, clutter, more than three colours,
arrow, plate number, page counter, personal signature, rubric label.
```

Più i colori dell'altra direzione, come nell'originale.

## Controllo prima di tenere un'immagine

Dieci secondi, guardando:

- Le parole sono scritte giuste, lettera per lettera
- Una sola riga del titolo ha il colore d'accento
- **Nessuna freccia, nessun numero di tavola, nessuna rubrica in alto, nessuna firma personale**
- La firma dice LML Technologies
- La richiesta c'è, ed è una riga sola
- Sul 9:16: niente sopra il 14% e **niente sotto il 35%**; niente di importante fuori dall'80% centrale in larghezza
- Il fondo è piatto: nessun alone, nessuna dominante negli angoli
- Nessun volto, nessun logo, nessuno schermo leggibile
- Il render è opaco

Poi i due controlli che contano:

1. **Sul telefono, a grandezza di miniatura.** Se il titolo non si legge lì, l'immagine non esiste. Un'immagine che regge sul monitor può sparire nel flusso.
2. **La gerarchia:** guardando di sfuggita, cosa si vede per primo? Se non è il titolo o il punto focale, si rifà.

## Quando smettere con il generativo

Regola dell'originale, e qui vale di più: un modello di immagine **approssima** le coordinate. La riga di chiusura, la firma e i margini sono elementi fissi identici su ogni immagine. Sovrapposti in HTML/CSS vengono al pixel esatto, una volta sola, per tutte le immagini future.

Per le inserzioni la cosa è più urgente che per il profilo: qui le immagini si fanno a decine, non a tre. **Conviene fissare presto il modello deterministico** e lasciare al generativo solo il render e il fondo.

## Nomi dei file

```
20260914_rivenditori_B1-lunedi-mattina_C2_9x16_v1.png
20260914_rivenditori_B1-lunedi-mattina_C2_4x5_v1.png
```

`data_settore_blocco_creativita_formato_versione`. Accanto, modello e seme.

## Regole vincolanti

1. **Solo da un brief di produzione.**
2. **Niente fuori dalla colonna "sì".**
3. **Un messaggio per immagine.**
4. **Firma LML Technologies. Mai la firma personale, mai freccia, mai numero, mai rubrica.**
5. **Si disegna il 9:16 come madre**, con tutto nella zona sicura.
6. **Si rigenera da zero**, non si incatenano correzioni.
7. **Test degli attributi personali** sul titolo.
8. **Niente schermi leggibili, niente finte conversazioni.**
9. **Non si modifica `lml-tavole-social`.** Se serve un cambiamento che riguarda anche il profilo, si segnala a Ivan.
10. **Nessuna pubblicazione prima del collaudo e del sì di Ivan.**

## Cosa fa dopo, e chi

Le immagini tornano nel pacchetto inserzione, passano il **collaudo**, e la **scrittura sicura su Meta** le carica nell'inserzione con il nome del blocco.

Va segnalato in chat: un titolo che funzionerebbe ma richiede una promessa non ammessa; un titolo che non passa gli attributi personali e non si riesce a riscrivere; il momento in cui conviene passare all'impaginazione deterministica perché le varianti sono troppe.
