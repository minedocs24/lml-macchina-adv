---
name: lml-voce-del-settore
description: Raccoglie le parole vere con cui, in un settore di clienti di LML Technologies, il cliente finale descrive il problema e il titolare descrive cosa vuole, cosa teme e cosa lo fa contento — frase per frase, con fonte e data — e le trasforma in una scheda "voce" datata che alimenta la scheda settore, gli angoli e i testi delle inserzioni. Usa SEMPRE questa skill quando l'utente chiede "come lo dicono i clienti", "che parole usano", "le frasi dei clienti", "recensioni del settore", "cosa scrivono nelle recensioni", "il linguaggio del cliente per il settore X", di aggiornare customer-language.md, oppure quando il radar inserzioni di un settore è appena stato fatto e va completato con la voce del cliente — anche se non nomina la skill e dice solo "prima di scrivere le inserzioni sentiamo come parlano". È il secondo anello della catena pubblicitaria LML, subito dopo il radar inserzioni e prima della scheda settore. Solo lettura: non contatta nessuno, non scrive su nessuna piattaforma.
---

# Voce del settore — le parole loro, non le nostre

**Versione 1.0 — 13 settembre 2026.** Skill di sola lettura. Non contatta persone, non scrive su piattaforme, non salva nomi.

## A cosa serve, in una riga

Il test che governa ogni frase pubblicata da LML è: *la scriverebbe un cliente in una recensione?* Questa skill va a prendere quelle frasi **prima** che qualcuno scriva un'inserzione, così il test non si fa a orecchio ma su un elenco.

Il metodo è noto nel mestiere come "message mining" o "review mining" (Joanna Wiebe, Copyhackers; Momoko Price, CXL). L'idea è vecchia e semplice: il cliente ha già scritto il testo migliore, nelle recensioni, nelle lamentele, nelle domande. Il lavoro è trovarlo e non peggiorarlo. La radice accademica è Griffin e Hauser (1993): i bisogni descritti **con le parole del cliente**, non tradotti.

## Le due voci — non confonderle mai

Per ogni settore ci sono due persone diverse che parlano, e servono entrambe:

| Voce | Chi è | Cosa ci dice | Dove si trova |
|---|---|---|---|
| **A — il cliente finale** | Chi chiama il rivenditore, chi prenota dal dentista, chi scrive all'e-commerce | **Il dolore che il titolare riconosce.** *"NON RISPONDONO AL TELEFONO"* è la frase che fa fermare il titolare, perché la teme | Recensioni Google delle attività del settore, in particolare quelle da 1 e 2 stelle |
| **B — il titolare** | Chi compra ARYA | Cosa vorrebbe, cosa teme di un fornitore, cosa dice quando è contento | Recensioni degli strumenti che già usa (segreterie, centralini, gestionali, prenotazioni), forum e gruppi di categoria, **e le fonti nostre** |

La voce A dà i **ganci**. La voce B dà **obiezioni, desideri e le parole del "dopo"**. Un'inserzione ha bisogno di tutte e due: si apre con A e si chiude con B.

## Prima di cominciare — leggi sempre

1. `.agents/customer-language.md` — è la versione attuale della voce, costruita sul mercato e non ancora sui clienti LML. Questa skill la **estende per settore**, non la riscrive.
2. `.agents/product-marketing.md`, sezioni "Problems & Pain Points", "Objections", "Switching Dynamics": dicono cosa cerchiamo di confermare o smentire.
3. `regole-adv.md` §5.1 (il messaggio per i prodotti) e §23 (cosa non si dice mai).
4. Il radar inserzioni del settore, se esiste: `radar/<settore>/` — la sezione "spazio libero" dice quali obiezioni cercare con più attenzione.
5. La scheda voce precedente dello stesso settore, se esiste: `voce/<settore>/`.

Dichiara nella scheda versione e data dei file letti.

## Cosa entra e cosa esce

**Entra:** un settore (uno solo), e — se ci sono — le fonti interne LML disponibili per quel settore (vedi Passo 4).

**Esce:**
- `voce/<settore>/<AAAA-MM-GG>.md`, secondo `references/scheda-voce.md`;
- una sezione "proposte per customer-language.md", **da approvare**: le frasi da aggiungere al documento di riferimento. Non si modifica `customer-language.md` direttamente: sta su un OneDrive condiviso e le modifiche le approva Ivan (CLAUDE.md);
- in chat: dieci righe con la riga secca, le cinque frasi migliori, e cosa manca.

---

## Passo 1 — Scegliere le fonti

Le fonti per settore stanno in `references/fonti.md`. Regola generale: **almeno due fonti per la voce A e almeno due per la voce B**, di tipo diverso. Una sola fonte dà il dialetto di quella piattaforma, non la lingua del cliente.

Per la voce A, le attività da leggere vanno scelte **nel territorio giusto**: Puglia e Sud prima (§4.3), poi il resto d'Italia. Il modo di lamentarsi cambia da regione a regione, e le prime campagne partono da qui.

## Passo 2 — Raccogliere le frasi

Si legge a mano, nel browser. Non si estrae in massa (vedi "Regole vincolanti").

Per ogni frase che vale, annota **quattro cose e basta**:

| Frase | Voce | Tipo di fonte | Data (mese/anno) |
|---|---|---|---|
| "…" | A o B | recensione Google 1★ di un'attività del settore / recensione di uno strumento / forum / nostra | |

**Cosa si prende:**
- la frase **esatta**, virgolettata, anche con gli errori e le maiuscole. Le maiuscole sono informazione.
- se è lunga, si tiene il pezzo che porta il peso, con i puntini per il taglio;
- se serve parafrasare, si scrive `[parafrasi]` accanto. Mai far passare una parafrasi per una citazione.

**Cosa NON si prende, mai:**
- il nome di chi scrive, il nome dell'attività recensita, il luogo preciso, link alla recensione. Si tiene solo il **tipo** di fonte e il mese. La frase serve, la persona no. È la regola che tiene la scheda fuori dai problemi di privacy: una frase senza nessun aggancio a una persona non è un dato personale;
- frasi che descrivono un fatto specifico riconoscibile ("il dottor X mi ha…");
- frasi scritte dal titolare in risposta a una recensione: quella è voce B, e va marcata come tale.

**Quando fermarsi:** quando tre fonti di seguito non aggiungono nessun tema nuovo. Di solito succede fra le 40 e le 80 frasi per settore. Le ricerche di questo tipo non hanno bisogno di grandi numeri: hanno bisogno di **varietà di fonti**.

Segna con un asterisco le frasi che sembrano già un titolo. Sono poche, e sono l'oro.

## Passo 3 — Classificare

Ogni frase va in una **casella sola**, fra cinque:

| Casella | Cosa contiene | Serve per |
|---|---|---|
| **Dolore** | Il problema, detto prima di risolverlo | Il gancio, l'apertura dell'inserzione |
| **Momento** | *Quando* succede: l'ora, il giorno, la situazione | I momenti d'ingresso (§2bis): "il venerdì sera", "alle 23", "mentre sono in sala" |
| **Desiderio** | Cosa vorrebbero, spesso detto in negativo ("basterebbe che…") | La promessa |
| **Dubbio** | Perché non comprano, di cosa non si fidano | Le obiezioni da affrontare, o da evitare |
| **Sollievo** | Come descrivono il fornitore quando funziona | Le parole del "dopo", la chiusura, la prova |

Poi, per ogni casella, **conta le parole**: quali verbi, quali aggettivi tornano più spesso. È da questo conteggio che nascono le liste "parole da usare" e "parole da evitare" di `customer-language.md`. Una parola che compare in una recensione su tre è lingua del cliente; una che non compare mai è lingua nostra.

## Passo 4 — Le fonti nostre

`product-marketing.md` lo dice chiaro: la voce attuale è costruita sul mercato, e va sostituita pezzo per pezzo con le frasi vere di chi lavora con noi. Tre fonti, da leggere **se esistono e se chi le tiene le rende disponibili**:

1. **Le conversazioni di ARYA** dei clienti di quel settore — ogni chat è una registrazione di come il cliente finale descrive il problema. Si leggono con questo scopo, non per il servizio, e se ne prendono solo frasi senza nessun dato della persona.
2. **Il campo "come ci hai conosciuto?"** dell'archivio contatti.
3. **Le risposte a "come ci descriveresti a un collega?"** raccolte a fine progetto o a 90 giorni.

Queste frasi valgono **il doppio** di quelle di mercato, e nella scheda vanno marcate `nostra`. Se non ce ne sono ancora, la scheda lo dice: "fonti interne: nessuna disponibile al <data>".

## Passo 5 — Confronto con quello che crediamo

La scheda chiude con un confronto in tre colonne con `product-marketing.md`:

| Cosa dice product-marketing | Confermato dalle frasi? | Frasi a sostegno o contro |
|---|---|---|

Esempio: product-marketing dice che il primo pensiero del personale è *"mi sostituisce"*. Se in 60 frasi di voce B nessuno lo dice, va scritto: non è che sia falso, ma non lo abbiamo trovato. Se invece lo dicono in dieci, è confermato e abbiamo le parole esatte.

**Quando le frasi smentiscono un'ipotesi del documento di riferimento, non si corregge il documento: si segnala a Ivan** nella sezione "da segnalare". La decisione è sua.

## Passo 6 — Scrivere la scheda

Compila `references/scheda-voce.md`. La sezione "proposte per customer-language.md" è la consegna più importante: sono le righe pronte, nello stesso formato del documento, che Ivan può approvare e incollare.

---

## Regole vincolanti

1. **Mai inventare una frase.** Nemmeno una plausibile, nemmeno per completare una casella vuota. Una casella vuota resta vuota e si scrive "non trovato".
2. **Mai una persona.** Nessun nome, nessuna attività nominata, nessun link alla singola recensione. Tipo di fonte e mese, basta. Se una frase non si può separare dalla persona, non si prende.
3. **Solo lettura, a mano.** Niente estrazioni in massa: le condizioni d'uso delle piattaforme lo vietano, e comunque il metodo non ne ha bisogno. Quaranta frasi lette bene valgono più di quattromila scaricate.
4. **Voce A e voce B separate**, sempre. Mescolarle produce inserzioni che parlano al cliente finale del titolare invece che al titolare.
5. **Le fonti nostre valgono il doppio**, e vanno marcate.
6. **Non si tocca `customer-language.md`.** Si propone, Ivan approva.
7. **Le parafrasi si dichiarano.** `[parafrasi]` accanto alla frase, sempre.
8. **Un settore per esecuzione**, un file datato, mai sovrascritto.

## Cadenza

**Una volta per settore prima di aprirlo**, poi **ogni tre mesi** per i settori aperti — con una differenza: dal secondo giro in poi le fonti nostre (chat ARYA, archivio contatti) pesano più delle recensioni di mercato. L'obiettivo dichiarato in product-marketing è che dopo un anno la voce sia fatta di clienti LML, non di recensioni trovate in giro.

## Dove si scrive

Nella cartella di lavoro `lml-adv`, sotto `voce/`:

```
voce/
  rivenditori/
    2026-09-14.md
    2026-12-14.md
  e-commerce/
    ...
```

Da Cowork si scrive direttamente. Dalla chat del progetto si consegna il file e lo carica l'utente. Vale la regola della cartella: file di appoggio, rilettura, copia sul file buono.

## Cosa fa dopo, e chi

La scheda voce entra nella **scheda settore** insieme al radar. Da lì la **coda degli angoli** prende dolore e momento per i ganci, e il **pacchetto inserzione** prende desiderio e sollievo per promessa e chiusura. Il **collaudo dei testi** usa le liste di parole per dire sì o no a ogni frase.

Va segnalato subito in chat, non solo nella scheda: una frase di voce B che smentisce un'ipotesi di product-marketing; un dubbio ricorrente che nessun materiale LML affronta; una frase di sollievo così buona da essere un titolo.
