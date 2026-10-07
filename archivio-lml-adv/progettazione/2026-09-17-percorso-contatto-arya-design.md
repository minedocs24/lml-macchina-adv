# Percorso automatico del contatto pubblicitario in ARYA

Data: 2026-09-17
Stato: in discussione. Approccio A (tutto dentro ARYA) proposto da Claude. Ivan ha chiesto di completare il lavoro senza scegliere al Cancello 1: l'approccio e le decisioni marcate "proposta" valgono solo dopo la sua revisione (Cancello 2).
Modalità: EVOLUZIONE di ARYA (Customer Care AI, in produzione).

Fonti lette: `regole-adv.md` v2.4 del 17/09/2026 (§3.1, §8, §10, §10.1, §11, §12, §13, §14, §23, §26) · skill `lml-archivio-contatti` v2.1 del 16/09/2026 · `fase-5-archivio-contatti.md` e `fase-7-4-contatti-importati.md` del 12/09/2026 · `Archivio-contatti-LML.xlsx` letto il 17/09/2026 · `inserzioni/software-house/B1-fuori-orario.md` del 17/09/2026.

**Limite di questa spec:** il codice di ARYA non era leggibile dalla sessione. Il progetto segue la struttura nota di ARYA (moduli `controller -> service -> repository`, porte e adattatori, code, isolamento per tenant, contratto `openapi.yaml`). Il Task 0 del piano confronta la spec con il codice vero e corregge i nomi prima di scrivere una riga.

---

## Obiettivo

Chi compila un modulo di un'inserzione prodotti riceve un messaggio WhatsApp di ARYA entro 5 minuti, a qualunque ora. Se risponde viene qualificato in chat, gli si può offrire la demo telefonica e viene assegnato a un commerciale per una call pomeridiana. L'esito della call torna nell'archivio. Ogni venerdì Ivan trova pronto, da approvare, l'elenco dei contatti buoni da rimandare a Meta. L'archivio vive in ARYA, non più su OneDrive.

---

## Decisioni

### Già prese da Ivan (verbale)

1. **Destinazione**: modulo dentro Meta, poi ARYA scrive su WhatsApp (14/09/2026). Motivo: nessuna inserzione sopravvissuta in Italia porta a WhatsApp, e il modulo arriva già attaccato all'inserzione.
2. **Un numero, una riga**: lo stesso numero che compila due volte è un contatto solo, con due contatti da parte di ARYA. Motivo: contarlo due volte gonfia i numeri.
3. **Demo telefonica solo a chi ha risposto in chat**. Motivo: una chiamata in uscita costa più di 1 €, una conversazione circa 0,10 €. Il costo delle chiamate sta fuori dal tetto pubblicitario di 300 €/mese.
4. **Nessuna scrittura automatica su Meta**. Il ritorno del venerdì si prepara e aspetta il sì di Ivan. Motivo: regola assoluta di `CLAUDE.md` e §24bis.
5. **Call fatte dai commerciali, nel pomeriggio**, e archivio visibile a tutti i commerciali (17/09/2026).
6. **Provenienza a tre valori**: inserzione, organico, partner (16/09/2026). Mai inventare `inserzione`.
7. **Regola di assegnazione non ancora decisa** (a turno o a mano): si progetta il punto di innesto e la regola resta configurabile.
8. **Il ricontatto vale anche di notte e la domenica** (pacchetto B1, regola L3): la promessa "adesso" regge solo se il primo messaggio parte sotto i 5 minuti a qualunque ora.

### Proposte da Claude, da confermare al Cancello 2

9. **Approccio A, tutto dentro ARYA.** Motivo: è l'unico che rispetta il vincolo "l'archivio è di ARYA". L'approccio B (Meta, poi Zoho, poi ARYA, come per Mr. Toner) lascerebbe l'archivio vero su Zoho. L'approccio C (automatico solo fino alla chat) lascerebbe promemoria ed esito alla memoria delle persone, che è proprio il punto debole di oggi (circa 1 contatto valido su 10 arriva alla call).
10. **I 157 contatti migrati non vengono mai ricontattati da ARYA.** Motivo: nessuno di loro ha dato il consenso a WhatsApp. Gli 87 "no" riguardano le email di marketing, gli altri 67 "sì" anche. Restano nell'archivio come storico, lavorabili a mano dai commerciali come oggi.
11. **Si migrano 157 righe, non 154.** Motivo: l'archivio ha 154 contatti della consulenza più 3 da LinkedIn. I 3 entrano con il loro fronte. Nessuno dei 157 è un contatto dei prodotti ARYA.
12. **"Valido" lo conferma una persona.** ARYA registra le risposte e segna "qualificazione superata". Lo stato `valido` lo mette il commerciale, al più tardi nell'esito della call. Motivo: regola 5 della skill archivio ("Valido lo mette una persona, non un automatismo"), e il ritorno a Meta deve contenere solo cose successe davvero.
13. **Due moduli dallo stesso numero entro 10 minuti contano come uno.** Motivo: il doppio invio per errore esiste, e due messaggi di ARYA a distanza di secondi sembrano un difetto. Oltre i 10 minuti vale la decisione 2.
14. **Il flusso automatico si accende modulo per modulo.** I moduli della consulenza entrano nell'archivio ma ARYA non scrive. Motivo: la §3.1 separa il percorso dei prodotti da quello della consulenza, e i fronti non si mescolano.
15. **Il consenso è registrato per finalità, non come un sì generico**: contatto su WhatsApp, marketing successivo, ritorno a Meta. Motivo: l'errore già visto (43 indirizzi con "no" in una lista d'invio) nasce proprio da un consenso usato per una finalità diversa.
16. **Il ritorno del venerdì parte solo da un clic di Ivan** nel pannello. In alternativa Ivan scarica il file e lo carica a mano su Meta. Motivo: in entrambi i casi l'azione su Meta è sua.
17. **Le skill di Claude leggeranno un estratto giornaliero senza dati personali** scritto da ARYA in `lml-adv/numeri/archivio/`. Motivo: oggi semaforo, lettura dei numeri e direttore leggono l'Excel. Tolto l'Excel, si fermerebbero in silenzio. Le skill esistenti non si toccano: se ne fanno copie rinominate.
18. **Fascia pomeridiana proposta: dal lunedì al venerdì, 14:30-18:30, call da 15 minuti.** È un valore di configurazione. Motivo: finora i contatti si richiamavano alle 15:00, e la call da 15 minuti è quella citata nel pacchetto.

### Restano a Ivan, e bloccano l'accensione (non il lavoro)

19. **Per quanto tempo si tengono i contatti**: si decide con chi segue la privacy. Il sistema rifiuta di accendere il flusso finché il valore non è impostato.
20. **Il testo dell'informativa** deve coprire le tre finalità della decisione 15, compreso il ritorno a Meta. Senza questo, il lotto del venerdì esce sempre vuoto e dice perché.

---

## Architettura

Nomi dei file indicativi, da allineare al Task 0. Il core parla di "contatto", "invio", "fonte": non nomina né Meta né parole di LML come blocco e angolo (principio A4).

### 1. Dominio: modulo `modules/lead`

**Entità**

| Entità | Cosa rappresenta | Chiave |
|---|---|---|
| `Lead` | una persona per tenant | `tenantId + phoneE164`, univoca |
| `LeadSubmission` | ogni compilazione di un modulo | `tenantId + sourceKey + externalId`, univoca (idempotenza) |
| `LeadEvent` | cronologia, sola aggiunta: cambi di stato, messaggi, call, esiti | id |
| `LeadConsent` | consenso per finalità, con data e testo dell'informativa | `leadId + purpose` |
| `CallAppointment` | call con il commerciale: slot, commerciale, stato | id |
| `ConversionBatch` | lotto settimanale da approvare | `tenantId + weekStart`, univoca |

**`LeadSubmission` porta con sé:** `sourceKey` (stringa dell'adattatore), `externalId` (id del modulo compilato), `formRef`, `adRef`, `adName`, `adTitle` (il titolo dell'inserzione visto), `attributes` (mappa chiave-valore: per LML `blocco` e `angolo`), `origin` (`inserzione` | `organico` | `partner` | `import`), `front`, `answers` (risposte del modulo, compresa la fascia di volume e "come ci hai conosciuto"), `consentSnapshot`, `submittedAt`, `receivedAt`.

**Stati di `Lead`**, dalla skill archivio v2.1:

| Stato | Chi lo mette |
|---|---|
| `nuovo` | sistema, all'ingresso |
| `in_lavorazione` | sistema, alla prima risposta in chat |
| `scartato` (con motivo) | ARYA in chat o commerciale |
| `valido` | commerciale (decisione 12) |
| `call_fissata` | ARYA o commerciale |
| `call_fatta` | commerciale |
| `non_ora` (con data di ricontatto) | commerciale |
| `perso` (con motivo) | commerciale |
| `attivazione` | solo Ivan (ruolo `admin`) |

Le transizioni ammesse stanno in una tabella sola (`lead.state-machine.ts`). Un passaggio non previsto viene rifiutato con un errore esplicito, mai ignorato. I motivi di scarto e di perdita vengono da una lista chiusa, configurabile per tenant: volume troppo basso, settore fuori, non è il titolare, cercava altro, fornitore, studente, nessuna risposta.

**Flag separati dallo stato:** `qualification` (`non_iniziata` | `in_corso` | `superata` | `non_superata`, con le risposte su settore, volume, ruolo e azienda) e `outreachAllowed` (calcolato dal consenso WhatsApp).

### 2. Ingresso: porta `LeadSourcePort`

`modules/lead/port/lead-source.port.ts`, volutamente povera:

- `parseWebhook(request) -> ExternalRef[]`: verifica la firma, estrae solo gli id
- `fetchSubmission(ref) -> NormalizedSubmission`
- `listSince(formRef, since) -> ExternalRef[]`: serve alla riconciliazione

Adattatore `adapters/meta-lead-ads/`: legge il modulo compilato e poi, solo in lettura, nome dell'inserzione e titolo della creatività. Il formato dei dati di Meta non esce dall'adattatore. La chiave `meta-lead-ads` è una stringa registrata nel registro delle fonti (A3).

**Flusso d'ingresso**

1. Il webhook risponde subito e mette in coda `lead-ingest` (A8).
2. Il worker legge il modulo, normalizza il telefono in formato E.164 e crea o aggiorna il `Lead` (decisioni 2 e 13). Poi crea la `LeadSubmission`. Se l'`externalId` esiste già non fa nulla (idempotenza).
3. Gli attributi si ricavano dal nome dell'inserzione con una regola configurata per tenant (`tenant.leadAttributionRule`, un'espressione con gruppi nominati). Se la regola non trova nulla, gli attributi restano vuoti e si segnala "provenienza incompleta". Non si indovina mai.
4. Se il modulo ha il flusso acceso (decisione 14) e il consenso WhatsApp è sì, si accoda `lead-outreach`.
5. **Riconciliazione ogni 15 minuti** (`lead-reconcile`): confronta i moduli compilati su Meta con quelli in ARYA e recupera i mancanti. Una volta al giorno, se i conteggi differiscono, scatta un avviso.

Il collegamento della pagina Facebook all'app (iscrizione al webhook) è una scrittura su Meta. Si fa una volta sola, con il sì esplicito di Ivan (Task 16).

### 3. Primo contatto: `LeadOutreachService`

- Usa la porta canale che esiste già (WhatsApp) e manda un **modello pre-approvato**. Il primo messaggio lo manda LML, quindi serve un modello.
- **Guardia del consenso**: senza `LeadConsent(whatsapp_contact)=sì` non si invia. La guardia sta nel service, non nel testo delle istruzioni dell'agente.
- **Guardia dell'articolo 50**: la configurazione rifiuta un modello di primo contatto che non abbia `aiDisclosure: true`. Il testo dichiara che scrive un assistente automatico.
- Il messaggio usa il titolo dell'inserzione vista e la fascia di volume, quando ci sono. Altrimenti usa la versione senza variabili prevista dal pacchetto B1.
- **Secondo modulo dallo stesso numero** (oltre i 10 minuti): secondo messaggio con il modello "nuova richiesta", nella stessa conversazione. Se c'è già una call fissata, il messaggio la ricorda invece di ricominciare la qualificazione.
- **Misura**: `firstOutreachAt - submittedAt` viene salvato su ogni invio. Se il messaggio non parte entro 5 minuti scatta un avviso a Ivan (§11).

### 4. Conversazione: strumenti dell'agente (registro degli strumenti, A5)

| Strumento | Cosa fa | Guardia nel codice |
|---|---|---|
| `lead.record_qualification` | salva settore, volume, ruolo, azienda, e calcola `qualification` con la soglia del settore (config) | nessuna |
| `lead.offer_demo_call` | propone la demo telefonica | acceso solo se il contatto ha scritto almeno un messaggio in chat |
| `lead.start_demo_call` | fa partire la chiamata | messaggio in chat + sì esplicito registrato + tetto giornaliero non superato |
| `lead.propose_call_slots` / `lead.book_call` | propone gli orari e fissa la call con il commerciale | qualificazione superata; orari dalla porta di assegnazione |
| `lead.discard` | scarta con un motivo della lista | motivo obbligatorio |

**Demo telefonica:** usa la capacità voce che esiste già. La prima frase dichiara che parla un assistente automatico. Il costo si registra in un centro di costo separato (`demo_call`) e c'è un tetto giornaliero di chiamate (config, proposto: 5). Se la chiamata fallisce, ARYA lo dice in chat e propone di nuovo; non richiama da sola.

### 5. Assegnazione: porta `AssignmentStrategyPort`

`modules/lead/assignment/assignment-strategy.port.ts`, un'operazione sola: `assign(lead, candidates, context) -> Assignment | PendingManual`.

- Strategie registrate: `round_robin` (a turno, salta chi non ha orari liberi) e `manual` (mette il contatto nella coda "da assegnare" e avvisa Ivan).
- Scelta per tenant: `tenant.leadAssignment.strategy`. Si cambia senza toccare il codice. Una strategia nuova è un file registrato in più.
- **Orari liberi**: fascia pomeridiana da configurazione (decisione 18), meno le call già fissate in ARYA per quel commerciale.
- Con `manual`, ARYA non può proporre orari prima dell'assegnazione. Allora raccoglie la disponibilità del contatto, e la call la fissa il commerciale assegnato.

### 6. Promemoria: coda `lead-reminders` (lavori programmati)

- **Al contatto**: un promemoria WhatsApp 2 ore prima della call, con un modello di servizio. Se la call è fissata a meno di 2 ore, nessun promemoria.
- **Al commerciale**: email all'assegnazione e 30 minuti prima, con nome, azienda, risposte della chat e titolo dell'inserzione vista.
- Se la call si sposta, i promemoria vecchi si annullano. I lavori hanno un id legato all'appuntamento, così non partono due volte.

### 7. Esito: pannello ARYA

- Il commerciale segna: `call_fatta` (con conferma di validità sì/no, note e "come ci hai conosciuto" a testo libero, §13), `non_ora` (data obbligatoria), `perso` (motivo obbligatorio) oppure "non si è presentato".
- "Non si è presentato" crea un evento e riporta il contatto a `in_lavorazione`. ARYA propone un nuovo orario una sola volta.
- **Scadenza dell'esito**: 24 ore dopo lo slot senza esito scatta un avviso al commerciale e a Ivan. È il caso peggiore della skill archivio: la call fissata e non fatta.
- `attivazione` la mette solo Ivan.

### 8. Ritorno a Meta: `ConversionBatchService` e porta `ConversionSinkPort`

- **Ogni venerdì alle 09:00** si costruisce il lotto della settimana con stato `in_attesa_approvazione`. Una riga per ogni passaggio avvenuto: `valido`, `call_fatta`, `attivazione`.
- **Entra solo chi ha tutti e tre i requisiti:** `origin = inserzione`, consenso "ritorno a Meta" sì, riga mai inviata prima. Il pannello mostra quanti contatti sono stati esclusi e per quale motivo (organico, partner, senza consenso, già inviati).
- **Lotto vuoto**: si crea lo stesso, con la spiegazione del perché è vuoto. Un lotto vuoto non passa mai per un lotto riuscito (A7).
- **Ivan può fare due cose:** approvare e inviare con un clic, oppure scaricare il file e caricarlo a mano. `ConversionSinkPort.send(batch)` rifiuta ogni lotto non approvato. La guardia sta nel service e c'è un test che la sorveglia.
- Adattatore `adapters/meta-conversions/`: usa l'id del modulo compilato come chiave di abbinamento. Salva la risposta di Meta riga per riga. Le righe rifiutate restano visibili e reinviabili.

### 9. Accessi

| Ruolo | Vede | Modifica |
|---|---|---|
| `admin` (Ivan) | tutto | tutto, compresi attivazione, lotti, configurazione |
| `commerciale` | tutti i contatti di LML (decisione di Ivan del 17/09) | esiti e note dei contatti assegnati a sé; presa in carico dalla coda "da assegnare" solo se la strategia lo permette |

- I commerciali non possono esportare (regola 7 della skill archivio). Gli export di `admin` finiscono nel registro degli accessi.
- Le nuove tabelle stanno dentro il perimetro del tenant: la regola applicativa e la policy del database valgono entrambe (A9).

### 10. Conservazione e cancellazione

- `tenant.leadRetentionMonths` è obbligatorio per accendere il flusso (decisione 19).
- Un lavoro mensile rende anonimi i contatti scaduti che non sono diventati clienti.
- Una richiesta di cancellazione elimina contatto, moduli, consensi e id di Meta, e lascia nella cronologia solo "cancellato su richiesta" con la data.

### 11. Migrazione dei 157 contatti: script `scripts/import-lead-archive.ts`

- **Legge** `Archivio-contatti-LML.xlsx`, foglio Contatti.
- **Due modalità:** `--dry-run` produce solo un rapporto, `--apply` scrive.
- **Traduce gli stati**: `incontro fissato` → `call_fissata`, `incontro fatto` → `call_fatta`, `non ora - in coltivazione` → `non_ora`. Gli stati che hanno già il nome giusto restano uguali (compresi `valido`, `scartato`, `nuovo`, `in lavorazione`). `analisi venduta` è uno stato che esiste solo per la consulenza. Uno stato sconosciuto ferma lo script.
- **Normalizza i telefoni.** I numeri che non si riescono a normalizzare vanno nel rapporto e non entrano.
- **Fonde i doppioni sullo stesso numero** e li elenca. Nella lettura di oggi c'è almeno una coppia.
- **Campi di provenienza:** `origin = import`, fronte originale, blocco e angolo vuoti, nome dell'inserzione dalla colonna D. Le note si conservano per intero.
- **Consensi:** marketing da colonna V (87 no, 67 sì, 3 vuoti che diventano "non dato"). WhatsApp e ritorno a Meta: "non dato" per tutti (decisione 10).
- **Riga ignorata:** la data e ora della prima risposta risale all'agenzia ed è stimata. Si porta nelle note, non nel campo misurato.
- **Rapporto finale:** righe lette = contatti creati + fusioni + scartati, con elenco.
- **Dopo l'importazione**, l'Excel si rinomina `Archivio-contatti-LML-congelato-2026-MM-GG.xlsx`, in sola lettura. Non si cancella.

### 12. Estratto giornaliero per Claude

- **Ogni giorno alle 06:00** ARYA scrive `lml-adv/numeri/archivio/AAAA-MM-GG.csv`: una riga per contatto, senza nome, telefono né email, con id interno, date, fronte, origine, blocco, angolo, titolo, stato, motivi, minuti al primo contatto e date della call.
- **Le skill da adattare** (archivio contatti, lettura dei numeri, semaforo, direttore) si duplicano con un nome nuovo e leggono questo file. Le originali restano come sono.

### Principi dell'Appendice A

| Principio | Esito |
|---|---|
| A1 strati | rispettato: webhook, lavori e pannello usano lo stesso `LeadService` |
| A2 contratto prima | rispettato: Task 2 prima dell'implementazione |
| A3 porte povere | rispettato: tre porte con 1-3 operazioni ciascuna, chiavi stringa |
| A4 core generico | rispettato: "blocco" e "angolo" vivono solo nella configurazione del tenant LML |
| A5 capacità registrate | rispettato: strumenti dell'agente e strategie di assegnazione nei registri |
| A6 errori | vedi "Comportamenti attesi" |
| A7 successo silenzioso | rispettato: avvisi su invio mancato, esito mancato, conteggi diversi, lotto vuoto spiegato |
| A8 code | rispettato: `lead-ingest`, `lead-outreach`, `lead-reconcile`, `lead-reminders`, `lead-demo-call` (corsia separata, perché la chiamata dura minuti) |
| A9 isolamento | rispettato: tabelle nuove registrate nel perimetro, test di completezza |
| A10 segreti | rispettato: token Meta cifrati per tenant, telefoni oscurati nei log |
| A11 rete di sicurezza | rispettato: Task 1 |
| A12 perché nel codice | le guardie di consenso, articolo 50 e approvazione portano il motivo nel commento |
| A13 scelte a Ivan | decisioni 19 e 20 restano sue; le 9-18 sono proposte |

---

## Vincoli critici

- **Nessuna scrittura su Meta senza un'azione di Ivan.** Se un lavoro programmato scrivesse da solo, violerebbe la regola assoluta del progetto e manderebbe a Meta dati magari senza consenso.
- **Non si contatta su WhatsApp chi non ha dato quel consenso**, compresi i 157 migrati. Toccarlo significa messaggi commerciali senza base legale.
- **Il primo messaggio e la demo dichiarano sempre l'assistente automatico** (articolo 50 del Reg. UE 2024/1689, applicabile dal 2 agosto 2026).
- **La demo telefonica non parte mai senza un messaggio del contatto in chat.** Senza questa guardia ogni modulo diventa una spesa di più di 1 €.
- **I fronti non si sommano** nei riepiloghi e nell'estratto giornaliero.
- **Il percorso lead già in produzione per Mr. Toner** (Zoho, poi WhatsApp) non si modifica. Il Task 1 lo fissa con dei test prima di toccare il canale.
- **Le skill esistenti non si modificano**: si duplicano.
- **L'Excel non si cancella**: dopo la migrazione resta congelato come prova di quello che c'era.

---

## Comportamenti attesi

| Caso | Cosa succede | Chi lo vede |
|---|---|---|
| Stesso modulo notificato due volte | una sola `LeadSubmission` (chiave univoca) | nessuno, è normale |
| Stesso numero, secondo modulo entro 10 minuti | un modulo in più registrato, nessun secondo messaggio | nessuno |
| Stesso numero, secondo modulo dopo 10 minuti | una riga, secondo modulo, secondo messaggio "nuova richiesta" | commerciale, nella cronologia |
| Webhook perso | recuperato dalla riconciliazione entro 15 minuti; primo messaggio in ritardo, tempo misurato e avviso se oltre 5 minuti | Ivan |
| Lettura del nome dell'inserzione fallita | contatto registrato e contattato lo stesso; attributi riprovati dopo; "provenienza incompleta" (l'errore non blocca) | Ivan, nell'estratto |
| Invio WhatsApp fallito | 3 tentativi con attesa crescente, poi coda degli errori e avviso (l'errore blocca) | Ivan |
| Numero non su WhatsApp | stato resta `nuovo`, evento "non raggiungibile su WhatsApp", avviso al commerciale per una telefonata a mano | commerciale |
| Consenso WhatsApp assente | nessun invio, evento "contatto non consentito" | commerciale |
| Il contatto non risponde | nessuna demo, nessuna chiamata; un solo messaggio di ripresa dopo 24 ore con modello, poi passa ai tentativi dei commerciali (§11, sei tentativi) | commerciale |
| Tetto giornaliero delle demo raggiunto | ARYA propone la call con il commerciale al posto della demo | Ivan, nel riepilogo costi |
| Nessun commerciale libero nella fascia | proposti i giorni successivi; se non c'è nulla entro 5 giorni lavorativi, coda "da assegnare" e avviso | Ivan |
| Call senza esito dopo 24 ore | avviso al commerciale e a Ivan | entrambi |
| Commerciale che prova a mettere `attivazione` | rifiutato con errore di permesso | commerciale |
| Lotto del venerdì non approvato | resta in attesa; il venerdì dopo se ne crea uno nuovo e il vecchio resta approvabile | Ivan |
| Meta rifiuta alcune righe | righe marcate "rifiutate" con il motivo, reinviabili | Ivan |
| Flusso acceso senza tempo di conservazione | accensione rifiutata con messaggio | Ivan |

---

## Limiti noti

- **Codice di ARYA non letto.** Nomi di file, comandi e forma del pannello sono da verificare (Task 0).
- **Nessun collegamento ai calendari dei commerciali.** Gli orari liberi si calcolano solo sulle call fissate in ARYA. Un impegno preso fuori da ARYA non si vede.
- **Parametri esatti dell'integrazione Meta non verificati** (tipo di modulo "maggiore intenzione", evento di ritorno, chiave di abbinamento). `CLAUDE.md` li segnala come da leggere alla prima campagna.
- **Costo dei messaggi WhatsApp con modello non misurato**: dipende dalla categoria che Meta assegna al modello. Da misurare nella prova con 20 contatti.
- **I 157 migrati non hanno tempi di risposta veri né provenienza di blocco.** Non entrano nei calcoli della §11 né nei lotti per Meta.
- **I moduli della campagna dell'agenzia sull'account Minedocs non sono tutti nell'archivio** (il semaforo del 17/09 ne conta 11 fuori). Meta li tiene 90 giorni: i più vecchi (3 luglio) cominciano a sparire intorno al 1 ottobre. Il recupero è un lavoro separato e urgente, fuori da questa spec.

---

## Test

| Test | Tipo | Cosa dimostra |
|---|---|---|
| `lead.state-machine.spec` | unità | solo le transizioni ammesse, motivi obbligatori, `attivazione` solo da `admin` |
| `lead.dedup.spec` | integrazione | stesso `externalId` = 1 modulo; stesso numero = 1 contatto; finestra dei 10 minuti |
| `lead-source.meta.spec` | adattatore | firma verificata, dati di Meta non escono dall'adattatore, regola degli attributi, nessun attributo inventato |
| `lead-reconcile.spec` | integrazione | un modulo senza webhook viene recuperato |
| `lead-outreach.consent.spec` | integrazione | senza consenso WhatsApp nessun invio, compresi i migrati |
| `lead-outreach.ai-disclosure.spec` | unità | un modello senza dichiarazione viene rifiutato |
| `lead-outreach.sla.spec` | integrazione | un invio oltre i 5 minuti produce l'avviso |
| `lead-tools.demo-guard.spec` | unità | niente demo senza messaggio in chat, senza sì, oltre il tetto |
| `assignment.strategies.spec` | unità | a turno salta chi è occupato; manuale mette in coda; strategia sconosciuta rifiutata dal registro |
| `lead-reminders.spec` | integrazione | un solo promemoria per call; annullato se la call si sposta |
| `lead-outcome.deadline.spec` | integrazione | 24 ore senza esito producono l'avviso |
| `conversion-batch.builder.spec` | unità | esclusi organico, partner, senza consenso, già inviati; lotto vuoto spiegato |
| `conversion-sink.approval.spec` | integrazione | un lotto non approvato non si invia |
| `lead.access.spec` | integrazione | un commerciale non esporta e non modifica contatti non suoi |
| `lead.retention.spec` | integrazione | accensione rifiutata senza conservazione; anonimizzazione dei contatti scaduti |
| `import-lead-archive.spec` | script | stati tradotti, doppioni fusi, conteggi che tornano, nessun consenso WhatsApp assegnato |
| test costituzionali esistenti: contratto OpenAPI, core generico a cricchetto, completezza del perimetro tenant | architettura | rotte nuove nel contratto; nessun "meta" o "blocco" nel core; tabelle nuove dichiarate |
| prova con 20 contatti finti | fine-corsa, su un modulo di prova | il cancello della §3.1 e della §26, con le cinque verifiche della skill archivio |

---

## Definition of Done

1. Tutti i test sopra passano, compresi i test costituzionali, con i registri aggiornati in un task dedicato.
2. **Prova con 20 contatti finti superata**, con un risultato scritto in `lml-adv/collaudi/`:
   - 20 su 20 contattati;
   - tempo al primo messaggio sotto i 5 minuti in almeno 19 casi su 20, di cui almeno 5 prove di notte o di domenica;
   - il doppio modulo produce una riga;
   - un contatto senza consenso WhatsApp non riceve nulla;
   - demo rifiutata a chi non ha risposto;
   - assegnazione, promemoria ed esito registrati;
   - lotto del venerdì costruito e **non inviato** senza approvazione.
3. **Migrazione eseguita**: il rapporto dice che righe lette = contatti + fusioni + scartati, e l'Excel è congelato.
4. **Almeno un commerciale** entra con il suo profilo, vede i contatti e registra un esito. Un'esportazione tentata da lui viene rifiutata.
5. **L'estratto giornaliero** compare in `numeri/archivio/` e le copie delle skill lo leggono.
6. **Tempo di conservazione e informativa** sono impostati da Ivan: senza, il flusso resta spento, ed è un risultato accettabile di questa consegna.
7. **Nessuna scrittura su Meta** è avvenuta senza un sì di Ivan registrato in conversazione.
