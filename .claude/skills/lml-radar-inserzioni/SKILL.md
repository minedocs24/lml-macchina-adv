---
name: lml-radar-inserzioni
description: Studia la Libreria Inserzioni di Meta per un settore di clienti di LML Technologies e produce la scheda "radar" datata — chi paga davvero pubblicità in Italia, con quali messaggi, in quale formato, da quanto tempo, e quale spazio resta libero per noi. Usa SEMPRE questa skill quando l'utente chiede di studiare i concorrenti su Meta, di vedere "cosa fanno gli altri", "chi fa pubblicità" in un settore, "quali inserzioni funzionano", "quale hook usare", "video o statica", "cosa dice la libreria inserzioni", oppure quando parte l'attività programmata "Osservatorio concorrenti", anche se non nomina la skill e dice solo "guardiamo il mercato prima di fare le inserzioni". È il primo anello della catena pubblicitaria LML: precede la scheda settore, la coda degli angoli e ogni testo di inserzione. Solo lettura: non scrive mai su Meta.
---

# Radar inserzioni — cosa pagano davvero i concorrenti

**Versione 1.0 — 13 settembre 2026.** Skill di sola lettura. Non tocca l'account pubblicitario, non spende, non pubblica.

## A cosa serve, in una riga

Le librerie pubblicitarie mostrano **cosa gira**, mai **cosa funziona**. L'unico indizio di funzionamento è **da quanto tempo un'inserzione è in aria**: nessuno paga per mesi una cosa che perde. Questa skill legge quell'indizio in modo sistematico, per un settore alla volta, e lo trasforma in una scheda che le skill successive possono usare senza rileggere la Libreria.

Uno studio di un venditore di strumenti (get-ryze.ai, 2026, su 47.392 inserzioni di 1.247 pagine) dice che solo l'11,3% delle inserzioni supera i 60 giorni. Il numero non è verificato in modo indipendente, ma l'ordine di grandezza regge: **un'inserzione viva da due mesi sta nel decimo che ha superato l'esame di qualcun altro.**

## Prima di cominciare — leggi sempre

1. `regole-adv.md` (radice della cartella `lml-adv`) — in particolare §0.1, §5.1, §22.1, §23, §26.
2. `.agents/product-marketing.md` — la sezione "Competitive Landscape" e la tabella dei concorrenti già visti nella Libreria.
3. `.agents/customer-language.md` — le parole dei clienti, che servono a leggere le inserzioni degli altri con l'occhio giusto.
4. Il radar precedente dello stesso settore, se esiste: `radar/<settore>/` (vedi "Dove si scrive").

Dichiara nella scheda quale versione e quale data hai letto di ciascun file.

## Cosa entra e cosa esce

**Entra:**
- il **settore** (uno solo per esecuzione): uno degli otto target ARYA, oppure "consulenza";
- i **termini di ricerca** per quel settore (se non ci sono, li derivi da `customer-language.md` e dalla §5.1 di regole-adv: parole del cliente, non nostre);
- la **lista delle pagine già note** per quel settore, dal radar precedente.

**Esce:**
- un file datato `radar/<settore>/<AAAA-MM-GG>.md` con la scheda, secondo `references/scheda-settore.md`;
- l'aggiornamento di `radar/<settore>/pagine.md`, la lista di sorveglianza con i numeri delle pagine;
- in chat: una sintesi di dieci righe con la riga secca, le tre cose nuove, e cosa non si è riusciti a vedere.

Nient'altro. Non produce angoli scelti, non produce testi, non decide il formato. Quelle sono le skill successive: questa gli dà i dati.

## Il metodo in due tempi

Lo strumento di ricerca del connettore Meta (`ads_library_search`) e il sito della Libreria Inserzioni fanno due lavori diversi. **Provato sul campo il 13 settembre 2026**, dettagli in `references/libreria-web.md`:

| | Strumento del connettore | Sito della Libreria (browser) |
|---|---|---|
| Trova le pagine che fanno pubblicità | ✅ veloce | lento |
| Testo dell'inserzione | ❌ solo il titolo del pulsante | ✅ |
| Video o immagine | ❌ | ✅ |
| Da quanto è in aria | data di partenza, non se è viva | ✅ "Attiva dal" |
| Ordinare dalle più vecchie | ❌ dà solo le 50 più recenti | ✅ |
| Persone raggiunte e a chi era rivolta | ❌ | ✅ pannello europeo, per legge |

Quindi: **lo strumento trova le pagine, il browser le profila.** Mai il contrario.

---

## Passo 1 — Scoperta: chi paga in questo settore

Con `ads_library_search`, sempre con `countries: ["IT"]` e `ad_active_status: "ACTIVE"`.

Fai **da tre a sei ricerche** per settore, con termini diversi:
- le parole del problema come le dice il cliente (§5.1): *"il telefono squilla"*, *"prenotazioni perse"*, *"risponde anche di notte"*;
- le parole della categoria: *"centralino AI"*, *"assistente telefonico"*, *"chatbot e-commerce"*, *"risponditore automatico"*;
- i nomi dei concorrenti già noti (product-marketing) e delle **alternative economiche** (§Competitive Landscape "Secondari": segreterie telefoniche esterne, centralini cloud, servizi di prenotazione).

Metti i termini fra virgolette per avere la frase esatta: senza, la ricerca restituisce migliaia di risultati che non c'entrano (misurato: 11.558 risultati per una ricerca senza virgolette, con pagine di tutt'altro genere in cima).

Da ogni ricerca prendi **solo il nome e il numero della pagina**. Non giudicare le inserzioni da qui: non si vede abbastanza.

Regola di inclusione di una pagina nella lista di sorveglianza:
- vende qualcosa allo stesso cliente finale del settore (anche se non è AI: una segreteria telefonica esterna è un concorrente di ARYA), **oppure**
- compare in almeno due ricerche diverse.

Scarta le pagine che non c'entrano (nella prova sono uscite pagine di intrattenimento). Segna a parte le **pagine che hanno lo stesso problema che risolviamo noi** ma non sono concorrenti — per esempio uno studio dentistico che fa pubblicità alle prime visite — perché sono clienti potenziali, non avversari.

Aggiorna `radar/<settore>/pagine.md`: aggiungi le pagine nuove con data di primo avvistamento, conferma quelle già note. Non togliere mai una pagina: se non fa più pubblicità, segna "nessuna inserzione attiva al <data>".

## Passo 2 — Profilo: cosa gira e da quanto

Per ogni pagina della lista, apri nel browser la Libreria filtrata su quella pagina:

```
https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IT&is_targeted_country=false&media_type=all&search_type=page&view_all_page_id=<NUMERO_PAGINA>
```

Poi ordina **dalla più vecchia** (ordinamento per data di inizio, crescente) e leggi le inserzioni una per una. Per ciascuna annota, nel formato di `references/scheda-settore.md`:

- numero della Libreria e collegamento;
- **attiva dal** (giorno) e i **giorni in aria** a oggi;
- formato: video, immagine, carosello;
- il **testo** intero, il **titolo**, il **pulsante**;
- dove porta il pulsante: sito, modulo, WhatsApp, Messenger;
- le piattaforme (Facebook, Instagram, altro);
- se l'inserzione è **duplicata** (stesso testo e stessa immagine in più copie): conta le copie, è segno di un'inserzione messa in scala;
- dal **pannello europeo** dell'inserzione: persone raggiunte nell'UE, fasce d'età, genere, zone incluse o escluse.

Se una pagina ha più di 30 inserzioni attive, profila **solo le 15 più vecchie e le 5 più recenti**. Le vecchie dicono cosa regge, le recenti dicono cosa stanno provando adesso.

Un settore tipico ha da 5 a 15 pagine: metti in conto 40-90 minuti di browser. Non è un difetto: è il lavoro.

## Passo 3 — I tre livelli

Ogni inserzione va in uno di tre livelli, **in base ai giorni in aria**:

| Livello | Giorni in aria | Cosa vuol dire |
|---|---|---|
| **Sopravvissuta** | 60 o più | Ha superato l'esame di chi la paga. È la fonte principale della scheda |
| **In scala** | da 14 a 59 | Sta funzionando abbastanza da restare accesa. Vale se ha copie duplicate |
| **Rumore** | meno di 14 | Non si conclude niente. Si registra e basta |

**Non trarre conclusioni dal Rumore**, salvo un caso: lo stesso messaggio nuovo compare da **tre o più pagine diverse** nello stesso mese. Allora non è rumore, è una mossa di mercato, e va segnalata come tale.

Il punto cieco dichiarato: chi prova cinquanta inserzioni brevi e le spegne subito non lascia sopravvissute, e questo metodo non lo vede. Il contro-segnale è la ripetizione fra concorrenti diversi. Scrivilo nella scheda quando sospetti che un concorrente lavori così (molte inserzioni, tutte recenti, poche vecchie).

## Passo 4 — Estrarre gli argomenti, non le creatività

Per ogni inserzione **Sopravvissuta** (e per quelle In scala con copie), compila la riga a quattro colonne:

| Promessa | Obiezione a cui risponde | Prova che porta | A chi parla |
|---|---|---|---|

Esempio, da un concorrente reale già visto (Ambrogio, "Chiamate perse? Basta."):

| Promessa | Obiezione | Prova | A chi |
|---|---|---|---|
| Non perdi più chiamate | "Non rispondo perché sono occupato" | nessuna nel testo | titolari di piccole attività, generico |

**È questa riga che si riusa, mai l'inserzione.** Una cartella di schermate è inutile dopo due settimane; una tabella di argomenti si legge fra sei mesi. E copiare la creatività di un concorrente è un problema legale (§23), oltre che di stile.

Poi raggruppa: quali promesse ricorrono? Quali obiezioni nessuno tocca? Quali prove mancano a tutti?

**Le tre domande che chiudono il passo:**
1. Qual è la promessa più ripetuta fra le Sopravvissute? (È la lingua che il cliente ha già imparato. Non la si evita: la si supera con "e fa", §Competitive Landscape.)
2. Quale obiezione del cliente, fra quelle di `customer-language.md`, **nessun concorrente affronta**? (È lo spazio libero.)
3. Quali prove portano? Nomi di clienti, numeri, demo, prova gratuita? (Dice contro cosa ci confrontiamo: il gratis è lo standard, noi non lo abbiamo.)

## Passo 5 — Formato e destinazione

Dalle sole inserzioni **Sopravvissute**, conta:
- quante video, quante immagini, quanti caroselli;
- quante portano a WhatsApp, quante a un modulo, quante a un sito;
- quante hanno una faccia (il titolare o una persona) e quante no.

Scrivi i numeri, non un'opinione. **Il formato non è una strategia:** quattordici video di un concorrente vogliono dire che il video è un posto dove lui compra, non che sia la mossa giusta. Le fonti di settore si contraddicono su video contro immagine, e nessuna parla di PMI italiane: l'unico dato che vale è questo conteggio, sul nostro settore, nel nostro Paese.

## Passo 6 — Scrivere la scheda

Compila `references/scheda-settore.md` e salvala come `radar/<settore>/<AAAA-MM-GG>.md`.

La scheda si apre con **la riga secca**: una frase che dice cosa è cambiato rispetto al radar precedente, o "primo radar di questo settore". Poi i numeri, poi gli argomenti, poi lo spazio libero, poi "cosa non ho visto".

**Confronto con il radar precedente**, se esiste: ogni inserzione è **nuova**, **in corso** (c'era già), o **spenta** (c'era, non c'è più). Le spente sono preziose: sono le uniche che non si vedranno mai più, e dicono cosa un concorrente ha provato e abbandonato.

### La sezione "Cosa non ho visto" è obbligatoria

Elenca, senza vergogna:
- pagine che non è stato possibile aprire;
- inserzioni senza pannello europeo;
- ricerche che hanno dato troppo rumore per essere usate;
- concorrenti che sospetti esistano e non hai trovato.

Un radar che dichiara i buchi vale più di uno che sembra completo.

---

## Regole vincolanti

1. **Solo lettura.** Nessuna scrittura su Meta. Nessuna esclusa.
2. **Nessuna conclusione sotto i 14 giorni**, salvo la ripetizione fra tre pagine.
3. **Nessun angolo consigliato.** La scheda dice cosa c'è e cosa manca; quale angolo scegliere lo decide la skill successiva, con la prova che LML può portare (§0.1 punto 4).
4. **Argomenti sì, creatività no.** Non si salvano immagini o video dei concorrenti nella cartella. Si salva il collegamento alla Libreria e la riga a quattro colonne.
5. **Non giudicare il budget dal numero di inserzioni.** Una pagina con 40 inserzioni prova tanto; una con 3 sopravvissute da un anno spende bene. Sono cose diverse.
6. **Un settore per esecuzione.** Mescolare i settori nella stessa scheda rende illeggibile la ripetizione fra concorrenti.
7. **Non estrarre in massa.** Lo strumento del connettore vieta l'estrazione a tappeto. Il radar legge quello che serve per una scheda, non scarica la Libreria.
8. **Le inserzioni spente spariscono.** Per le inserzioni commerciali non esiste un archivio: se non è nel nostro radar, è persa. Per questo ogni esecuzione scrive un file datato e non sovrascrive mai il precedente.

## Cadenza

**Ogni mese per i settori aperti**, ogni tre mesi per gli altri. Non meno spesso: i concorrenti cambiano messaggio al ritmo delle loro prove, e un radar trimestrale legge un mercato che si è già mosso. È il compito dell'attività programmata "Osservatorio concorrenti".

Un radar completo su un settore nuovo richiede una sessione lunga. I radar successivi sullo stesso settore sono più brevi: la lista delle pagine c'è già, e si guarda cosa è cambiato.

## Dove si scrive

Nella cartella di lavoro `lml-adv`, sotto `radar/`:

```
radar/
  rivenditori/
    pagine.md            ← lista di sorveglianza, con numeri di pagina e date
    2026-09-13.md        ← scheda datata
    2026-10-13.md
  e-commerce/
    ...
```

Da Cowork si scrive direttamente. Dalla chat del progetto si può leggere OneDrive ma non scriverci: in quel caso la scheda si consegna come file e la carica l'utente. Ricordare la regola della cartella: scrivere su un file di appoggio, rileggerlo, poi copiarlo sul file buono.

## Cosa fa dopo, e chi

La scheda alimenta, nell'ordine: la **scheda settore** (che aggiunge quello che sappiamo noi: casi, partner, capacità di ARYA in quel settore), la **coda degli angoli**, il **pacchetto inserzione**. Nessuna di queste rilegge la Libreria: usano il radar.

Se durante il radar emerge un concorrente nuovo importante, un messaggio che coincide con il nostro, o una prova gratuita nuova, va segnalato subito in chat, non solo nella scheda: sono decisioni di Ivan, non dati.
