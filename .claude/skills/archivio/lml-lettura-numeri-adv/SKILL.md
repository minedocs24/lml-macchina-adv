---
name: lml-lettura-numeri-adv
description: Legge i numeri delle campagne pubblicitarie di LML Technologies fino al contatto e alla call — unendo la spesa presa da Meta e gli esiti presi dall'archivio contatti — e produce il semaforo mattutino, il report del lunedì e la lettura di fine blocco, nel formato delle regole LML, con i due confronti obbligatori e la sezione "cosa non so". Usa SEMPRE questa skill quando l'utente chiede come vanno le campagne, "quanto ci costa un contatto", "il report", "come è andato il blocco", "stiamo andando bene?", "quanto abbiamo speso", "il semaforo", oppure quando parte l'attività programmata del report settimanale o un blocco finisce. NON sostituisce la skill generica performance-report del pacchetto marketing, che resta invariata: quella non conosce i riferimenti italiani né le regole LML. È il dodicesimo e ultimo anello della catena pubblicitaria LML: chiude il cerchio riportando l'esito nella coda degli angoli.
---

# Lettura dei numeri — fino al contatto, non fino al clic

**Versione 1.0 — 13 settembre 2026.** Sola lettura su Meta. Scrive solo file. Non cambia budget, non mette in pausa, non attiva.

## Una precisazione

Nel pacchetto marketing preso dal web esiste `performance-report`, una skill generica di rendicontazione. **Non va modificata.** Non è stata duplicata perché non serviva: il suo scheletro (sintesi, tabella dei numeri, cosa ha funzionato, cosa no, proposte) è utile e l'ho tenuto, ma i suoi contenuti — metriche da e-commerce, ritorno sulla spesa, obiettivi trimestrali — non c'entrano con noi. Quello che ci serve è il formato della §25 e i riferimenti italiani della §17, che quella skill non conosce.

## A cosa serve, in una riga

Dire se stiamo andando bene o male, e perché, con numeri che arrivano fino alla **call fissata** — non al clic, non alla chat.

## La regola che decide tutto: qual è il numero che conta

Tutte le fonti sulle inserzioni verso WhatsApp dicono la stessa cosa: **un clic non è niente.** Il conteggio che vale è la **conversazione avviata**, cioè quando la persona preme invio. E nemmeno quella basta per noi.

La scala, dal meno al più utile:

| Numero | Cosa dice | Quanto vale per noi |
|---|---|---|
| Clic | Quante persone hanno toccato il pulsante | **Quasi niente.** Sulle inserzioni verso WhatsApp le percentuali di clic sono gonfiate: si tocca per curiosità |
| Conversazioni avviate | Quante hanno davvero scritto | È il primo numero vero. Si legge da Meta |
| **Risposte alla prima domanda** | Quante hanno risposto ad ARYA | **Misura se l'inserzione e la chat combaciano.** Sotto il 25% il messaggio di apertura non corrisponde a quello che l'inserzione prometteva |
| **Contatti validi** | Quanti erano clienti veri (§10) | Il numero che separa il volume dal valore |
| **Call fissate** | L'obiettivo dichiarato della campagna | **È il numero che conta.** Tutto il resto è diagnosi |

**Il costo per call fissata è la riga secca del report.** Il costo per chat è una diagnosi: serve a capire *dove* si rompe, non a dire se va bene.

Il caso dell'agenzia lo dimostra: 4,51 € per contatto suonava ottimo, ma il costo per contatto buono era **33 €**. Sette volte tanto. Chi guardava il primo numero stava guardando la cosa sbagliata.

## Quando non si conclude niente

È la parte che fa risparmiare più soldi, ed è la più facile da ignorare.

- **Mai prima di 7 giorni pieni e 50 conversazioni** (§26). Non 7 giorni *o* 50: tutti e due.
- I risultati fanno **corse strane**: tre giorni fiacchi e poi un giorno buono. Una settimana non è una tendenza.
- Con 10 € al giorno servono circa tre settimane per arrivare a 50. **Se a 21 giorni non ci siamo, si giudica lo stesso e si scrive che il giudizio è debole.**
- **Una variazione percentuale su numeri piccoli non è un risultato.** Da 2 call a 3 call non è "+50%": sono tre call. La regola pratica: **sotto le 10 unità si scrivono i numeri interi, non le percentuali.**
- Un peggioramento va confrontato con quanto è cambiata la spesa. Se la spesa è salita del 40% e i contatti sono rimasti uguali, è un segnale; se sono saliti del 35%, non è successo niente.

Su questo la skill deve essere scomoda: **dire "non lo so ancora" è una risposta**, e la §25 la richiede in una sezione apposta.

## Prima di cominciare — leggi sempre

1. **Riverificare gli account del connettore.**
2. `regole-adv.md`: §17 (riferimenti italiani), §20 (consumo delle creatività), §25 (formato del report), §26, §27 (tetto per cliente), §32 (chiusura del mese).
3. `angoli/<settore>.md` — il blocco in campo e il registro dei blocchi precedenti.
4. L'**archivio contatti** — il foglio di riepilogo per blocco.
5. `montaggi/<settore>/` — quando è partito il blocco.

Dichiara versione e data di ogni file letto.

## Da dove vengono i numeri

**Da Meta, in sola lettura:** spesa, impressioni, clic, conversazioni avviate, costo per conversazione, frequenza (quante volte la stessa persona ha visto l'inserzione).

**Dall'archivio contatti:** validi, call fissate, call fatte, attivazioni, motivi di scarto, tempi di risposta, contatti senza provenienza.

**Il conto lo fa questa skill**, incrociando i due. Meta non sa quali contatti valevano: glielo diciamo noi (§24: i dati escono da Meta).

**Se l'archivio non è leggibile**, il report si ferma alle conversazioni e **lo dichiara in cima**, non a piè di pagina.

## I tre prodotti

### 1. Il semaforo — ogni mattina lavorativa

Non è un report. È un allarme: **parla solo se c'è un problema.** Una mail che arriva tutti i giorni e dice sempre "tutto ok" smette di essere letta.

Controlla:
- spesa di ieri contro i tetti (10 € al giorno, 300 € al mese);
- inserzioni ferme, rifiutate o in revisione;
- **frequenza sopra 3** — è il segnale che le creatività si stanno consumando;
- chat senza risposta, e da quanto;
- **call fissate e non fatte** — il caso peggiore: contatto pagato, tempo speso, e la persona si è sentita dare buca;
- contatti senza provenienza: se sono oltre il 10%, **è un problema tecnico**, non un caso.

Avvisa anche quando **manca qualcosa che doveva succedere**: zero conversazioni da 48 ore su una campagna attiva è un allarme quanto una spesa fuori controllo.

### 2. Il report del lunedì

Formato §25, cinque parti, in quest'ordine:

**1. Una riga secca.** Bene o male, e perché. Il numero è il costo per call fissata.

**2. I numeri, con i due confronti obbligatori.** Settimana scorsa **e** riferimento italiano. Un numero senza termine di paragone non entra. E se un numero non serve a decidere qualcosa, non va nel report.

**3. Cosa è cambiato, e la spiegazione più probabile.** Una sola, quella più probabile, detta come ipotesi.

**4. Le proposte**, ognuna con: cosa cambia, quanto costa, cosa succede se non lo faccio.

**5. Cosa non so.** Obbligatoria. Dati mancanti, numeri troppo piccoli, cose non verificabili.

**I tre fronti non si sommano mai** (prodotti ARYA, consulenza, personal brand). Tre righe separate, mai un totale.

**Niente sigle non spiegate.** Mai.

### 3. La lettura di fine blocco

Quando un blocco arriva a 7 giorni pieni e 50 conversazioni — o a 21 giorni.

Restituisce alla coda degli angoli **una riga sola**: l'angolo ha funzionato, non ha funzionato, o il giudizio è debole. Con i numeri e la lettura più probabile: era il momento? la promessa? l'esecuzione?

**La distinzione che conta**, e che la coda degli angoli usa per decidere:

| Cosa si vede | Cosa vuol dire |
|---|---|
| Poche conversazioni, costo alto per conversazione | **L'angolo non prende.** Cambia angolo |
| Tante conversazioni, poche risposte alla prima domanda | **L'inserzione e la chat non combaciano.** Stesso angolo, si sistema il messaggio di apertura |
| Tante conversazioni, tanti scarti | **L'angolo attira i clienti sbagliati.** Guarda i motivi di scarto: dicono se stringere il pubblico o il testo |
| Tanti validi, poche call | **Il problema è dopo**, nella chat o nell'agenda. Non è l'angolo |
| Tutto buono, poi peggiora dopo 10-14 giorni con frequenza alta | **Non è l'angolo: sono le creatività consumate.** Varianti nuove dello stesso angolo |

È la distinzione che evita l'errore più costoso: buttare un angolo buono perché l'esecuzione si era consumata.

## I riferimenti

Il termine di paragone ufficiale è la §17. Dove quella non copre le inserzioni verso WhatsApp, si usano gli intervalli di mercato, **marcandoli come stime esterne e non come nostri obiettivi**:

| Numero | Intervallo dichiarato dalle fonti | Nota |
|---|---|---|
| Costo per conversazione avviata | circa 1,50-8 € secondo il settore | Molto variabile per paese e settore. È un intervallo, non un bersaglio |
| Risposte alla prima domanda | sano fra 40% e 70% | Sotto il 25%: il messaggio di apertura non corrisponde all'inserzione |

**Il nostro bersaglio si calcola al contrario**, dai nostri conti: se una call su quattro diventa cliente e un cliente vale X, si ricava quanto possiamo pagare una call, e da lì quanto una conversazione. **Questo conto va fatto con Ivan una volta**, e poi diventa il riferimento vero. Finché non c'è, si usano gli intervalli di mercato e si dice che sono di mercato.

Il tetto per cliente resta quello della §27.

## Cosa entra e cosa esce

**Entra:** il periodo, oppure il blocco.

**Esce:**
- `numeri/semaforo/<data>.md` — **solo se c'è un allarme**;
- `numeri/settimana/<data>.md` — il report del lunedì;
- `numeri/blocchi/<blocco>.md` — la lettura di fine blocco, che va riportata nella coda degli angoli.

Modelli in `references/modelli.md`.

## Regole vincolanti

1. **Sola lettura su Meta.** Nessuna pausa, nessun cambio di budget, nessuna attivazione. Le proposte si scrivono; le esegue Ivan, o la skill di montaggio dopo il suo sì.
2. **Il numero che conta è il costo per call fissata.** Il resto è diagnosi.
3. **Due confronti su ogni numero**: settimana scorsa e riferimento. Senza, non entra.
4. **Mai giudicare prima di 7 giorni pieni e 50 conversazioni.** Un giudizio debole si dichiara.
5. **Sotto le 10 unità, numeri interi e non percentuali.**
6. **I tre fronti non si sommano mai.**
7. **"Cosa non so" è obbligatoria**, e sta nel report, non in fondo in piccolo.
8. **I numeri stimati si marcano come stime.** Quelli misurati vanno con la fonte.
9. **Non si dice che una modifica è stata applicata** senza averlo verificato con una lettura.
10. **Niente sigle non spiegate.**
11. **Non si modifica `performance-report`.**

## Cadenza

- **Semaforo:** ogni mattina lavorativa, solo se c'è un problema.
- **Report:** ogni lunedì.
- **Fine blocco:** quando il blocco matura.
- **Chiusura del mese:** il primo giorno lavorativo, formato §32, con il confronto fra costo per cliente e tetto della §27, i clienti ARYA persi (§28), e l'esportazione dei dati fuori da Meta (§24).

## Cosa fa dopo, e chi

La lettura di fine blocco torna nella **coda degli angoli**, che riordina. Le proposte vanno a Ivan. Se servono creatività nuove, il **pacchetto inserzione** riparte. Se cambia qualcosa sulla campagna, lo fa il **montaggio**, dopo il sì.

Va segnalato subito in chat, non solo nel report: la spesa che si avvicina al tetto mensile; la frequenza sopra 3; una call fissata e non fatta; il tempo di risposta oltre i 30 minuti, perché la §17 blocca gli aumenti di budget quando succede; contatti senza provenienza sopra il 10%; e il caso in cui il costo per chat scende mentre quello per contatto valido sale — è il segnale che Meta sta imparando a portare la gente sbagliata, e vuol dire che il ritorno dei contatti buoni non sta funzionando.
