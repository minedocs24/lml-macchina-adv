# Le attività programmate — quattro, non otto

**Versione 3.0 — 14 settembre 2026.**

**Cosa è cambiato rispetto alla 2.0:** le cadenze disponibili in Cowork sono soltanto **ogni ora, ogni giorno, giorni feriali, ogni settimana, manuale**. Non esistono cadenze mensili, trimestrali, né "primo lunedì del mese". Quattro delle otto attività precedenti servivano solo a dire "è passato abbastanza tempo?" — e quel controllo il direttore lo fa già nella sua tabella delle decisioni. Erano doppioni miei e sono state tolte.

**Le cadenze lunghe non stanno nello scheduler: stanno nel prompt.** L'attività parte ogni giorno e la prima cosa che fa è chiedersi se è il momento, guardando la data dell'ultimo file prodotto. Viene meglio: se un'esecuzione salta, quella dopo recupera invece di perdere il giro.

**Da verificare prima di lunedì:** le attività di Cowork su desktop girano solo se il computer è acceso e l'app è aperta. Se Cowork è disponibile anche da web, conviene creare le attività lì.

---

## Le quattro

| Attività | Cadenza | Ora | Quando accenderla |
|---|---|---|---|
| **Direttore** | giorni feriali | 8:00 | **adesso** |
| **Semaforo** | giorni feriali | 7:30 | il giorno in cui parte la prima campagna |
| **Report** | settimanale, lunedì | 9:00 | il giorno in cui parte la prima campagna |
| **Archivio** | settimanale, venerdì | 17:00 | quando cominciano ad arrivare contatti |

Il direttore chiama le skill al posto tuo: radar, voce, scheda settore, coda angoli, pacchetto, collaudo, lettura dei numeri, chiusura del mese. **Non serve un'attività per ogni skill.**

---

## Il blocco di apertura

Va incollato all'inizio di **ognuna** delle quattro, identico. Non è un riferimento: è testo da copiare, perché un'attività che parte a freddo non ha memoria di niente.

```
CONTESTO
Lavori sulla cartella OneDrive Company/Marketing/lml-adv/. È l'unica copia buona:
se ne trovi un'altra altrove, non lavorarci e segnalalo.

PRIMA DI QUALSIASI COSA, in quest'ordine:
1. Leggi regole-adv.md e .agents/product-marketing.md. Annota versione e data di
   entrambi: vanno scritte nel file che produci.
2. Riverifica a quali account risponde il connettore Meta (§24bis). Se risponde a
   un account inatteso, FERMATI: non fare altro, scrivi solo la segnalazione.
3. Leggi l'ultimo file prodotto da questa stessa attività. Se contiene già il
   lavoro di oggi, FERMATI: non rifarlo.

LIMITI CHE VALGONO SEMPRE
- Su Meta solo lettura. Nessuna creazione, modifica, pausa o attivazione, mai,
  per nessun motivo.
- Non approvare niente al posto di Ivan. Una proposta resta una proposta.
- Non modificare regole-adv.md, product-marketing.md, glossario.md,
  customer-language.md o CLAUDE.md: si propone, non si scrive.
- Non generare immagini né video: costano a ogni generazione.
- Non mandare niente a nessun cliente.
- Se una skill fallisce, fermati e scrivi cosa è andato storto. Non ripiegare su
  un'altra skill.

COME SI SCRIVE IN QUESTA CARTELLA
Scrivi prima su un file di appoggio, rileggilo per verificare che il contenuto sia
davvero quello, poi copialo sul file definitivo in una chiamata separata, e rileggi
ancora. In questa cartella è già successo che la scrittura dicesse "fatto" lasciando
il contenuto vecchio. Non fidarti del messaggio di successo.
Se non riesci a scrivere, NON eseguire il lavoro: scrivi solo cosa ti ha bloccato,
dove riesci. Un lavoro fatto e non salvato verrebbe rifatto uguale domani.
```

---

# 1 · Il direttore

**Giorni feriali, 8:00. Da accendere adesso. È l'unica che serve oggi.**

*[blocco di apertura]*

```
COMPITO
Usa la skill lml-direttore-adv.

PASSO 1 — SEI IN PAUSA?
Leggi numeri/direttore/da-rivedere.md.
Se contiene righe con data più vecchia di 3 giorni lavorativi, NON produrre niente
di nuovo. Scrivi solo: "in attesa che Ivan riveda [elenco]" e fermati qui.
Serve a non accumulare cinque lavori che nessuno ha aperto.
Se il file non esiste, crealo vuoto e vai avanti.

PASSO 2 — RICOSTRUISCI LO STATO
Guarda cosa c'è in radar/, voce/, settori/, angoli/, inserzioni/, collaudi/,
montaggi/, numeri/, e con quali date. Leggi le prime venti righe di ogni file di
stato: schede settore (BOZZA o CONFERMATA), coda degli angoli (quale angolo in
campo e da quando), ultimo verbale di collaudo.

PASSO 3 — DECIDI
Applica la tabella delle decisioni della skill, dall'alto. La PRIMA riga che
corrisponde decide. Le altre le annoti, non le esegui.

Le scadenze lunghe le calcoli tu dalle date dei file, non dal calendario
dell'attività:
- panoramica del radar più vecchia di 90 giorni → radar in modo Panoramica
- radar di un settore aperto più vecchio di 30 giorni → radar in modo Settore
- voce di un settore aperto più vecchia di 90 giorni → voce del settore
- oggi è il primo giorno lavorativo del mese → chiusura del mese
- l'ultima manutenzione mensile dell'archivio è del mese scorso → manutenzione
  mensile dell'archivio

LIMITE DI QUESTA ESECUZIONE
UNA SOLA skill che produce qualcosa di nuovo. I controlli in sola lettura sono
liberi. Se ne toccherebbero due, fai la prima e annota la seconda.

PASSO 4 — SCRIVI
File: numeri/direttore/AAAA-MM-GG.md
Tre sezioni, in quest'ordine, e niente altro:
  ## Cosa ho fatto
  ## Cosa aspetta Ivan
  ## Cosa ho annotato per la prossima volta

L'elenco per Ivan: massimo cinque righe, ordinate per quanto bloccano. Ogni riga
dice cosa si ferma senza quella risposta — non basta "serve la risposta su X".
Niente cose che Ivan ha già rifiutato.

PASSO 5 — AGGIORNA LA CODA DA RIVEDERE
Se hai prodotto qualcosa, aggiungi una riga a numeri/direttore/da-rivedere.md:
data, cosa hai prodotto, percorso del file. Le righe le cancella Ivan quando ha
guardato.

QUANDO NON SCRIVERE NIENTE
Se non c'era niente da fare e l'elenco per Ivan è vuoto, non scrivere il file e non
mandare niente. Un rapporto che arriva ogni mattina dicendo "tutto a posto" smette
di essere letto in due settimane.

VERIFICA FINALE
Rileggi il file scritto. Nella risposta dimmi: quale riga della tabella ha deciso,
quale skill hai eseguito, e quante righe ci sono nell'elenco per Ivan.
```

---

# 2 · Il semaforo

**Giorni feriali, 7:30. Da accendere il giorno in cui parte la prima campagna.**

*[blocco di apertura]*

```
COMPITO
Usa la skill lml-lettura-numeri-adv, semaforo mattutino.

Se non c'è nessuna campagna attiva, fermati subito: non scrivere niente e non
mandare niente.

Controlla queste cose, e segnala SOLO quelle che superano la soglia:
- spesa di ieri sopra 10 € su una campagna
- spesa del mese sopra 240 € (l'80% del tetto di 300 €)
- inserzioni ferme, rifiutate o in revisione da più di 24 ore
- frequenza sopra 3 (le creatività si stanno consumando)
- zero moduli compilati da 48 ore su una campagna attiva
- contatti nell'archivio senza risposta di ARYA da più di 2 ore in fascia lavorativa
- call fissate e non fatte, anche una sola
- contatti senza provenienza oltre il 10%
- tempo medio fra modulo compilato e primo messaggio di ARYA oltre i 30 minuti

Segnala anche quando MANCA qualcosa che doveva succedere: zero risultati da due
giorni su una campagna accesa è un allarme quanto una spesa fuori controllo.

COSA SCRIVERE
Solo se c'è almeno un allarme: numeri/semaforo/AAAA-MM-GG.md.
Per ogni allarme: cosa, il numero, e cosa fare in una riga.
In fondo, una riga sola con cosa hai controllato e stava bene.

QUANDO NON SCRIVERE
Se non c'è nessun allarme: non scrivere il file, non mandare niente, non dire
"tutto ok". Il silenzio è la risposta.

VERIFICA FINALE
Se hai scritto, rileggi il file e riporta gli allarmi nella risposta, dal più
urgente.
```

---

# 3 · Il report

**Settimanale, lunedì 9:00. Da accendere il giorno in cui parte la prima campagna.**

*[blocco di apertura]*

```
COMPITO
Usa la skill lml-lettura-numeri-adv, report settimanale, formato §25.

Se non c'è stata nessuna campagna attiva nella settimana, scrivi due righe: spesa
zero e cosa sta bloccando la partenza. Non scrivere un report vuoto.

Prendi la spesa e i moduli compilati da Meta (sola lettura). Prendi validi, call
fissate, call fatte, motivi di scarto e tempi di risposta dall'archivio contatti.
Il conto lo fai tu incrociando i due.

Se l'archivio non è leggibile, il report si ferma ai moduli compilati e lo DICHIARI
IN CIMA, non in fondo.

REGOLE DEI NUMERI
- Ogni numero ha due confronti: settimana scorsa e riferimento. Senza, non entra.
- Se un numero non serve a decidere qualcosa, non va nel report.
- Sotto le 10 unità scrivi i numeri interi, non le percentuali: da 2 call a 3 non
  è "+50%", sono tre call.
- I tre fronti (prodotti ARYA, consulenza, personal brand) non si sommano mai:
  tre righe separate, nessun totale.
- Niente sigle non spiegate.
- Il numero della riga secca è il costo per call fissata, non per modulo compilato.

STRUTTURA, in quest'ordine
1. Una riga secca: bene o male, e perché
2. I numeri con i due confronti
3. Cosa è cambiato, e UNA spiegazione, quella più probabile, detta come ipotesi
4. Le proposte, ognuna con: cosa cambia, quanto costa, cosa succede se non lo faccio
5. Cosa non so — obbligatoria

COSA SCRIVERE
File: numeri/settimana/AAAA-MM-GG.md

DA SEGNALARE SUBITO NELLA RISPOSTA
- la spesa che si avvicina al tetto mensile
- il tempo di risposta oltre i 30 minuti (la §17 blocca gli aumenti di budget)
- il costo per modulo che scende mentre quello per contatto valido sale: vuol dire
  che Meta sta imparando a portare la gente sbagliata

VERIFICA FINALE
Rileggi il file. Nella risposta: la riga secca, il costo per call fissata, e quante
proposte hai fatto.
```

---

# 4 · L'archivio

**Settimanale, venerdì 17:00. Da accendere quando cominciano ad arrivare contatti.**

*[blocco di apertura]*

```
COMPITO
Usa la skill lml-archivio-contatti, manutenzione settimanale.

Se l'archivio non esiste, non è leggibile, o è vuoto, fermati e dillo in una riga.

Controlla:
- contatti fermi in "nuovo" o "in lavorazione" da più di 3 giorni
- call fissate e non fatte
- contatti senza provenienza: quanti, e in percentuale
- "non ora" con il ricontatto scaduto
- righe senza settore o senza volume di richieste: sono contatti che non si possono
  contare

NON cambiare nessuno stato. Gli stati li cambia chi li possiede. Se una riga sembra
sbagliata, la segnali.

La manutenzione mensile — doppioni, scadenza di conservazione, confronto fra i
numeri di Meta e quelli dell'archivio — NON la fai qui: la fa il direttore quando
si accorge che è passato un mese.

COSA SCRIVERE
Solo se c'è qualcosa da sistemare: numeri/archivio/AAAA-MM-GG.md, con una riga per
problema e cosa fare.

QUANDO NON SCRIVERE
Se è tutto in ordine, non scrivere niente.

DA SEGNALARE SUBITO
Contatti senza provenienza oltre il 10%: è un problema tecnico, non un caso.

VERIFICA FINALE
Se hai scritto, rileggi e riporta i problemi nella risposta.
```

---

# Il file che tieni tu

`numeri/direttore/da-rivedere.md` è l'unica cosa che richiede un tuo gesto, e dura dieci secondi.

```
# Da rivedere

| Data | Cosa | File |
|---|---|---|
| 2026-09-15 | scheda settore e-commerce | settori/ecommerce.md |
```

Il direttore aggiunge una riga ogni volta che produce qualcosa. **Tu cancelli le righe che hai guardato.** Se una riga resta lì più di tre giorni lavorativi, il direttore smette di produrre e aspetta.

Senza questo meccanismo, in una settimana ti ritrovi cinque schede fatte e nessuna letta — e la sesta sarà costruita su un errore delle prime.

---

# Cosa non va MAI in un'attività programmata

- Qualunque scrittura su Meta: creare, modificare, mettere in pausa, attivare.
- L'approvazione di un collaudo giallo.
- La conferma di una scheda settore.
- La modifica di un documento di riferimento.
- La generazione di immagini o video.
- L'invio di qualsiasi cosa a un cliente.
- Il cambio di uno stato nell'archivio contatti.

---

# Come si capisce, fra due settimane, se funzionano

1. **Il direttore ha scritto "niente da fare" tre volte di fila?** La tabella delle decisioni è tarata male, o la catena è ferma per un motivo che non vede.
2. **Il semaforo ha mandato allarmi che non erano allarmi?** Le soglie vanno alzate, o si smetterà di leggerlo.
3. **L'elenco "cosa aspetta Ivan" è sempre lo stesso?** Il problema non è l'automazione: è che a quelle domande non risponde nessuno.
4. **`da-rivedere.md` è sempre pieno?** Il direttore produce più di quanto qualcuno riesca a guardare: va rallentato a settimanale.
