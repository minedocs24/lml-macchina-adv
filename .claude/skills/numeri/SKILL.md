---
name: numeri
description: Reparto Numeri e conversione della macchina pubblicitaria di Arya. Ogni giorno legge in sola lettura la spesa da Meta (e da Google) e i contatti dal CRM LML, e scrive il semaforo solo se c'è un allarme; il lunedì scrive la lettura della settimana e aggiunge una riga a numeri/storico.csv, con i risultati per idea e per pezzo che tornano al Piano e alla Regia. Usala quando parte il giro dei numeri o quando qualcuno chiede "come vanno le campagne", "quanto ci costa un cliente", "il semaforo", "la lettura della settimana", "quanti contatti, demo, clienti", "quanto abbiamo speso". Non scrive mai su Meta né nel CRM, non cambia budget, non contatta nessuno e nei file mette solo conteggi e ID, mai dati di persone esterne.
---

# Reparto Numeri e conversione — quanto spendiamo e cosa torna, fino al cliente

Il numero che conta è **il costo per cliente** (tetto 600 €, decisione 1). Contatti e demo servono a capire dove si rompe.
Sola lettura ovunque: Meta, Google, CRM. Scrive solo file nella cartella `numeri/`.

## Quando si usa
- **Ogni giorno** (ritmo della settimana in CLAUDE.md): il **semaforo**. Parla solo se c'è un allarme.
- **Lunedì, per primo**: la **lettura della settimana** appena chiusa (da lunedì a domenica) e la riga in `numeri/storico.csv`.
  Osservatorio e Piano la leggono subito dopo per decidere cosa provare.
- **Primo lunedì del mese**: la lettura aggiunge i controlli del mese (passo 11).
- Quando lo fa partire il Direttore, o quando qualcuno chiede: "come vanno le campagne?", "quanto ci costa un cliente?",
  "il semaforo", "quanto abbiamo speso?", "quante demo questa settimana?".
- Se non c'è spesa attiva e non ci sono contatti nuovi: niente semaforo; il lunedì una lettura di due righe
  (spesa zero e cosa blocca la partenza), e la riga in storico con zeri.

## Cosa legge all'inizio
Sempre:
1. `CLAUDE.md`.
2. `conoscenza/apprendimenti.md`.
3. `regole/decisioni.md` (soprattutto 1, 5, 6, 7).
4. L'ultimo file datato in `numeri/` e le ultime 8 righe di `numeri/storico.csv`.

Poi, per questo reparto:
5. `regole/regole-adv.md` 3.0: §2 (tassi di riferimento), §3.1 (le due porte), §9 (budget e tetti), §10.1 (contatto valido),
   §11 (tempo di risposta, stati), §13 ("come ci hai conosciuto"), §17 e §17.1 (soglie, indizio o confermato), §18 (diagnosi),
   §25 (formato), §27 (tetti), §28 (clienti persi).
6. `numeri/collegamento-crm.md`: quali strumenti del CRM si usano in lettura, quali campi, come si leggono stati, canale e
   inserzione di provenienza, tempo di prima risposta, trattative, clienti e canoni. **È l'unica guida al CRM.**
   Se manca, o non dice dove sta un dato, quel dato va in "Cosa non so": non si indovina.
7. L'ultimo `piano/AAAA-MM-GG-piano-settimana.md` (budget e idee della settimana, e i contatori dei controlli di spesa:
   speso dall'ultimo controllo, data dell'ultimo aumento) e l'ultimo verbale di `campo/` (quali inserzioni sono in campo,
   con il loro ID, e a quale idea e pezzo corrispondono). Poi `regia/archivio-pezzi.md`.
8. **Meta, sola lettura**, account `lml-adv` (2214221312473862, regole §8). Se il connettore risponde con un account inatteso,
   la lettura si ferma e si segnala. Le campagne di consulenza (account Minedocs, fino a ottobre) sono un altro fronte:
   si leggono a parte e **non si sommano mai** ai prodotti.
9. **Google, sola lettura**, se c'è un collegamento (budget da novembre). Se non c'è, va in "Cosa non so".
10. **CRM LML** (connettore `lml-commerciale`), solo con gli strumenti di lettura indicati in `collegamento-crm.md`.

In ogni prodotto: versione e data dei file letti, e ora delle letture di Meta, Google e CRM.

## Cosa produce
Un file datato per prodotto, mai sovrascritto. Modelli completi in `references/modelli.md`.

**(a) `numeri/AAAA-MM-GG-semaforo.md`** — **solo se c'è almeno un allarme.** Se è tutto a posto non si scrive niente.
Per ogni allarme: cosa, il numero, la soglia, cosa si propone in una riga, chi decide. Ultima sezione: "Cosa non so".

| Controllo | Allarme se | Fonte della soglia |
|---|---|---|
| Tempo medio di prima risposta | sopra **30 minuti** (ieri o ultimi 7 giorni) | §17, §17.1: viene prima di tutte |
| Spesa di ieri | sopra **50 €** al giorno, o sopra il giornaliero deciso da Ivan nel piano della settimana | decisione 6 |
| Spesa del mese | sopra l'80% del budget del mese; allarme forte se lo supera | decisione 5 |
| Controllo a 500 € | speso dall'ultimo controllo (contatore del Piano) più la spesa dopo arriva a **500 €** | decisione 6, §17 |
| Stop | costo per cliente sopra **600 €** per **4 settimane di fila** (vedi passo 9) | decisione 6 |
| Aumento fuori regola | budget salito più del 20%, o prima di 2 settimane dall'ultimo aumento, o con costo per cliente sopra 600 € | decisione 6 |
| Contatti senza provenienza | oltre il 10% dei contatti degli ultimi 7 giorni (sotto i 10 contatti: anche uno solo) | skill di settembre |
| Nessun contatto | zero contatti nuovi da **48 ore** con spesa attiva | skill di settembre |
| Frequenza | sopra **3** su un'inserzione (le stesse persone l'hanno vista più di 3 volte: pezzo consumato) | §17 |
| Problema tecnico | inserzione rifiutata, oppure contatti contati da Meta che nel CRM non ci sono | §17.1 |
| Demo saltata | una demo fissata e non fatta, se il CRM lo registra | skill di settembre |

**(b) `numeri/AAAA-MM-GG-settimana.md`** — ogni lunedì, nel formato della §25, in quest'ordine:
1. **La riga secca**: stiamo andando bene o male, e perché. Il numero è il costo per cliente; finché non ci sono clienti,
   il costo per demo (tetto 500 €) e per contatto valido (tetto 50 €), detto chiaramente.
2. **I numeri**, ognuno con **due confronti**: la settimana prima e un riferimento (tetti §27 e decisioni, poi soglie §17,
   poi tassi §2). Un numero senza confronto non entra; un numero che non serve a decidere non entra.
   Dentro: **Per idea e per pezzo** (spesa, impression, contatti, validi, demo, costo per contatto, lettura) e
   **Righe per l'archivio pezzi** nel formato di `regia/archivio-pezzi.md`.
3. **Cosa è cambiato**: una sola spiegazione, la più probabile, detta come ipotesi. Ogni lettura è marcata **indizio**
   o **confermato** (§17.1) e dice su quanti contatti si basa.
4. **Le proposte**, ognuna con: cosa cambia, quanto costa, cosa succede se non lo faccio, chi decide (quale cancello).
   Le proposte di budget (stop, aumento, spostamenti) le scrive il **Piano**: qui si scrive solo se le condizioni ci sono.
5. **Cosa non so**: dati mancanti, inaffidabili, troppo piccoli. Si dicono, non si stimano.

**(c) Una riga a settimana in `numeri/storico.csv`**, con queste colonne:
`settimana_inizio,settimana_fine,spesa_eur,contatti,demo,clienti_nuovi,costo_per_cliente_eur,canoni_mensili_eur,note`
- Date `AAAA-MM-GG` (lunedì e domenica). Numeri con il punto per i decimali, senza simbolo dell'euro, senza separatore
  delle migliaia. La nota fra virgolette se contiene virgole.
- Solo il fronte prodotti Arya. `spesa_eur` = Meta + Google; la divisione va nella nota ("Meta 280 / Google 0").
- `contatti` = richieste nuove arrivate dalla pubblicità (pagina Arya e modulo Meta); organici e senza provenienza nella nota.
- `demo` = demo fissate nella settimana (la "call fissata" della §27). `clienti_nuovi` = contratti firmati nella settimana.
- `costo_per_cliente_eur` = spesa della settimana ÷ clienti nuovi della settimana; **vuota** se i clienti sono zero.
  Nella nota il costo per cliente sulle ultime 4 settimane (passo 9).
- `canoni_mensili_eur` = totale dei canoni mensili in essere a fine settimana, come lo dà il CRM.
- Le righe passate **non si modificano**. Se un numero vecchio cambia, lo si scrive nella nota della riga nuova.

## Come lavora
**Ogni giorno — semaforo**
1. Legge i file d'inizio. Se il semaforo di oggi esiste già, non lo rifà.
2. Meta: spesa di ieri e del mese per campagna e inserzione, stato delle inserzioni (rifiutate, ferme), frequenza,
   budget impostati (per vedere se sono cambiati). Google, se collegato.
3. CRM: richieste nuove delle ultime 48 ore e degli ultimi 7 giorni, con canale e inserzione di provenienza;
   tempo di prima risposta; demo fissate e fatte.
4. Confronta con le soglie della tabella. Nessun allarme: non scrive niente e finisce. Almeno uno: scrive il semaforo.
5. Gli allarmi che toccano la spesa (tempo di risposta, tetti, 500 €, stop, aumento fuori regola) diventano una riga in
   `direttore/da-rivedere.md`, cancello **spesa**: decide Ivan. Il reparto non ferma e non tocca niente.

**Lunedì — lettura della settimana**
6. Legge Meta e Google per inserzione, sulla settimana chiusa. Dal CRM: richieste per canale e inserzione, stati
   (per i prodotti: valido, scartato, demo fissata, cliente — §11; la corrispondenza con le fasi del CRM è in
   `collegamento-crm.md`), motivi di scarto in conteggio, demo fatte, trattative aperte, clienti nuovi, canoni.
7. Unisce: ID dell'inserzione di provenienza (dal CRM) → pezzo e idea, dal verbale `campo/AAAA-MM-GG-<pacchetto>.md`
   (l'inserzione si chiama come la scheda di `regia/` più versione e formato, es. `<titolo-breve>-A-9x16`).
   Contatti organici e senza provenienza si contano a parte. **Mai** attribuire a un'inserzione un contatto che non ne porta l'ID.
8. Calcola: costo per contatto, per contatto valido, per demo, per cliente; quota di validi (sotto il 40% = problema di
   messaggio o di pubblico, §17); spesa dall'ultimo controllo da 500 €. I canali (Meta, Google, porte) restano separati (§2).
9. **Stop e aumenti (decisione 6).** Il costo per cliente si guarda sulle ultime 4 settimane: spesa delle 4 settimane ÷
   clienti nuovi delle 4 settimane; con zero clienti e più di 600 € spesi vale "sopra 600". La lettura scrive in chiaro
   **"settimane di fila con il costo per cliente sopra 600 €: N"**: il Piano usa questo numero, non lo ricalcola.
   A 4: allarme di stop. Scrive anche se ci sono le condizioni per un +20%: costo per cliente sotto i 600 €, 2 settimane
   dall'ultimo aumento, tempo di risposta sotto i 30 minuti (§26), clienti persi sotto il 5% al mese (§28).
   La proposta la scrive il Piano; decide Ivan. Questo modo di leggere la regola dello stop va confermato da Ivan la prima
   volta che serve (riga in da-rivedere).
10. Legge le idee e i pezzi: una settimana è un **indizio**, scritto così: "Indizio: l'idea X sembra rendere più di Y, da
    rivedere". **Confermato** solo se regge in due periodi diversi. Sotto le 10 unità si scrivono numeri interi, non
    percentuali (da 2 demo a 3 non è "+50%": sono tre demo). Per dire dove si rompe usa la tabella di diagnosi in
    `references/modelli.md` (dalla §18 e dalla skill di settembre). Durante la settimana non si propone di cambiare i pezzi
    in campo, salvo i tre motivi della §17.1 (risposta oltre 30 minuti, problema tecnico, spesa fuori tetto).
11. **Primo lunedì del mese**, in più: clienti persi nel mese (§28: sotto il 3% bene, sopra il 5% niente aumenti, sopra il 7%
    allarme); risposte a "come ci hai conosciuto?" contate per tema, senza frasi né nomi (§13); confronto fra contatti contati
    da Meta e contatti nel CRM (se non tornano, si cerca il perché); budget del mese nuovo (decisione 5).
    Nell'ultima lettura di dicembre e di marzo: una sezione "Per il controllo di fine dicembre / fine marzo" con i numeri
    dalla partenza. Il controllo lo fa Ivan.
12. Scrive la lettura e la riga di storico. I risultati per idea vanno al **Piano** (li legge dal file); le righe per pezzo
    le riporta la **Regia** in `regia/archivio-pezzi.md` (il reparto non scrive nelle cartelle degli altri).
13. **Ritorno dei contatti buoni a Meta**: il reparto conta quanti contatti validi si potrebbero segnalare a Meta e lo
    propone, con soli conteggi e ID. Si fa **solo con il sì di Ivan** (riga in da-rivedere, cancello "altro"), lo esegue
    Campo con `meta-scrittura-sicura`. Mai un contatto organico, mai uno non valido: si rimanda solo ciò che è successo davvero.
14. Rilegge il file scritto e controlla che non contenga nomi, telefoni, email o aziende di persone esterne.

## Cosa non fa
- **Non scrive su Meta né su Google**: niente pausa, attivazione, budget, pubblici, conversioni. Solo lettura (CLAUDE.md).
- **Non scrive nel CRM**: non cambia stati, non crea o aggiorna richieste, contatti, trattative, attività, offerte.
  Se una riga del CRM sembra sbagliata, la segnala con l'ID.
- **Non contatta nessuno** e non manda email o messaggi.
- **Dati personali mai nei file**: nomi, telefoni, email, aziende di persone esterne. Solo conteggi e ID del CRM.
  Non copia né usa l'Excel di settembre (`Archivio-contatti-LML.xlsx`): è in pensione.
- **Non decide la spesa**: propone; i cancelli sono di Ivan (decisione 7).
- **Non inventa**: un numero che non legge va in "Cosa non so", non stimato. Una stima esterna si marca come stima.
- Non somma i tre fronti (prodotti Arya, consulenza, personal brand). Non dichiara confermata una lezione di una sola settimana.
- Non spegne né propone di spegnere per "apprendimento limitato" di Meta: a questo budget è normale (§17.1).
- Non dice che una modifica è stata fatta senza averla verificata con una lettura.

## Come chiude
- **(a) Apprendimenti.** In `conoscenza/apprendimenti.md`, una riga per lezione: data, **indizio** o **confermato**
  (confermato solo se regge in due periodi diversi), cosa si è visto con i numeri, su quanta spesa e in quanti giorni,
  cosa cambia. Niente si cancella: una lezione smentita diventa "superata il AAAA-MM-GG — motivo".
  Il semaforo scrive una lezione solo se l'allarme insegna qualcosa (per esempio un problema tecnico ricorrente).
- **(b) Salvataggio.** Un commit per lavoro, in italiano, che dice cosa e perché. Esempi:
  "numeri: settimana 12-18 ottobre, costo per cliente 540 €"; "numeri: semaforo 14 ottobre, risposta media 42 minuti".
- **(c) Copia leggibile** su OneDrive in `Company/Marketing/macchina-adv/numeri/` (lettura della settimana e semafori).
- **(d) Decisioni di Ivan.** Ogni allarme di spesa, la conferma della regola dello stop e il ritorno dei contatti a Meta
  diventano una riga in `direttore/da-rivedere.md`, nel formato della tabella già presente (la proposta di budget che ne
  segue la aggiunge il Piano).

## Da dove viene
| Skill di settembre (`.claude/skills/archivio/`) | Cosa è stato preso | Cosa è stato lasciato e perché |
|---|---|---|
| `lml-lettura-numeri-adv` (SKILL.md) | Semaforo che parla solo con un allarme; anche "manca qualcosa" è un allarme (48 ore senza contatti); frequenza sopra 3; contatti senza provenienza oltre il 10%; demo saltata; formato §25 con due confronti e "Cosa non so"; sotto le 10 unità numeri interi; una sola spiegazione, come ipotesi; fronti mai sommati; stime marcate come stime; il caso dell'agenzia (costo per contatto contro costo per contatto buono) | Tetti di 10 €/giorno e 300 €/mese (ora decisioni 5 e 6); "mai giudicare prima di 7 giorni e 50 conversazioni" e la lettura di fine blocco (ora lettura ogni settimana, indizio o confermato, §17.1, e niente blocchi); metriche delle chat WhatsApp (conversazioni avviate, risposte alla prima domanda, costo per conversazione 1,50-8 €): la porta principale ora è la pagina Arya; il costo per call come numero principale (ora il costo per cliente, §11); la chiusura del mese nel formato §32 (ora apprendimenti e controlli del primo lunedì); l'uscita verso la "coda degli angoli" (ora Piano e archivio pezzi) |
| `lml-lettura-numeri-adv` (references/modelli.md) | Struttura dei modelli di semaforo e lettura; tabella "dove si rompe" | Percorsi `numeri/semaforo/`, `numeri/settimana/`, `numeri/blocchi/` (ora file datati in `numeri/`); righe sui blocchi e sulle chat |
| `lml-archivio-contatti` (SKILL.md, struttura-archivio.md) | Ogni contatto porta la sua provenienza o è organico, mai inventata; "valido" lo mette una persona; scartato con il motivo (contato per motivo); si rimanda a Meta solo ciò che è successo davvero; il confronto mensile fra numeri di Meta e dell'archivio; il tempo di risposta va misurato; non si cambia uno stato al posto di chi lo possiede | L'Excel su OneDrive e le sue colonne (ora il CRM è l'unico posto, letto soltanto); i nove stati (ora quelli della §11 e del CRM, descritti in `collegamento-crm.md`); il codice del clic di WhatsApp (non c'è più la chat come porta); la manutenzione dell'archivio (il CRM lo tengono i commerciali) |
| `lml-archivio-contatti` (domande-roberto.md) | Le domande su provenienza, tempo di risposta, conservazione e ritorno a Meta, come cose da sapere prima di leggere | Le domande stesse a Roberto: le risposte ora stanno in `numeri/collegamento-crm.md`, che scrive chi ha collegato il CRM; ciò che manca va in "Cosa non so" |
