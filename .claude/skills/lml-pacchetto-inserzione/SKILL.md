---
name: lml-pacchetto-inserzione
description: Trasforma un angolo in campo della coda LML in un pacchetto pronto da produrre e pubblicare — ganci video e ganci testo separati, testo principale nei primi 125 caratteri, titolo breve, pulsante, messaggio di apertura della chat WhatsApp, nome della campagna e delle inserzioni, brief di produzione — per 3-4 creatività dello stesso angolo. Usa SEMPRE questa skill quando l'utente chiede di scrivere un'inserzione, un testo pubblicitario, un gancio, un titolo, "cosa scriviamo nell'inserzione", "preparami le creatività", "il testo per la campagna", "il messaggio che vede quando apre WhatsApp", oppure quando la coda degli angoli ha appena messo un angolo in campo — anche se non nomina la skill e dice solo "scriviamo l'inserzione per i rivenditori". È il quinto anello della catena pubblicitaria LML: dopo la coda degli angoli, prima della produzione video/grafica e del collaudo. Non produce immagini né video, non tocca Meta.
---

# Pacchetto inserzione — dall'angolo al testo pronto

**Versione 1.0 — 13 settembre 2026.** Scrive solo file nella cartella di lavoro. Non genera immagini o video: scrive i brief per chi li produce. Non tocca Meta. Ogni pacchetto passa dal collaudo prima di andare in produzione.

## A cosa serve, in una riga

La coda degli angoli decide **cosa dire**. Questa skill decide **come dirlo**, nei formati esatti che Meta accetta, con i vincoli di lunghezza reali e senza mai uscire dalle promesse ammesse.

## I quattro fatti tecnici che governano la scrittura

Verificati a settembre 2026. Vanno riverificati ogni sei mesi: Meta li cambia.

**1. Si scrive per 125 caratteri, non per 2.200.** Il testo principale viene tagliato con "Altro" intorno ai 125 caratteri sul telefono. Meta accetta molto di più e non rifiuta niente — semplicemente tronca. Chi apre "Altro" è una minoranza piccolissima. **Quindi i primi 125 caratteri sono l'inserzione intera.** Il resto è un premio per chi tocca.

**2. Il titolo va sotto i 27 caratteri.** Meta dice 40, ma sul telefono il taglio arriva prima; la guida ufficiale per il feed raccomanda 27. Sotto i 27 si è sicuri ovunque.

**3. Si scrive per il posto più stretto.** La stessa creatività finisce nel feed, nelle storie e nei Reels. Nei Reels lo spazio è molto minore (circa 40-70 caratteri di testo, titoli di pochissime parole). Se si scrive per il feed e basta, nei Reels il messaggio sparisce. **Regola: il gancio deve reggere anche a 40 caratteri.**

**4. Nelle storie e nei Reels comanda quello che è scritto sopra l'immagine, non il campo di testo.** Il gancio visivo è il gancio.

## La regola che fa rifiutare più inserzioni di tutte

Meta ha una regola, gli "attributi personali", che vieta di far credere al lettore che sappiamo qualcosa di personale su di lui. È fra i motivi di rifiuto più comuni, e l'applicazione nel 2026 è automatica e severa.

Il test, semplice: **togli il nome del prodotto e leggi la frase. Descrive quello che offriamo, o dice al lettore qualcosa su di lui?**

| Rischioso | Sicuro |
|---|---|
| "Stai perdendo clienti perché non rispondi?" | "Le chiamate perse costano clienti. Ecco come rispondere sempre." |
| "Il tuo studio è in difficoltà?" | "Segreteria che risponde anche quando lo studio è chiuso." |
| "Sei un rivenditore che non ce la fa più?" | "Per rivenditori con più richieste che tempo." |

La domanda non è una scappatoia: "Hai problemi con il telefono?" resta rischiosa. E la parola "tu" non è vietata: lo diventa quando è attaccata a una difficoltà o a una condizione.

**Per noi il punto delicato è la difficoltà economica.** "Perdi soldi", "stai buttando fatturato", "la tua azienda non regge" sono la versione nostra di quella regola. Il dolore si racconta **in terza persona o come situazione**, mai come diagnosi sul lettore. E questo si sposa con la voce: il cliente in una recensione racconta un fatto, non si fa la diagnosi.

## Prima di cominciare — leggi sempre

1. `angoli/<settore>.md` — **l'angolo in campo, con il nome del blocco.** Se non c'è un angolo in campo, fermati.
2. `settori/<settore>.md` — CONFERMATA. La colonna "sì", le prove, la forma anonima del caso, il prezzo da dire, le tre domande della chat.
3. `voce/<settore>/` — le frasi esatte. **I ganci si costruiscono da qui, non si inventano.**
4. `.agents/customer-language.md` — parole da usare e da evitare.
5. `regole-adv.md`: §5.1, §8 (il formato dei nomi), §18, §20, §23.
6. `.agents/glossario.md` — come si chiamano le cose quando si parla al cliente.

Dichiara versione e data di ogni file letto.

## Cosa entra e cosa esce

**Entra:** settore e nome del blocco.

**Esce:** `inserzioni/<settore>/<blocco>.md` — il pacchetto completo, secondo `references/modello-pacchetto.md`: 3-4 creatività, il messaggio di apertura della chat, i nomi, i brief di produzione, e la scheda di approvazione con le tre cose.

Il pacchetto **non va in produzione finché non passa il collaudo** e non riceve il sì di Ivan.

---

## Passo 1 — Le tre parti che non vanno confuse

Ogni creatività ha **tre ganci diversi**, e sono davvero diversi:

| Gancio | Dove | Vincolo | Chi lo incontra |
|---|---|---|---|
| **Gancio visivo** | primi 3 secondi del video, o l'immagine | si capisce **senza audio** | chi scorre |
| **Gancio scritto** | prime parole del testo principale | dentro i primi 125 caratteri, regge anche a 40 | chi legge |
| **Titolo** | sotto la creatività | sotto i 27 caratteri | chi ha già guardato |

Sono tre porte sulla stessa stanza. Chi guarda il video non legge il testo; chi legge il testo può non aver guardato. **Nessuno dei tre può dipendere dagli altri per avere senso.**

## Passo 2 — Costruire i ganci dalla voce

Per ogni creatività, si parte da **una frase della scheda voce**, casella "Momento" o "Dolore", e si trasformano:

- **Gancio visivo:** la scena di quella frase. Non la frase detta, la scena vista. Se la frase è "il lunedì mattina trovo dieci chiamate perse", il gancio visivo è lo schermo del telefono con le chiamate perse, oppure Ivan che lo dice guardando in camera nei primi due secondi. Si scrive cosa si vede, non cosa si dice.
- **Gancio scritto:** la stessa frase, ripulita e portata sotto i 40 caratteri. Mantiene le parole del cliente. Passa il test degli attributi personali.
- **Titolo:** la promessa, non il problema. Sotto i 27 caratteri.

**Ogni gancio cita la frase da cui viene**, con la fonte. È il controllo che nessuno stia inventando.

## Passo 3 — Il testo principale

Struttura in quattro pezzi, e solo il primo è garantito:

1. **Prime 125 battute:** il momento e la promessa. Deve funzionare da solo. Se qui non c'è tutto, l'inserzione non esiste.
2. **Dopo il taglio:** la prova, nella forma ammessa dalla scheda (nome solo con consenso, altrimenti forma anonima).
3. **La qualificazione discreta:** una riga che fa capire a chi non è adatto di non scrivere (es. il volume di chiamate, il tipo di attività). Risparmia contatti scartati.
4. **L'invito:** cosa succede se scrive. Deve corrispondere a quello che accade davvero: si apre WhatsApp e risponde ARYA.

Regole di scrittura:
- **Frasi corte.** Il test resta quello delle regole: la scriverebbe un cliente in una recensione?
- **Niente parole della lista "da evitare".** Nessun cliente contento scrive *soluzione*, *innovativo*, *trasformazione*, *intelligenza artificiale*.
- **Numeri solo se misurati** e solo se continuano a essere misurati.
- **Il prezzo si dice** se la scheda settore lo prevede: è una qualificazione gratuita.
- **Niente promesse fuori dalla colonna "sì"**, nemmeno accennate, nemmeno come "presto".

Si scrivono **due versioni del testo principale** per ogni creatività: una corta (sotto 125) e una lunga. Meta permette di caricarle entrambe.

## Passo 4 — Il pulsante e il messaggio di apertura della chat

La destinazione è WhatsApp. Due cose precise:

**Il pulsante è "Invia messaggio".** Non "Scopri di più", non "Contattaci": il pulsante deve dire quello che succede davvero quando lo si tocca, altrimenti si paga un clic e si perde la persona.

**Il messaggio di apertura** è il testo che il cliente si trova già scritto in WhatsApp prima di premere invio. È il pezzo più trascurato e conta moltissimo:
- deve essere **scritto dal cliente, in prima persona**, non da noi: *"Vorrei capire come rispondere alle chiamate quando siamo chiusi"*;
- deve dire **da quale settore e da quale blocco** arriva, in modo naturale, così ARYA parte già informata e i numeri tornano attaccati al blocco;
- deve essere corto: se il cliente deve leggere tre righe prima di premere invio, non preme;
- **non deve promettere niente** che non accada subito dopo.

Nel pacchetto si scrive anche **la prima risposta di ARYA** (che configura la skill dell'assistente, non questa), perché il messaggio di apertura e la prima risposta devono combaciare: è il primo momento in cui il cliente verifica se abbiamo detto la verità. Va incluso l'avviso privacy, con il link.

**E va detto che risponde una macchina.** Dal 2 agosto 2026 l'articolo 50 del regolamento europeo sull'AI obbliga chi mette a disposizione un assistente conversazionale a renderlo riconoscibile **al primo contatto**, non in una pagina collegata. La prima risposta di ARYA lo dice in una riga, in italiano semplice: *"Sono l'assistente automatico di LML: rispondo io, e se serve ti passo a una persona."* Vale anche come prova del prodotto: il cliente sente esattamente quello che comprerebbe.

**Attenzione a non confondere due cose.** Dichiarare la macchina **nella chat** è un obbligo. Mettere "intelligenza artificiale" **nell'inserzione** è una scelta, e le prove dicono di non farla: uno studio su oltre mille persone (Cicek, Gursoy e Lu, *Journal of Hospitality Marketing & Management*, 2024, sei esperimenti su otto categorie) ha trovato che la sola parola "intelligenza artificiale" nella descrizione di un prodotto **abbassa la fiducia e l'intenzione d'acquisto**, e l'effetto è più forte quando l'acquisto è percepito come rischioso — che è il nostro caso. È la conferma scientifica della regola di `customer-language.md`: nell'inserzione si descrive quello che fa, non con cosa è fatto.

## Passo 5 — I nomi

Secondo il formato della §8, e sempre con il nome del blocco dentro. Serve a far tornare i numeri attaccati all'angolo:

- **Campagna:** `ARYA - Call fissate - <Settore> - <mese anno>`
- **Gruppo:** `<Settore> - Italia - Largo - B<n>-<nome-angolo>`
- **Inserzione:** `B<n>-<angolo>-<C1|C2|C3>-<formato>-<gancio in due parole>`

Esempio: `B1-lunedi-mattina-C2-video-chiamate-perse`.

## Passo 6 — I brief di produzione

Uno per creatività, per chi la realizza. Non è la creatività: è l'ordine di lavoro.

**Per un video** (va alla skill del copione e poi al montaggio): durata 15-25 secondi, il gancio visivo nei primi 2 secondi, cosa si vede blocco per blocco, cosa si sente, se c'è la faccia di Ivan o la registrazione di ARYA, i sottotitoli (obbligatori: si guarda senza audio), il formato verticale 9:16 e il ritaglio 4:5 per il feed, e **la zona di sicurezza**: niente di importante nel 10% in alto e in basso, che l'interfaccia copre.

**Per una tavola statica** (va alla skill delle tavole, variante pagina LML): cosa dice, quanta scritta (poca: le immagini cariche di testo vengono mostrate meno), formati 1:1 e 9:16, la firma LML e non quella del profilo personale di Ivan.

**Per una registrazione di ARYA:** cosa chiede il cliente finto, cosa risponde ARYA, quanto dura, e il fatto che va registrata da una conversazione **vera** o dichiaratamente dimostrativa. Mai finta e spacciata per vera (§23).

**Nel brief va sempre scritto che cosa questa creatività prova** rispetto alle altre del blocco — l'esecuzione, non l'angolo.

## Passo 7 — La scheda di approvazione

Il pacchetto chiude con la scheda per Ivan: cosa cambia, quanto costa (tempo di produzione e budget giornaliero), cosa succede se non lo faccio. Più:
- l'elenco di cosa serve produrre, e da chi;
- il collaudo: passato / da fare;
- le promesse usate, con accanto la riga della colonna "sì" che le autorizza.

---

## Regole vincolanti

1. **Solo da un angolo in campo**, di una scheda CONFERMATA. Mai a memoria.
2. **Le tre creatività del blocco sono varianti dello stesso angolo.** Cambia l'esecuzione, non la promessa.
3. **Ogni gancio cita la frase della voce da cui viene.**
4. **125 caratteri e 27 caratteri** sono i vincoli di progetto. Il gancio regge anche a 40.
5. **Test degli attributi personali** su ogni frase: togli il prodotto, rileggi. Se dice qualcosa sul lettore, riscrivi.
6. **Niente fuori dalla colonna "sì".**
7. **Il pulsante dice quello che succede.** "Invia messaggio", per WhatsApp.
8. **Il messaggio di apertura è del cliente, in prima persona, corto, e porta il nome del blocco.**
9. **Nessuna produzione prima del collaudo e del sì di Ivan.**
10. **Non si genera nessuna immagine o video qui.** Si scrivono i brief.

## Cadenza

Una volta per blocco, quando la coda mette un angolo in campo. Si riapre a metà blocco **solo** se il collaudo o Meta bocciano una creatività, o se le creatività si consumano (frequenza sopra 3, §20) e servono varianti nuove dello stesso angolo.

## Dove si scrive

```
inserzioni/
  rivenditori/
    B1-lunedi-mattina.md
    B2-ordine-nel-gestionale.md
```

Un file per blocco, datato dal blocco, mai sovrascritto: serve a rileggere cosa esattamente aveva detto un angolo che ha funzionato. Da Cowork si scrive direttamente; dalla chat si consegna il file. File di appoggio, rilettura, copia sul file buono.

## Cosa fa dopo, e chi

Il **collaudo** legge il pacchetto e dà verde, giallo o rosso. La **skill del copione video** e la **skill delle tavole** prendono i brief e producono. Il **montaggio** finisce i video. La **scrittura sicura su Meta** crea campagna, gruppo e inserzioni con questi nomi esatti, in pausa. La **lettura dei numeri** riporta gli esiti nella coda, attaccati al blocco.

Va segnalato subito in chat: un gancio che funzionerebbe ma richiede una promessa non ammessa (è una domanda per Roberto, non un problema di scrittura); una frase della voce troppo forte per gli attributi personali e che non si riesce a riscrivere senza perderla; un caso in cui il consenso al nome cambierebbe molto la forza del pacchetto.
