---
name: lml-tavole-social
description: Genera le tavole per i caroselli Instagram e LinkedIn del profilo personale Ivan Arpino (LML Technologies) tramite Higgsfield, producendo prompt completi in inglese con coordinate fisse, palette bloccata, render 3D isometrico e riga di chiusura identica su ogni tavola. Usa SEMPRE questa skill quando l'utente chiede di creare, generare, modificare o impaginare una tavola, un carosello, un post social, una copertina, una grafica per Instagram o LinkedIn, oppure quando chiede un prompt per Higgsfield o per un generatore di immagini, anche se non nomina la skill, non nomina Higgsfield e dice solo "fammi un post", "creami una grafica", "una tavola sul tema X" o allega una tavola da correggere.
---

# Tavole social — sistema visivo

Genera prompt per Higgsfield che producono tavole 4:5 pronte per il flusso, coerenti fra loro tavola dopo tavola e carosello dopo carosello.

Il valore di questo sistema non sta nella singola tavola bella: sta nel fatto che venti tavole prodotte a distanza di settimane sembrino la stessa mano. Per questo le misure sono coordinate esatte e non indicazioni, e la riga di chiusura è identica ovunque.

## Come si usa

1. Chiedi o deduci: **direzione** (chiara o scura), **argomento**, **numero di tavole**.
2. Leggi `references/direzioni.md` per il blocco FONDAMENTI della direzione scelta.
3. Se serve un argomento, leggi `references/argomenti.md`.
4. Componi il prompt: FONDAMENTI + LAYOUT con coordinate + RIGA DI CHIUSURA + AVOID.
5. Genera con `Higgsfield:generate_image`, modello `nano_banana_pro`, `aspect_ratio: "4:5"`.
6. Applica la checklist di verifica.

I prompt si scrivono **in inglese**, il testo dentro la tavola resta **in italiano**. I modelli di immagine seguono meglio istruzioni in inglese, ma il contenuto è per un pubblico italiano.

## La regola che conta più di tutte

**Genera sempre la tavola intera da zero. Non incatenare modifiche.**

Ogni modifica su immagine rigenera l'intero fotogramma: il testo si ammorbidisce, le lettere si corrompono, e al terzo passaggio la tavola è visibilmente peggiore delle sorelle. Se una tavola ha bisogno di tre correzioni, riscrivi il prompt completo con le tre correzioni già dentro e rigenera una volta sola.

Le modifiche su immagine esistente si giustificano solo in due casi: aggiungere un singolo elemento a una tavola altrimenti perfetta, oppure allargare un render fotografico. In entrambi i casi passa il **job_id della generazione originale** come `medias`, mai uno screenshot: gli screenshot portano compressione e ritagli.

## Misure — identiche su ogni tavola

Tela 1080 x 1350 px, rapporto 4:5. Margini: laterali 65 px, alto 81 px, basso 108 px. Niente li attraversa mai.

Il gancio della tavola sta fra il 20% e il 45% dell'altezza: quella fascia resta libera perché è dove cade l'occhio nel flusso.

## Riga di chiusura — da copiare invariata

Questa è la parte che rende riconoscibile la serie. Le coordinate sono esatte perché due tavole con la firma a quote diverse si notano mentre si scorre, anche se ogni singola tavola è impeccabile.

```
BOTTOM ROW. Canvas is 1080 x 1350 px, left margin 65 px, right margin 65 px.
"IVAN ARPINO": uppercase, baseline at y=1242, starting flush at x=65 from the left
edge. Small size, regular weight, MODERATE uniform letter-spacing - not
wide-tracked, not tight.
ARROW: one thin right-pointing arrow, vertically centred on the same y=1242
baseline as "IVAN ARPINO", so the two sit on one horizontal line. Total length
120 px, ending flush at x=1015 from the left edge. Uniform 1.4 px monoline stroke,
simple shaft with a small open arrowhead, outline only, no circle, no fill, no
shadow.
"Generated with AI": baseline at y=1290, right-aligned ending flush at x=1015.
Sentence case, capital G only, very small, lighter than every other element.
Nothing else occupies the bottom margin. No horizontal rule at the bottom.
```

I colori di firma, freccia e dicitura cambiano con la direzione: prendili da `references/direzioni.md`.

**Sull'ultima tavola del carosello, ometti la freccia.** Indica una tavola che non esiste. Firma e dicitura restano.

**La dicitura "Generated with AI" va su ogni tavola**, non solo sulla copertina: chi apre la terza tavola da una condivisione non ha visto la prima. Su TikTok va anche dichiarato al momento della pubblicazione, non basta scriverlo sulla tavola.

## Filetto in alto — su ogni tavola, copertina compresa

```
y = 81: one thin hairline horizontal rule spanning the full column width from
x=65 to x=1015. On that rule: a small uppercase micro-label at the left, starting
flush at x=65, and the plate number at the far right ending flush at x=1015,
written as "01 / 03".
```

L'etichetta a sinistra nomina la rubrica: `CANTIERE` per i progetti in corso, `LO FACCIO IO` per cose già provate, `OBBLIGHI` per normativa e scadenze. Sono le stesse evidenze del profilo, quindi la tavola dice subito a quale filone appartiene.

## Tipografia

Poppins, e nient'altro. Titolo maiuscolo, extra bold, interlinea stretta, da due a quattro righe. Corpo regular, piccolo. Micro-etichette maiuscole, piccole, spaziatura larga.

**Una sola riga del titolo prende il colore d'accento.** Mai due, mai una parola isolata dentro una riga. È il vincolo che tiene insieme tutte le tavole della serie.

Allineamento: la direzione chiara è centrata su asse verticale, la direzione scura è centrata anch'essa. La riga di chiusura è invece sempre allineata ai bordi, mai centrata.

### Far uscire il testo giusto

I modelli sbagliano le lettere, e in italiano più che in inglese. Difese, in ordine di efficacia:

- **Poche parole.** Sotto le venti parole totali gli errori crollano. Titolo da cinque a otto parole, sottotitolo da una a due righe.
- **Niente lettere accentate.** Riscrivi per evitarle: "gia" diventa "adesso", "perche" diventa "il motivo". Metti `accented characters` nell'AVOID.
- **Maiuscolo nel titolo.** Meno forme da sbagliare.
- **Le stringhe esatte fra virgolette**, riga per riga, con l'indicazione di quale riga prende l'accento.

Se il testo esce storto, **accorcia invece di rigenerare uguale**: rigenerare la stessa stringa lunga produce lo stesso errore.

## Il render tridimensionale

L'elemento 3D è il carattere della serie. Due varianti, entrambe opache.

**Isometrico in argilla** — per concetti, strutture, relazioni fra parti:

```
A SOFT 3D ISOMETRIC RENDER, centred. Matte clay surfaces, unpolished, powdery, no
gloss, no chrome, no reflections. One soft diffused light from the upper left,
gentle ambient occlusion, long low-contrast shadows falling onto the background.
Thin connector lines at 1.4 px. Like an architectural model photographed on paper.
No text on the render.
```

**Scena fotoreale** — per ambienti di lavoro, solo in direzione scura:

```
A PHOTOREAL 3D SCENE shot from a low three-quarter angle. Everything matte, no
chrome, no gloss. Deep shadows, one warm key light, gentle ambient occlusion,
shallow depth of field. No screens with legible text, no logos, no brand marks,
no people, no faces.
```

Il render sta **sotto il blocco di testo, mai dietro**. Testo sopra una fotografia è la cosa che fa somigliare la tavola a un post fatto al volo.

Se il render è fotoreale e non arriva ai margini, o lo porti a vivo su entrambi i lati o lo tieni dentro una cornice definita con filetto: le fasce scure asimmetriche accanto a una foto si notano.

Il 3D tende al lucido: se esce plasticoso, aggiungi `matte clay, unpolished, powdery surface` subito dopo la descrizione degli oggetti.

## Struttura di un carosello a tre tavole

- **Tavola 1** — il gancio. Titolo più lungo, render presente, la tavola che fa il 90% del lavoro.
- **Tavola 2** — la sostanza. Elenco, schede o righe. Nessun render: qui il contenuto è la struttura.
- **Tavola 3** — la chiusura. Titolo breve, render, e una riga che dice cosa succede adesso. Niente invito all'acquisto.

Massimo sette voci sulla tavola 2. Oltre, il testo diventa troppo piccolo per il telefono e il modello inizia a sbagliare le parole.

## Vincoli di contenuto

Valgono sempre, e vengono prima dell'estetica:

- **Nessun logo reale, nessun marchio riconoscibile.** Se serve un simbolo, si disegna astratto.
- **Nessun volto, nessuna persona identificabile.**
- **Nessun testo leggibile dentro fotografie o schermi** del render.
- **Niente che possa passare per un cliente, un cantiere o un risultato reale.** Il materiale generato è ambientazione, mai prova.
- **Niente emoji, niente pulsanti d'azione, niente elenchi di servizi**, niente inviti a scrivere in privato. Sono i vincoli del profilo che non vende.
- **Niente cliché AI**: cervelli luminosi, circuiti, robot umanoidi, ologrammi azzurri, pannelli dati fluttuanti.

## Blocco AVOID

Va in fondo al prompt, mai sparso fra le istruzioni.

```
AVOID: real brand logos, recognisable trademarks, social media logos, app icons,
readable screen interfaces, dashboards, charts, screenshots, faces, people, hands,
emoji, watermark, gibberish text, misspelled words, scrambled letters, duplicated
words, extra characters, accented characters, sci-fi, holograms, circuit patterns,
robots, glowing brains, neon, glow, glossy plastic, chrome, reflections, harsh
shadows, lens flare, oversaturation, gradients, vignette, collage, overlapping
elements, text over the photograph, clutter, centred bottom row, more than three
colours.
```

Aggiungi in coda i colori dell'altra direzione: generando in chiara escludi `dark background, black background`; in scura escludi `light background, white background`.

## Checklist prima di tenere una tavola

Dieci secondi, guardando:

- Le parole sono tutte scritte giuste, lettera per lettera
- Una sola riga del titolo ha il colore d'accento
- Il filetto in alto c'è, con etichetta a sinistra e numero a destra
- Firma, freccia e dicitura sono sulla riga di chiusura alle quote giuste
- Il fondo è piatto: nessun alone, nessuna vignettatura, nessuna dominante negli angoli
- Nessun volto, nessun logo, nessun testo leggibile dentro il render
- Il render è opaco, non lucido

Poi il controllo che conta davvero: **le tavole in fila, sul telefono, dentro il flusso**. Il fondo deve essere identico fra una tavola e l'altra, e firma e freccia devono stare alla stessa quota. Una tavola che regge sul monitor può sparire in un flusso; il contrario non capita quasi mai.

## Quando smettere di insistere con il generativo

Un modello di immagine non lavora davvero a coordinate: le approssima. Se dopo due tentativi restano differenze di pochi pixel sulla riga di chiusura, la risposta non è un terzo tentativo.

Firma, freccia, dicitura e filetto sono elementi fissi, identici su ogni tavola, e non cambiano mai. Sovrapposti in HTML/CSS vengono al pixel esatto, una volta sola, per tutte le tavole future. Il generativo serve per il render e per il fondo; il deterministico per ciò che deve essere sempre uguale.

## Animazione

Si fa in un secondo passaggio: prima la tavola ferma, poi quella approvata come primo fotogramma per il modello video. Chiedere direttamente un video con del testo dentro degrada la tipografia fotogramma per fotogramma.

Movimenti brevi, quattro o cinque secondi, in ciclo, con la tipografia dichiarata bloccata. Meglio ancora: anima il solo render senza testo e sovrapponi la tipografia dopo.

## Nomi dei file

```
20260819_chiara_gancio_4x5_v1.png
20260819_scura_catena-02_4x5_v1.png
```

`data_direzione_argomento_formato_versione`. Accanto, una riga con il modello e il seme usato: senza quella la serie non si riproduce.
