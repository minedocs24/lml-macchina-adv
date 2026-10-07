---
name: lml-collaudo-creativita
description: Collauda un pacchetto inserzione completo di LML Technologies prima che si produca o si pubblichi qualunque cosa — testi, ganci, titoli, immagini, video, messaggio di apertura della chat, nomi e parametri della campagna — contro le regole ADV, la lingua dei clienti, le promesse ammesse dalla scheda settore e le regole di Meta, e restituisce un esito verde, giallo o rosso con le correzioni già scritte. Usa SEMPRE questa skill quando l'utente chiede di controllare, verificare, collaudare o "dare un'occhiata prima di pubblicare" a un'inserzione, una creatività, un pacchetto o una campagna, quando chiede "si può pubblicare?", "è tutto a posto?", "controlla prima di caricare", oppure quando un pacchetto inserzione è appena stato scritto o un video o un'immagine sono appena stati prodotti. NON sostituisce la skill collaudo-testi-adv, che resta invariata e controlla i soli testi: questa copre il pacchetto intero e la richiama se presente. È il nono anello della catena pubblicitaria LML, e nessuna produzione o pubblicazione lo salta.
---

# Collaudo della creatività — l'ultimo controllo prima che costi qualcosa

**Versione 1.0 — 13 settembre 2026.** Solo lettura e scrittura di file. Non tocca Meta. Non riscrive il pacchetto: propone le correzioni e le passa a chi lo ha scritto.

## Una precisazione, perché conta

Esiste già una skill installata, **`collaudo-testi-adv`**, che controlla i testi prima della pubblicazione. **Non va modificata.** Da questa sessione non è leggibile — è installata dal lato Cowork — quindi non è stata duplicata né riscritta: sarebbe stato un lavoro fatto alla cieca.

Questa skill copre un perimetro diverso e più largo: **il pacchetto intero**, quindi anche immagini, video, messaggio di apertura della chat, nomi e parametri della campagna. Dove il testo è in gioco, **chiama `collaudo-testi-adv` se è disponibile** e ne riporta l'esito, invece di rifare quel controllo a modo suo. Se non è disponibile, fa anche la parte testi con i propri criteri e **lo dichiara nel verbale**, così si sa che quel pezzo non è passato dallo strumento collaudato.

Prima volta che si usa questa skill da Cowork: leggere `collaudo-testi-adv` e, se i criteri si sovrappongono, togliere da qui i doppioni. La sovrapposizione non è un errore, ma è spreco.

## A cosa serve, in una riga

Fermare, prima che costi, tutto quello che può essere fermato gratis: una promessa che non reggiamo, una frase che Meta rifiuta, un titolo tagliato a metà nei Reels, un nome sbagliato che fa perdere i numeri, una campagna che parte attiva invece che in pausa.

## Le tre cose che la ricerca dice, e che governano il metodo

**1. Chi controlla non è chi ha scritto.** È il punto su cui tutte le fonti concordano: il controllo deve essere un passaggio separato con una firma sola, non una riletta veloce di chi ha appena finito. In pratica, per noi: questa skill parte **in una sessione pulita**, legge il pacchetto come se non l'avesse mai visto, e non ha memoria di perché una frase è stata scritta così. Se una scelta non si capisce dal pacchetto, è un difetto del pacchetto.

**2. Un controllo è un sistema, non una scorsa.** La differenza fra "qualcuno ha controllato?" e "quali righe sono pronte, quali sono bloccate, e cosa esattamente va corretto". L'esito deve essere una lista di righe, non un giudizio.

**3. Gli errori nascono agli incroci.** Non dentro un pezzo, ma fra un pezzo e l'altro: la creatività giusta attaccata al gruppo sbagliato, il nome che non corrisponde al blocco, il video che promette una cosa e la chat ne fa un'altra. **Per questo il collaudo guarda le corrispondenze, non solo i contenuti.** È la parte che un rilettura distratta non fa mai.

E una regola pratica: **si controlla l'anteprima, non l'editor.** Un titolo che sta bene mentre lo si scrive può essere tagliato a metà nei Reels.

## Prima di cominciare — leggi sempre

1. `inserzioni/<settore>/<blocco>.md` — il pacchetto da collaudare.
2. `settori/<settore>.md` — **la colonna "sì"**. È la fonte di verità sulle promesse.
3. `angoli/<settore>.md` — l'angolo in campo, per verificare che il pacchetto dica quello e non altro.
4. `voce/<settore>/` — per verificare che i ganci vengano davvero da lì.
5. `.agents/customer-language.md` — parole da usare e da evitare.
6. `regole-adv.md`: §5.1, §8 (i nomi), §18, §20, §23, §26.
7. I file prodotti: copioni, immagini, video.

Dichiara versione e data di ogni file letto. **Se manca uno dei primi tre, il collaudo non si fa**: senza scheda e senza angolo non c'è niente contro cui controllare.

## Cosa entra e cosa esce

**Entra:** settore e blocco. Più i file prodotti, se ci sono già.

**Esce:** `collaudi/<settore>/<blocco>-<data>.md` — il verbale, secondo `references/verbale.md`, con:
- **l'esito**: VERDE, GIALLO o ROSSO;
- una riga per ogni rilievo, con gravità, posizione e **la correzione già scritta**;
- cosa non è stato possibile controllare.

In chat: l'esito in una riga, i rilievi rossi, e cosa serve per passare.

### Cosa vogliono dire i tre esiti

| Esito | Vuol dire | Cosa succede |
|---|---|---|
| **VERDE** | Nessun rilievo grave. Si può produrre e caricare | Il pacchetto va alla scrittura sicura su Meta, sempre in pausa |
| **GIALLO** | Rilievi medi: qualcosa è debole o non verificabile, ma niente è pericoloso | **Decide Ivan.** La skill non promuove da sola un giallo a verde |
| **ROSSO** | Almeno un rilievo grave | Si ferma. Si corregge e si ricollauda |

**Un rilievo grave da solo fa rosso.** Non si fa la media.

---

## I sette controlli

Si fanno in quest'ordine: i primi fermano tutto, gli ultimi costano solo tempo.

### 1 — Le promesse (grave)

Per ogni frase del pacchetto che promette qualcosa — in un testo, in un titolo, in un copione, su un'immagine, nel messaggio di apertura, nella prima risposta di ARYA:

- **Sta nella colonna "sì" della scheda settore?** Se no: **rosso**. Non "quasi", non "in sostanza": la riga deve esserci.
- **La prova citata è nella forma ammessa?** Nome del cliente solo con consenso scritto registrato nella scheda. Altrimenti forma anonima, quella scritta nella scheda. Nome senza consenso: **rosso**.
- **I numeri sono misurati, e ancora misurati?** Un numero senza fonte o non più aggiornato: **rosso**.
- **Nessun "presto", "a breve", "stiamo per".** Una capacità futura non si promette.

Nel verbale, ogni promessa va scritta accanto alla riga che la autorizza. È il controllo che tiene insieme §23 e la normativa europea.

### 2 — Le regole di Meta (grave)

- **Attributi personali.** Per ogni frase: togli il nome del prodotto e rileggi. Descrive cosa offriamo, o dice al lettore qualcosa su di lui? Per noi il rischio è la difficoltà economica — "stai perdendo soldi", "la tua azienda non regge", "sei in difficoltà". La forma interrogativa non salva.
- **Promesse esagerate**: risultati garantiti, guadagni, tempi certi.
- **Coerenza fra inserzione e destinazione.** Meta controlla anche dove si arriva: se l'inserzione promette una cosa e la prima risposta di ARYA ne fa un'altra, è un problema di regolamento oltre che di fiducia.
- **La prima risposta di ARYA dichiara che risponde una macchina**, al primo contatto e in italiano semplice. È l'articolo 50 del regolamento europeo sull'AI, in vigore dal 2 agosto 2026: se manca, **grave**.
- **Nessuna finta conversazione** presentata come vera, nessuno schermo leggibile con dentro un dialogo inventato.
- **Nessun logo, marchio o volto** dentro le immagini generate.

### 3 — La lingua (medio, grave se ricorrente)

- Il **test della recensione** su ogni frase pubblicata: la scriverebbe un cliente?
- Nessuna parola della lista "da evitare": *soluzione*, *innovativo*, *trasformazione*, *intelligenza artificiale*, e le altre.
- I ganci **vengono davvero da una frase della voce**, citata nel pacchetto. Un gancio senza frase citata è un gancio inventato: **medio**, e se sono tutti così **grave**.
- Nessun termine del registro istituzionale LML: qui vince la lingua del cliente.
- Nessuna sigla non spiegata.

### 4 — Le misure (medio, grave se il messaggio sparisce)

- Testo principale: il messaggio sta **nei primi 125 caratteri**?
- Il gancio scritto **regge a 40 caratteri** (Reels)?
- Titolo **sotto i 27**?
- Video: **15-25 secondi**, gancio nei primi 2, **niente marchio nei primi 3**, sottotitoli incisi.
- Immagini: nel verticale, niente sopra il 14% e **niente sotto il 35%**; niente di importante fuori dall'80% centrale in larghezza.
- Le parole scritte dentro le immagini sono corrette lettera per lettera.

**Il controllo vero si fa sull'anteprima di ogni posizione**, non nell'editor. Se l'anteprima non è disponibile in questa sessione, si scrive in "cosa non ho potuto controllare" e si chiede a Ivan di guardarla in Gestione inserzioni.

### 5 — Le corrispondenze (grave)

È il controllo che nessuno fa e che fa perdere i numeri.

- Il **nome del blocco** è lo stesso in: coda degli angoli, pacchetto, nome campagna, nome gruppo, nome di ogni inserzione, messaggio di apertura della chat, nomi dei file. Uno diverso: **grave**.
- I nomi seguono il formato della §8.
- Ogni creatività del blocco porta **lo stesso angolo**. Se una dice un'altra promessa, non è una variante: è un secondo angolo infilato dentro, e rovina il blocco. **Grave.**
- Il **pulsante** è "Invia messaggio" e la destinazione è WhatsApp.
- Il **messaggio di apertura** e la **prima risposta di ARYA** combaciano.
- Il brief di produzione e quello che è stato prodotto corrispondono.

### 6 — I parametri della campagna (grave)

Se il pacchetto arriva con i parametri pronti per Meta:

- **Stato: in pausa.** Attiva: **rosso**, sempre.
- Account: quello di LML, non un altro.
- Budget: **entro 10 € al giorno**, entro i 300 € al mese complessivi.
- Un angolo per gruppo. Pubblico largo.
- Dichiarazione europea di chi paga e chi beneficia: presente.
- **Massimo due campagne attive** in tutto (§0.1). Se questa sarebbe la terza: **rosso**.

### 7 — I cancelli ancora aperti (grave)

- La scheda settore è ancora **CONFERMATA**? Se è tornata BOZZA mentre il pacchetto veniva scritto, la promessa potrebbe non reggere più.
- Chi risponde ai contatti, e in quali fasce? Se non c'è risposta, la campagna produrrebbe contatti che nessuno lavora: **grave** (§11, §26).
- La destinazione WhatsApp è provata?

---

## La prova a voce — facoltativa, per passare da giallo a verde

Con 10 € al giorno, la spesa impiega tre settimane a dire se un gancio funziona. Una cosa più economica si può fare prima: **leggere il gancio e il titolo a cinque titolari del settore** — clienti, conoscenti, il fornitore di fiducia — e annotare tre cose: cosa hanno capito, cosa li ha infastiditi, quale parola avrebbero usato loro. Cinque persone non provano niente in senso statistico, ma bastano a scoprire l'equivoco grosso: la frase che sembra un'accusa, il termine che nel settore vuol dire un'altra cosa. Costa un'ora. Se il pacchetto è giallo per la lingua, l'esito della prova a voce va nel verbale ed è un elemento in più per la decisione di Ivan — non la sostituisce.

## Come si scrive un rilievo

Quattro campi, sempre. Un rilievo senza la correzione scritta non è un rilievo: è un'opinione.

| Campo | |
|---|---|
| **Dove** | il pezzo esatto: "C2, titolo" |
| **Cosa** | il problema, in una riga |
| **Gravità** | grave / medio / lieve |
| **Come si corregge** | il testo di sostituzione, scritto |

Per i rilievi gravi, sempre il prima e il dopo.

**Il collaudo non riscrive il pacchetto.** Propone, e la correzione la applica chi lo ha scritto. Serve a non perdere la separazione fra chi fa e chi controlla.

## Regole vincolanti

1. **Sessione pulita.** Il collaudo legge il pacchetto come se non l'avesse mai visto. Se una scelta non si capisce dal pacchetto, è un difetto del pacchetto.
2. **Un rilievo grave fa rosso.** Nessuna media, nessuna compensazione.
3. **La colonna "sì" è l'unica fonte di verità sulle promesse.**
4. **Non si promuove un giallo a verde.** Decide Ivan.
5. **Non si riscrive il pacchetto.** Si propongono le correzioni.
6. **Non si modifica `collaudo-testi-adv`.** Si chiama, se c'è, e si riporta il suo esito.
7. **Cosa non si è potuto controllare va scritto.** Un verbale che sembra completo e non lo è è peggio di nessun verbale.
8. **Il collaudo non pubblica e non tocca Meta.**
9. **Ogni ricollaudo è un verbale nuovo**, datato, non una modifica del precedente.

## Quando si fa

- **Sul pacchetto scritto**, prima di produrre video e immagini. È il momento che fa risparmiare di più: una promessa non ammessa scoperta qui costa zero, scoperta dopo costa una giornata di ripresa.
- **Sul pacchetto prodotto**, prima di caricare su Meta.
- **Di nuovo**, dopo ogni correzione.
- **Non serve** per una variante che cambia solo l'immagine di una creatività già verde: in quel caso si collauda la sola immagine e si scrive nel verbale che il resto è invariato.

## Dove si scrive

```
collaudi/
  rivenditori/
    B1-lunedi-mattina-2026-09-20.md
    B1-lunedi-mattina-2026-09-22.md   ← ricollaudo dopo le correzioni
```

Da Cowork si scrive direttamente; dalla chat si consegna il file. File di appoggio, rilettura, copia sul file buono.

## Cosa fa dopo, e chi

Con esito **verde**, il pacchetto va alla **scrittura sicura su Meta**, che crea tutto in pausa. Con **giallo**, torna a Ivan per la decisione. Con **rosso**, torna a chi lo ha scritto — il pacchetto inserzione, il copione o le tavole — con le correzioni già pronte.

Va segnalato subito in chat, non solo nel verbale: una promessa non ammessa che regge tutto il blocco (è una domanda per Roberto, non una correzione di testo); una scheda settore tornata BOZZA; una campagna che sarebbe la terza attiva; un rilievo che si ripete blocco dopo blocco, perché allora il problema non è il pacchetto ma una regola da chiarire a monte.
