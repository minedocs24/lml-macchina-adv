---
name: lml-copione-video-adv
description: Scrive i copioni dei video pubblicitari di LML Technologies destinati alle inserzioni Meta — 15-25 secondi, gancio nei primi 2 secondi, comprensibili senza audio, con una richiesta finale esplicita e verticali 9:16. Usa SEMPRE questa skill quando l'utente chiede il copione, lo script o il girato di un VIDEO PUBBLICITARIO, di una creatività per una campagna, di una inserzione video, quando parte da un brief di produzione del pacchetto inserzione, oppure quando dice "il video per la campagna rivenditori", "gira il video dell'inserzione", "il copione della creatività C1". NON usare questa skill per i video del profilo personale di Ivan Arpino: quelli restano a lml-copione-video, che non va mai modificata. Il montaggio lo esegue lml-montaggio-video. Questa skill si ferma prima della ripresa.
---

# LML — Copione dei video pubblicitari

**Versione 1.0 — 13 settembre 2026.** Variante pubblicitaria di `lml-copione-video`, che resta invariata e continua a governare i video del profilo personale. La copia dell'originale da cui questa nasce è in `references/copione-originale-v1.md`.

## Perché una skill separata

`lml-copione-video` scrive video per il profilo personale, e dice testualmente: nessuna vendita, nessuna richiesta commerciale, nessun servizio nominato. Un video pubblicitario fa esattamente il contrario: **è pagato per chiedere qualcosa**, dura un quarto del tempo, e viene visto in mezzo a uno scorrimento da qualcuno che non ci conosce.

| | Profilo personale | Inserzione |
|---|---|---|
| Durata | 25-90 secondi | **15-25 secondi** |
| Primi 6-8 secondi | solo faccia e sottotitoli, niente grafica | **il gancio, e deve già dire tutto** |
| Struttura | sette blocchi, curva di energia | **quattro blocchi** |
| Richiesta finale | mai | **sempre, esplicita** |
| Chi guarda | chi ci segue | chi non ci conosce |
| Audio | si presume acceso | **si presume spento** |
| Chi decide se funziona | il pubblico, nel tempo | la spesa, in 7 giorni |

Cosa resta dell'originale, perché funziona anche qui: i silenzi recitati e non montati, le icone come oggetti fisici concreti, le regole di sottrazione, il divieto di percentuali inventate, la chiusura senza enfasi sull'ultima parola, e la persona di riferimento — titolare di PMI.

## I fatti che governano un video pubblicitario

Verificati a settembre 2026. Da riverificare ogni sei mesi.

**1. I primi 3 secondi decidono.** Meta conta una visualizzazione a 3 secondi, e quel numero — la quota di chi resta oltre i 3 secondi — condiziona quanto l'inserzione viene mostrata. Un buon valore è sopra il 30%. Sotto, la maggior parte del budget non arriva nemmeno al messaggio.

**2. Si guarda senza audio.** La stima più citata è che circa l'85% dei video su Facebook venga guardato muto. Se una frase esiste solo nella voce, per la maggior parte del pubblico non esiste. **Sottotitoli incisi, sempre**, e il gancio scritto sullo schermo nel primo fotogramma.

**3. Il logo all'inizio uccide il video.** Aprire con due secondi di marchio o con una panoramica lenta fa perdere metà del pubblico prima del messaggio. **Il marchio va in fondo**, mai in testa.

**4. 15-30 secondi per chiedere qualcosa.** Sotto i 15 si completa di più ma non si fa in tempo a convincere; sopra i 30 si perde gente prima della richiesta. Per noi: **15-25 secondi**, con la richiesta che arriva entro il quindicesimo.

**5. Verticale, 9:16.** Oltre due terzi delle visualizzazioni sono su telefono in verticale. Si gira verticale e poi si ritaglia 4:5 per il feed, mai il contrario.

**6. Sembrare un contenuto, non uno spot.** I video che aprono come una pubblicità rendono meno di quelli che sembrano un post normale. Per noi è una fortuna: la faccia di Ivan che parla al telefono è già quello.

## Prima di cominciare — leggi sempre

1. **Il brief di produzione** dentro `inserzioni/<settore>/<blocco>.md`. Contiene il gancio visivo, la promessa ammessa, la prova nella forma consentita. **Se non c'è il brief, fermati.**
2. `settori/<settore>.md` — la colonna "sì". Il copione non può dire niente che non stia lì.
3. `voce/<settore>/` — le frasi esatte. Il parlato si costruisce da qui.
4. `.agents/customer-language.md` — parole da usare e da evitare.
5. `regole-adv.md` §5.1, §18, §20, §23.
6. `lml-montaggio-video` — palette, icone, coordinate. Non si riscrivono qui.

**Non si fa la ricerca dell'angolo.** Nell'originale la Fase 1 cerca l'attualità sul web: qui l'angolo è già stato deciso dalla coda degli angoli e scritto nel pacchetto. Cercarne un altro vorrebbe dire rompere il blocco.

## Cosa entra e cosa esce

**Entra:** settore, blocco, e quale creatività del pacchetto (C1, C2, C3).

**Esce:** un file markdown in `inserzioni/<settore>/<blocco>-<C>-copione.md`, con il copione blocco per blocco, le note di ripresa e la tabella tecnica. Poi va al montaggio.

---

## La struttura — quattro blocchi

Non sette. La curva di energia lunga qui non c'è: non c'è tempo.

**0 — Gancio** *(0-3 secondi)*

Il blocco che conta più di tutti gli altri messi insieme.

- **Si vede e si legge nel primo fotogramma.** La frase del gancio scritta a schermo, grande, leggibile senza audio.
- **È la scena della frase della voce**, non la frase spiegata. Se la frase è *"il lunedì mattina trovo dieci chiamate perse"*, si vede lo schermo del telefono con le chiamate perse, oppure Ivan che lo dice guardando in camera. Si scrive **cosa si vede**, non cosa si dice.
- **Niente marchio, niente logo, niente panoramica.**
- **Nessun silenzio qui.** Nell'originale la testa ha 0,1s; qui nemmeno quello: si parte già dentro la frase.
- Il gancio nomina il **momento**, non il prodotto. Chi guarda non ci conosce.

**1 — La conseguenza** *(3-8 secondi)*

Cosa succede per colpa di quel momento, detto come fatto, non come diagnosi sul lettore. Qui vale il test degli attributi personali: **si racconta una situazione, non si dice al lettore com'è messo.**

Una frase, al massimo due. Se serve spiegare, il gancio era sbagliato.

**2 — Il ribaltamento** *(8-15 secondi) — PICCO**

La promessa, presa dalla colonna "sì". È il "e fa": non solo risponde, agisce.

Qui sta l'unico silenzio del video: **0,4s prima della parola che ribalta.** Nell'originale il silenzio del picco è 0,6s; in 20 secondi 0,6s sono troppi e sembrano un errore di montaggio.

Se la creatività è la registrazione di ARYA, **il picco è la voce vera**: si sente ARYA rispondere. Non si descrive, si fa sentire. È la prova più forte che abbiamo e batte qualunque frase.

**3 — La richiesta** *(15-25 secondi)*

Esplicita. Dice cosa succede se si tocca il pulsante, e deve corrispondere a quello che accade davvero: si apre WhatsApp, risponde ARYA.

- Nessun "contattaci" generico. Si dice l'azione e il risultato.
- La prova, se c'è, sta qui: nella forma ammessa dalla scheda settore, nome solo con consenso scritto.
- Il prezzo si dice se la scheda lo prevede.
- **Il marchio compare qui, non prima.**
- L'ultima frase resta la più lenta, e senza enfasi sull'ultima parola: quella dell'originale è una buona regola e vale anche qui.

### Il conto dei secondi

Circa **150 parole al minuto**, più i silenzi. Quindi:

| Durata | Parole parlate |
|---|---|
| 15 secondi | 35-40 |
| 20 secondi | 45-50 |
| 25 secondi | 55-62 |

Conta sempre e dichiara la durata stimata. Se sfora, il primo taglio è nel blocco 1: la conseguenza è quasi sempre spiegata due volte.

## Ritmo e silenzi

I silenzi **si recitano, non si montano**: se in ripresa si attacca la frase dopo, in montaggio quel silenzio non esiste più. Regola dell'originale, confermata.

Notazione: `// 0,4s` su riga propria.

| Posizione | Durata |
|---|---|
| Prima della parola che ribalta | 0,4s |
| Prima di una cifra | 0,3s |
| Testa | **nessuna** |
| Coda | 0,2s |

**In tutto: uno o due silenzi.** Non di più. In un video di venti secondi ogni pausa costa il 2-3% della durata.

Andatura: il gancio **non corre** — nell'originale la prima frase corre perché è contesto; qui è il messaggio, e va detta chiara. Poi si accelera sulla conseguenza, si frena sul ribaltamento, e la richiesta si dice piano.

## Cosa si costruisce sopra

### Regole di sottrazione

Niente icone, niente suoni, niente movimento in questi punti:

1. **I primi 3 secondi.** Solo la scena e la scritta del gancio. Vale ancora di più che nell'originale: qui si gioca tutto lì.
2. **Il silenzio prima della parola che ribalta.**
3. **Sulle cifre**: il numero a schermo è già l'elemento.
4. **Sulla voce di ARYA**, se c'è: si sente lei, e basta.

### Zoom

**Uno o due in tutto.** Uno sulla parola che ribalta. Eventualmente un tenuto sulla chiusa. Nell'originale un reel standard ne ha sei o sette: qui sarebbero un videoclip.

### Icone

**Due o tre al massimo.** Regole dell'originale, valide e non riscritte qui: oggetto fisico concreto (mai lampadine o ingranaggi), il gesto racconta, e due icone imparentate fanno sistema. Test: coperti i sottotitoli, l'icona deve dire di cosa si parla.

### Sottotitoli

**Obbligatori e incisi**, non attivabili. Parola per parola, come nel montaggio LML. Sono il canale principale, non un aiuto: l'85% guarda muto.

La scritta del gancio è **più grande** dei sottotitoli e resta ferma per i primi 2-3 secondi.

### Zona di sicurezza

Niente di importante nel 10% in alto e nel 10% in basso: l'interfaccia di storie e Reels li copre. Vale per il gancio scritto e per i sottotitoli.

### Suoni

Regole dell'originale, ridotte: **un solo impatto** in tutto il video, sulla parola che ribalta o sulla cifra. Niente riser in apertura — ruba i primi decimi al gancio. Muto assoluto sul silenzio.

---

## Regole vincolanti

1. **Solo da un brief di produzione** di un pacchetto inserzione. Mai a memoria, mai da un'idea.
2. **Niente fuori dalla colonna "sì"** della scheda settore.
3. **Il gancio si capisce senza audio**, nel primo fotogramma.
4. **Niente marchio nei primi 3 secondi.**
5. **Test degli attributi personali** su ogni frase: togli il prodotto e rileggi. Se dice al lettore qualcosa su di lui, riscrivi.
6. **La richiesta finale è esplicita** e corrisponde a quello che succede davvero.
7. **Nessuna percentuale inventata.** Regola dell'originale, vale uguale. I numeri solo se misurati e ancora misurati.
8. **15-25 secondi.** Se il copione non ci sta, l'angolo è troppo largo: si segnala, non si allunga il video.
9. **Non si modifica `lml-copione-video`.** Se serve un cambiamento che riguarda anche il profilo personale, si segnala a Ivan.
10. **Nessuna ripresa prima del collaudo** del pacchetto e del sì di Ivan.

## Consegna

File markdown in `inserzioni/<settore>/<blocco>-<C>-copione.md`, presentato con `present_files`. Non incollarlo tutto in chat: si consulta durante la ripresa e dentro il montaggio.

**Struttura del file:**

1. Titolo, blocco, creatività, durata stimata, formato (9:16, ritaglio 4:5)
2. Legenda: `//` = silenzio da rispettare in ripresa
3. I quattro blocchi, ciascuno con: secondi → cosa si vede → parlato con i silenzi → RITMO → MONTAGGIO
4. **Il gancio scritto**, testo esatto e dove sta a schermo
5. Tabella tecnica: silenzi, zoom, icone, suoni, con i punti di aggancio
6. **Cosa si taglia** se sfora, indicato per nome
7. **Note di ripresa:** le pause si recitano; un secondo di margine in testa e in coda; girare **due versioni del gancio** (le fonti consigliano di provare 3-5 aperture per ogni idea: noi ne giriamo almeno due, costa solo un minuto in più di ripresa)
8. **La promessa usata e la riga della colonna "sì" che la autorizza**

**In chat:** tre o quattro scelte editoriali e il perché, più l'avvertimento pratico più utile. Non elencare cosa hai scritto.

## Lessico e registro

Persona: **titolare di PMI**, come nell'originale. Si parla di conseguenze, non di tecnologia.

**Da non fare mai:**
- parole della lista "da evitare": *soluzione*, *innovativo*, *trasformazione*, *intelligenza artificiale*;
- cliché: *rivoluzione*, *il futuro è adesso*, *non è fantascienza*;
- percentuali inventate;
- aprire con il marchio o con un dato;
- dire al lettore com'è messo.

**Da fare:**
- frasi brevissime, una per riga;
- le parole della voce, così come le dicono;
- far sentire ARYA invece di descriverla;
- chiudere con l'azione, non con un riassunto.

## Cosa fa dopo, e chi

Il copione va a `lml-montaggio-video`, che esegue in ChatCut: sottotitoli, icone, zoom, suoni. Poi il video torna nel pacchetto, passa il collaudo, e la scrittura sicura su Meta lo carica nell'inserzione con il nome del blocco.

Va segnalato in chat: un copione che non sta in 25 secondi (l'angolo è troppo largo); una frase della voce troppo forte per gli attributi personali; un gancio che funzionerebbe solo con una promessa non ammessa.
