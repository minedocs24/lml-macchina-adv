# Piano: percorso automatico del contatto pubblicitario in ARYA

Data: 2026-09-17
Spec di riferimento: `progettazione/2026-09-17-percorso-contatto-arya-design.md`
Stato: **bozza.** Vale dopo che Ivan ha approvato la spec (Cancello 2). Nessun task si esegue prima.
Ordine dei task: uno dopo l'altro, salvo dipendenze dichiarate.

I nomi dei file e i comandi seguono la struttura nota di ARYA. Il Task 0 li confronta con il codice vero e li corregge **in questo file**, prima di tutto il resto.

---

## Task 0: allineare la spec al codice di ARYA
Cosa: leggere `CLAUDE.md`, i documenti in `docs/`, le spec precedenti, il modulo canale, il percorso lead di Mr. Toner, il registro degli strumenti e i test costituzionali. Poi correggere nomi e comandi nella spec e in questo piano.
File: la spec e il piano (nessun codice)
Dipende da: approvazione della spec
Verifica: `git diff --stat docs/` → cambiano solo spec e piano; una sezione "Scostamenti trovati" nella spec, anche vuota con scritto "nessuno"
Commit: `docs: allinea la spec del percorso contatto al codice`

## Task 1: rete di sicurezza sul percorso esistente
Cosa: test che fissano il comportamento attuale del canale WhatsApp in uscita (invio con modello, errori) e del percorso lead di Mr. Toner (Zoho, poi WhatsApp).
File: `apps/api/src/modules/channel/**/__tests__/outbound-template.characterization.spec.ts`, `apps/api/src/modules/<lead-mr-toner>/__tests__/*.characterization.spec.ts`
Dipende da: Task 0
Verifica: `pnpm --filter api test -- characterization` → tutti verdi, **senza modifiche al codice di produzione**
Commit: `test: fissa il comportamento attuale del canale in uscita e del percorso lead esistente`

## Task 2: contratto pubblico
Cosa: aggiungere a `openapi.yaml` le rotte per webhook fonte, contatti, moduli, eventi, esiti, coda da assegnare, lotti (costruzione, approvazione, invio, scarico), consensi e configurazione. Poi rigenerare il client.
File: `openapi.yaml`, `packages/shared/**` (generato)
Dipende da: Task 0
Verifica: `pnpm generate:client && pnpm --filter api test -- openapi-contract` → verde; le rotte nuove risultano documentate e non ancora implementate secondo il meccanismo del test (da confermare al Task 0)
Commit: `feat(contract): rotte del percorso contatto`

## Task 3: schema dei dati e perimetro del tenant
Cosa: tabelle `Lead`, `LeadSubmission`, `LeadEvent`, `LeadConsent`, `CallAppointment`, `ConversionBatch`, con le chiavi univoche della spec. Registrazione nel perimetro del tenant e policy del database.
File: `prisma/schema.prisma`, `prisma/migrations/<data>_lead_pipeline/`, elenco delle entità con ambito
Dipende da: Task 2
Verifica: `pnpm prisma migrate dev && pnpm --filter api test -- tenant-isolation` → verde, compreso il test di completezza con le 6 tabelle nuove
Commit: `feat(lead): schema dati e isolamento per tenant`

## Task 4: dominio del contatto
Cosa: `LeadService` con la tabella delle transizioni, i motivi obbligatori, la deduplica per numero, la finestra dei 10 minuti e la cronologia a sola aggiunta.
File: `modules/lead/lead.service.ts`, `lead.state-machine.ts`, `lead.repository.ts`, test `lead.state-machine.spec.ts`, `lead.dedup.spec.ts`
Dipende da: Task 3
Verifica: `pnpm --filter api test -- lead.state-machine lead.dedup` → verde
Commit: `feat(lead): stati, deduplica e cronologia del contatto`

## Task 5: ingresso dalla fonte
Cosa: `LeadSourcePort`, registro delle fonti, adattatore `meta-lead-ads` (firma, lettura del modulo, nome e titolo dell'inserzione in sola lettura), code `lead-ingest` e `lead-reconcile`, regola degli attributi da configurazione del tenant.
File: `modules/lead/port/lead-source.port.ts`, `modules/lead/adapters/meta-lead-ads/**`, `modules/lead/jobs/ingest.processor.ts`, `reconcile.processor.ts`, test relativi
Dipende da: Task 4
Verifica: `pnpm --filter api test -- lead-source lead-reconcile generic-core` → verde; il test del core generico non trova "meta" né "blocco" fuori dagli adattatori e dalla configurazione
Commit: `feat(lead): ingresso dei moduli con riconciliazione`

## Task 6: primo contatto su WhatsApp
Cosa: `LeadOutreachService` con la guardia del consenso, il controllo della dichiarazione dell'articolo 50 sui modelli, il secondo messaggio "nuova richiesta", la misura del tempo e l'avviso oltre i 5 minuti. Coda `lead-outreach` con 3 tentativi e coda degli errori.
File: `modules/lead/outreach/**`, validatore della configurazione dei modelli, test `lead-outreach.*.spec.ts`
Dipende da: Task 5, Task 1
Verifica: `pnpm --filter api test -- lead-outreach characterization` → verde, **compresi i test del Task 1 invariati**
Commit: `feat(lead): primo contatto con consenso e dichiarazione dell'assistente`

## Task 7: strumenti dell'agente per la qualificazione e la call
Cosa: registrare `lead.record_qualification`, `lead.offer_demo_call`, `lead.propose_call_slots`, `lead.book_call` e `lead.discard`, con le guardie nel codice. Soglie di qualificazione per settore da configurazione.
File: `modules/tools/lead/**`, test `lead-tools.*.spec.ts`
Dipende da: Task 6
Verifica: `pnpm --filter api test -- lead-tools` → verde; lo strumento della demo risulta spento per un contatto senza messaggi in chat
Commit: `feat(tools): qualificazione e prenotazione in chat`

## Task 8: demo telefonica
Cosa: `lead.start_demo_call` su una corsia dedicata `lead-demo-call`, frase iniziale con la dichiarazione, tetto giornaliero, centro di costo `demo_call`.
File: `modules/tools/lead/start-demo-call.tool.ts`, `modules/lead/jobs/demo-call.processor.ts`, test `lead-tools.demo-guard.spec.ts`
Dipende da: Task 7
Verifica: `pnpm --filter api test -- demo-guard` → verde; a tetto raggiunto lo strumento risponde "non disponibile oggi" e non accoda nulla
Commit: `feat(lead): demo telefonica con guardie e tetto`

## Task 9: punto di innesto dell'assegnazione
Cosa: `AssignmentStrategyPort`, registro delle strategie, `round_robin` e `manual`, fascia pomeridiana e calcolo degli orari liberi, coda "da assegnare" con avviso.
File: `modules/lead/assignment/**`, test `assignment.strategies.spec.ts`
Dipende da: Task 4 (in parallelo ai Task 5-8)
Verifica: `pnpm --filter api test -- assignment` → verde; cambiando `tenant.leadAssignment.strategy` nel test cambia il comportamento senza modifiche al codice
Commit: `feat(lead): assegnazione configurabile al commerciale`

## Task 10: promemoria
Cosa: coda `lead-reminders`, promemoria al contatto 2 ore prima e email al commerciale all'assegnazione e 30 minuti prima. Id dei lavori legato all'appuntamento, annullamento se la call si sposta.
File: `modules/lead/reminders/**`, test `lead-reminders.spec.ts`
Dipende da: Task 7, Task 9
Verifica: `pnpm --filter api test -- lead-reminders` → verde; spostare una call lascia un solo promemoria in coda
Commit: `feat(lead): promemoria della call`

## Task 11: esito, ruoli e scadenze nel pannello
Cosa: schermate contatti, cronologia, coda "da assegnare" ed esito. Ruolo `commerciale` con i permessi della spec, blocco delle esportazioni, registro degli accessi, avviso a 24 ore senza esito.
File: `apps/web/src/features/leads/**`, `modules/lead/lead.controller.ts`, guardie dei ruoli, test `lead.access.spec.ts`, `lead-outcome.deadline.spec.ts`
Dipende da: Task 9, Task 10
Verifica: `pnpm --filter api test -- lead.access lead-outcome && pnpm --filter web test -- leads` → verde
Commit: `feat(lead): esito della call e accesso dei commerciali`

## Task 12: lotto del venerdì
Cosa: `ConversionBatchService` (costruzione alle 09:00 del venerdì, esclusioni spiegate, lotto vuoto spiegato), approvazione e scarico da pannello, `ConversionSinkPort` con l'adattatore `meta-conversions` che rifiuta i lotti non approvati.
File: `modules/lead/conversions/**`, `modules/lead/adapters/meta-conversions/**`, pagina lotti, test `conversion-batch.*.spec.ts`, `conversion-sink.approval.spec.ts`
Dipende da: Task 11
Verifica: `pnpm --filter api test -- conversion` → verde; nessuna chiamata di rete verso Meta nei test senza un lotto in stato `approvato`
Commit: `feat(lead): lotto settimanale da approvare per il ritorno a Meta`

## Task 13: conservazione e cancellazione
Cosa: `tenant.leadRetentionMonths` obbligatorio per accendere il flusso, anonimizzazione mensile, cancellazione su richiesta.
File: `modules/lead/retention/**`, validatore della configurazione, test `lead.retention.spec.ts`
Dipende da: Task 4
Verifica: `pnpm --filter api test -- lead.retention` → verde; accensione senza valore rifiutata con messaggio
Commit: `feat(lead): conservazione e cancellazione dei contatti`

## Task 14: migrazione dei 157 contatti
Cosa: `scripts/import-lead-archive.ts` con `--dry-run` e `--apply`. Prova a secco su una copia dell'Excel, rapporto rivisto da Ivan, poi esecuzione e congelamento del file.
File: `scripts/import-lead-archive.ts`, test `import-lead-archive.spec.ts`, rapporto in `lml-adv/progettazione/migrazione-archivio-<data>.md`
Dipende da: Task 4, Task 13. **L'esecuzione con `--apply` richiede il sì di Ivan sul rapporto.**
Verifica: `pnpm tsx scripts/import-lead-archive.ts --dry-run <copia.xlsx>` → rapporto con righe lette 157 = contatti + fusioni + scartati; `outreachAllowed = false` su tutti
Commit: `feat(scripts): migrazione dell'archivio contatti da Excel`

## Task 15: estratto giornaliero e copie delle skill
Cosa: lavoro delle 06:00 che scrive il CSV senza dati personali in `lml-adv/numeri/archivio/`. Copie rinominate delle skill archivio, lettura dei numeri, semaforo e direttore che leggono il CSV invece dell'Excel.
File: `modules/lead/jobs/daily-extract.processor.ts`, adattatore di scrittura su OneDrive, le quattro skill duplicate
Dipende da: Task 14
Verifica: `pnpm --filter api test -- daily-extract` → il CSV non contiene colonne con nome, telefono o email; il giorno dopo il file esiste nella cartella e la copia del semaforo lo legge senza errori
Commit: `feat(lead): estratto giornaliero per i report`

## Task 16: collegamento reale e prova con 20 contatti finti
Cosa, in quattro passi:
1. Proporre a Ivan, con account, pagina e app esatti, l'iscrizione dell'app al webhook della pagina LML. È una scrittura su Meta e si esegue **solo dopo il suo sì**.
2. Configurare il tenant: modulo di prova, modelli approvati, fascia, strategia, conservazione.
3. Fare la prova con 20 contatti finti, di cui almeno 5 di notte o di domenica.
4. Scrivere l'esito.

File: `lml-adv/collaudi/percorso-contatto-<data>.md`
Dipende da: Task 12, Task 13, Task 15, decisioni 19 e 20 di Ivan, modello del primo messaggio approvato da Meta
Verifica: il documento di collaudo riporta i sette punti della Definition of Done n. 2, ciascuno con esito e prova (id del contatto, orari misurati). Se un punto fallisce, la campagna non parte (§26).
Commit: `docs: esito della prova con 20 contatti`

---

## Fuori piano ma urgente

**Recupero dei moduli della campagna dell'agenzia prima del 1 ottobre.** I contatti vivono su Meta per 90 giorni e i più vecchi sono del 3 luglio. Il lavoro è solo in lettura (export dal Centro contatti di Meta) e aggiunge le righe mancanti all'Excel di oggi, così entrano anche nella migrazione del Task 14. Non dipende da nessun task e conviene farlo adesso.
