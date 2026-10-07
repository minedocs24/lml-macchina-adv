# Glossario LML Technologies

**Versione 1.1 — 14 settembre 2026.** Da aggiornare quando cambia un nome, un prezzo o una regola.

> Documento compagno di [`product-marketing.md`](product-marketing.md).
> **Regola generale: la parola tecnica resta nei documenti interni e nei contratti; al cliente si dice cosa fa.**

---

## 1. Prodotti e nomi

**ARYA** — La suite: il nome che tiene insieme tutti i prodotti in abbonamento. Nei testi si scrive "Arya" o "ARYA", **mai "Aria"** (era solo un espediente di pronuncia per una voce sintetica, ormai abbandonato). *Al cliente:* "il tuo assistente".

**ARYA Voice** — Il modulo voce: risponde al telefono, capisce la richiesta in italiano parlato, prende ordini d'asporto e appuntamenti, riconosce chi ha già chiamato, passa a una persona solo quando serve. Verticali dichiarati: ristorazione, odontoiatria, PA. *Al cliente:* "l'assistente telefonico".

**ARYA Care** — Il modulo customer care: risponde su WhatsApp, Telegram, chat del sito, con lo stesso cervello del modulo voce. Prima era solo Telegram e solo Wix: oggi tutti i canali, qualsiasi e-commerce. **Il nome non è definitivo.** *Al cliente:* "il customer care che risponde anche quando il negozio è chiuso".

**a-Mail (ARYA Mail)** — Il modulo email: legge, smista, risponde e inoltra le email con agenti AI. Si paga **per email elaborata, non per casella**. Tre fasce: Start / Crescita / Impresa. *Al cliente:* "la casella che si svuota da sola".

**Modulo di riconciliazione bancaria** — In sviluppo con un partner albanese: abbina i movimenti bancari alle fatture con l'AI. **Non ancora in vendita.**

**MineDocs** — L'e-commerce di LML per lo studio (panieri e riassunti per università telematiche). Serve anche come negozio fittizio nelle demo e nei video. **Da non confondere con un cliente.**

**Cambiomano** — Piattaforma per il passaggio d'impresa: mette in contatto PMI in vendita e investitori. È un progetto costruito per un cliente, **non un prodotto LML**. Il marchio è del cliente.

**LML RAG, VoiceScribe AI, Cyber-DNA** — Prodotti storici citati nei materiali precedenti (chatbot documentale, trascrizione audio, cybersecurity). **Non sono nel perimetro attuale della comunicazione:** la suite ARYA li ha superati.

---

## 2. Come funziona la piattaforma (termini tecnici)

**Piattaforma multi-tenant** — Un solo software che serve tanti clienti, ognuno chiuso nel proprio spazio. È il motivo per cui il canone può essere basso. *Al cliente non si dice:* si dice "il tuo spazio".

**Tenant** — Lo spazio di un singolo cliente dentro la piattaforma: i suoi dati, il suo catalogo, le sue istruzioni, i suoi numeri. Un cliente può avere più tenant (il rivenditore ne ha due: uno per l'assistenza, uno per i contatti commerciali).

**Istruzioni (prompt)** — Il testo con cui si spiega all'assistente chi è, cosa sa, come si comporta. Ogni tenant ne ha uno solo, valido sia per la voce sia per la chat. **È il cuore della configurazione e lo scrive LML, non il cliente.** *Al cliente:* "gli insegniamo come parlare per te".

**Knowledge base (base di conoscenza)** — I documenti da cui l'assistente pesca le risposte: orari, politiche, FAQ, procedure. Si carica all'attivazione. *Al cliente:* "tutto quello che sa la tua segretaria migliore, scritto una volta".

**Catalogo** — I prodotti o i servizi del cliente caricati nella piattaforma: menù, listino, prestazioni. L'assistente li conosce e li propone.

**Connettore (MCP)** — Il ponte fra l'assistente e i programmi che il cliente usa già: gestionale, agenda, CRM, e-commerce. Con il connettore l'assistente non dice "la richiamiamo": **fa** — mette l'ordine, fissa l'appuntamento, controlla la spedizione. **È la differenza fra ARYA e un risponditore.** MCP è il nome dello standard tecnico; al cliente si dice "collegamento" o "integrazione". Inclusi: 0 in Base, 2 in Pro, 5 o più in Scale.

**Connettore proprietario (personalizzato)** — Quando il gestionale del cliente non ha un connettore già pronto, lo costruisce LML. Voce a parte nel listino.

**Escalation (passaggio a operatore)** — Quando l'assistente non riesce o non deve rispondere, passa la conversazione a una persona, con tutto il contesto. Su Base si fattura 0,15 € a conversazione passata; gratis su Pro e Scale. *Al cliente:* "quando serve, ci sei tu — e trovi già tutto".

**Conversazione risolta** — Una richiesta chiusa dall'assistente senza intervento umano. È l'unità su cui si paga la quota a risultato: **si paga solo quello che l'AI ha fatto da sola.**

**Conversazione chiusa** — Una chat si considera finita dopo **6 ore** di silenzio (prima erano 24). Conta per la fatturazione a conversazione.

**Fasce (Base / Pro / Scale)** — I tre livelli del customer care: **98, 189, 290 €/mese**. Voce e immagini da Pro in su; chiavi AI proprie solo su Scale. I prezzi di listino sono più alti e vengono scontati a questi importi. Le vecchie fasce a conversazioni incluse (1.000 / 3.000 / 10.000) sono superate: **non si vendono pacchetti di conversazioni.**

**Una tantum di attivazione (messa in servizio)** — L'importo iniziale, tenuto volutamente alto rispetto al canone: copre la configurazione, le istruzioni, la base di conoscenza, il catalogo, i test. *Al cliente:* "il lavoro per farlo partire bene".

**Canone** — Il mensile. Copre assistenza LML, aggiornamenti e manutenzione della piattaforma. **Non include conversazioni.**

**Pagamento a risultato (a successo)** — La terza voce del listino: una quota per ogni conversazione risolta dall'AI.

**Onboarding** — L'attivazione di un nuovo cliente: contratto, documento di benvenuto, base di conoscenza, catalogo, numeri, test. Esiste una **procedura standard in sei passaggi**, nata dal primo cliente. *Al cliente:* "l'attivazione".

**Motore AI / modello** — Il cervello che genera le risposte. Gira su un server di LML con una scheda grafica professionale; non dipende da fornitori esterni per i dati. *Al cliente:* "i tuoi dati restano su un server nostro, in Italia".

**RAG** — La tecnica con cui l'assistente pesca nella base di conoscenza prima di rispondere, invece di inventare. **Termine solo interno.**

**LLM** — Il tipo di modello linguistico che sta sotto. **Termine solo interno.** *Al cliente:* "l'intelligenza artificiale".

**Webhook** — Il meccanismo con cui WhatsApp o Telegram consegnano un messaggio alla piattaforma. **Solo tecnico.**

---

## 3. WhatsApp, Meta e canali

**WhatsApp Business (app)** — L'app gratuita che usano le piccole attività sul telefono. Fa poco e non si collega a nulla.

**WhatsApp Cloud API** — La versione "professionale" di WhatsApp che permette a un software come ARYA di rispondere. Serve un account Meta Business e una registrazione del numero. **Ogni cliente paga Meta con il proprio metodo di pagamento, mai con uno di LML.**

**WABA (WhatsApp Business Account)** — L'account WhatsApp aziendale registrato su Meta a cui è agganciato un numero. Un numero, una WABA. La fatturazione si separa per cliente sulla singola WABA.

**Portfolio business (Business Manager)** — Il contenitore Meta dove stanno account, numeri, Pixel e campagne. Il portfolio resta di LML; i clienti stanno dentro come WABA separate. **Verifica dell'azienda: non ancora ottenuta** (prima domanda rifiutata il 12/09/2026, seconda in controllo). Finché non passa, WhatsApp non si attiva.

**Tech Provider** — L'accreditamento che LML ha richiesto a Meta (settembre 2026) per collegare i numeri dei clienti dentro una sola app di piattaforma. **È una scelta irreversibile** e cambia l'architettura: non più un'app Meta per ogni numero, ma una sola app con un instradamento per numero.

**Coesistenza** — La possibilità di tenere lo stesso numero sia sull'app WhatsApp Business sia collegato ad ARYA, con lo storico sincronizzato (180 giorni). Serve per non perdere le chat vecchie quando un cliente attiva l'assistente. Richiede l'accreditamento Tech Provider.

**Embedded Signup** — Il flusso con cui un cliente collega il proprio numero WhatsApp alla piattaforma da solo, dal pannello, senza passare per LML a mano.

**Finestra delle 24 ore** — Su WhatsApp, dopo un messaggio del cliente finale, l'azienda può rispondere liberamente per 24 ore. Passate quelle, serve un template.

**Template (modello di messaggio)** — Un messaggio pre-approvato da Meta che si può mandare fuori dalla finestra delle 24 ore o per primi (ricontatto, promozione, appuntamento). **Il primo contatto in uscita verso un lead richiede sempre un template.**

**Conversazione avviata dall'utente** — Quando è il cliente finale a scrivere per primo (per esempio da un'inserzione che apre WhatsApp): lato WhatsApp è **gratuita da novembre 2024**.

**Inserzione che apre WhatsApp (Click-to-WhatsApp)** — Il formato pubblicitario Meta in cui il clic apre direttamente una chat con il numero dell'azienda. **Non è più il formato scelto per i prodotti:** dal 14 settembre 2026 le inserzioni dei prodotti portano a un **modulo dentro Meta** e ARYA ricontatta su WhatsApp (`regole-adv.md` §3.1).

**Bot Telegram** — Il canale storico della piattaforma; oggi uno dei canali, non l'unico.

---

## 4. Il metodo e la vendita

**Learn · Model · Launch** — **Il nome dell'azienda è il metodo:** capire (analisi), progettare (modello), mettere a terra (rilascio). Nei contenuti si usa come filosofia, non come slogan.

**Metodo LML in 10 fasi** — Il percorso commerciale standard: primo contatto → incontro conoscitivo → avvio analisi → preventivo analisi → analisi → presentazione documento e preventivo sviluppo → negoziazione → contratto → rilascio. Documento interno per la forza vendita.

**Incontro conoscitivo (meeting conoscitivo)** — Il primo appuntamento, **gratuito**. Serve a capire se c'è un problema che vale un'analisi. *Al cliente:* "una chiacchierata di mezz'ora".

**Analisi preliminare** — Il primo passo **a pagamento**: LML entra in azienda, guarda i processi, e consegna un documento con cosa fare e cosa costa. Si vende a ore (da remoto, in presenza o mista) con tariffa fissa. Preventivo dedicato (`Prev_A_`). **È la conversione vera della consulenza.** Regola nuova: deve consegnare anche **il costo annuo del problema in euro**.

**Assessment / AI Readiness Assessment** — L'analisi fatta per reparto (direzione, IT, produzione, amministrazione) per capire dove l'AI serve davvero. Usato con l'azienda di traduzioni. È un'analisi preliminare in versione estesa.

**Documento di analisi** — Il risultato dell'analisi: aree di intervento, impatto, proposta modulare.

**Preventivo modulare** — Il preventivo di progetto diviso in moduli che il cliente può scegliere o fermare (esempio: quattro moduli da 5.000, 12.000, 18.000, 12.000 con possibilità di fermarsi dopo il primo). Codici: `Prev_P_` progetti · `Prev_F_` formazione · `Prev_A_` analisi.

**Fisso più canone** — Ogni progetto su misura ha un prezzo fisso più un canone mensile di manutenzione. **Regola interna: il canone è circa l'1% del fisso al mese** (450 su 45.000), ma si può decidere fuori dalla regola.

**Canone di manutenzione** — Il mensile dei progetti su misura: correzioni, aggiornamenti, assistenza. **È il modo in cui il custom diventa ricorrente.** Durata tipica 3-4 anni.

**Ricorrenti** — **L'obiettivo centrale dell'azienda:** i ricavi che tornano ogni mese. Quattro tipi, con tempi diversi: canone di manutenzione, continuità di consulenza, formazione ricorrente, abbonamento ARYA.

**Milestone (a rilascio)** — Il piano pagamenti standard dei progetti: 30% alla firma, 40% a metà, 30% alla consegna. Oppure pagamenti a rilascio su più release.

**Collaudo** — La verifica finale del cliente prima dell'accettazione. Da lì parte la garanzia (3-12 mesi secondo il progetto).

**One-pager** — La scheda di una pagina che sintetizza il metodo, da allegare alla prima email.

**Presa in carico** — Quando LML prende in gestione una cosa che il cliente aveva già (sito, posizionamento): una tantum piccola più canone pluriennale. Usata col polo universitario (48 mesi).

**MOM, FSD, Process Discovery Report** — Documenti interni di progetto: verbale di riunione, specifica funzionale, rapporto sui processi rilevati. **Non compaiono nella comunicazione esterna.**

---

## 5. Partner, canali, ecosistema

**Partner** — Chi vende o consegna insieme a LML: canale trasversale a prodotti, custom e formazione. Esempio: chi fornisce il gestionale ai ristoranti e ha già dentro i clienti a cui vendere l'assistente telefonico.

**Segnalatore** — Chi porta un contatto in cambio di una provvigione, senza vendere lui. Contratto dedicato.

**Accordo quadro** — Il contratto standard con i partner: rivendita reciproca, integrazione di sistema, sviluppo congiunto. Nato con uno spin-off universitario, replicato con altri.

**White-label (marchio bianco)** — Quando LML eroga qualcosa (per esempio la formazione) con il proprio marchio ma tramite un fornitore esterno, o quando un partner rivende la piattaforma con il suo marchio.

**Formazione** — La terza strada dell'azienda: corsi per manager e per reparti, in tre livelli (Base, Estensione, Sviluppo). Erogata anche tramite un formatore partner. **È la porta d'ingresso naturale quando il freno del cliente è la competenza.**

**Parco clienti installato** — I clienti che un partner ha già dentro il proprio prodotto. **Il canale più economico per i prodotti verticali.**

**Provvigione e sconto (grossup)** — I preventivi incorporano un margine di sconto negoziabile (15%) e una provvigione per il partner (10%), calcolati per divisione e **mai visibili nel documento**.

---

## 6. Bandi e finanza agevolata

**Bando** — Una misura pubblica che finanzia un investimento. A LML interessano quelli su digitalizzazione e AI per le PMI.

**Sportello** — Il bando in cui le domande si presentano in ordine di arrivo finché ci sono fondi: si chiude in ore o giorni. **Le campagne si preparano prima dell'apertura.**

**Voucher** — Un contributo a fondo perduto di importo definito, spesso camerale (Camera di Commercio). Esempio: voucher doppia transizione.

**Fornitore qualificato** — Il ruolo di LML nei bandi dei clienti: il cliente usa il contributo per pagare i servizi LML. **È l'argomento di vendita più forte che esista.**

**Impresa beneficiaria** — Il ruolo di LML nei propri bandi (esempio: la domanda regionale per la suite ARYA). Riguarda l'azienda, non le campagne.

**Startup innovativa** — Lo status di LML (fondata dicembre 2024). Dà accesso a misure dedicate e va citato dove serve credibilità istituzionale.

---

## 7. Marketing e posizionamento

**SEO** — Farsi trovare su Google.
**AIO / AEO** — Farsi citare nelle risposte degli assistenti AI (ChatGPT, Gemini, AI Overview). LML lo vende come servizio e lo fa per sé.

**Personal brand** — Il profilo personale di Ivan come voce pubblica dell'azienda: lo strato della memoria (**parla al 95% che non sta comprando adesso**).

**I tre fronti** — Personal brand, prodotti, consulenza: tre obiettivi con canali diversi, **mai mescolati nella stessa campagna**.

**Momenti d'ingresso** — Le situazioni concrete in cui il titolare pensa al problema ("il telefono squilla a vuoto il venerdì sera"). **I contenuti parlano di quelli, non di "intelligenza artificiale".**

**Contatto qualificato** — Un contatto che rispetta i criteri: azienda italiana, dimensione giusta, chi decide, e — per i prodotti — un volume reale di chiamate o messaggi in entrata.

**Lead magnet** — Un contenuto di valore offerto in cambio di un contatto. Nella roadmap è uno dei canali di acquisizione.

**Prodotto gratuito** — Un elemento fisso della roadmap: qualcosa che LML dà gratis, alimentato dai prodotti e dalla formazione, che rinforza il brand. **Non ancora definito nel dettaglio.**

**Caso studio** — Un cliente vero raccontato con problema, intervento e risultato in numeri. Obiettivo: **uno nuovo ogni due mesi**. Si racconta col nome **solo con autorizzazione scritta**.

---

## 8. Legale e conformità (quello che compare nei contenuti)

**GDPR** — La legge europea sulla privacy. Le soluzioni LML sono "privacy by design"; il DPA (accordo sul trattamento dati) è disponibile su richiesta.

**Titolare e responsabile del trattamento** — Nel canale WhatsApp, l'azienda cliente è il **titolare** dei dati dei suoi clienti; LML è il **responsabile** che li tratta per suo conto. Le pagine legali pubbliche lo dichiarano.

**EU AI Act** — Il regolamento europeo sull'AI. Le soluzioni sono classificate per livello di rischio; nella comunicazione **non si attribuiscono ai sistemi capacità che non hanno**.

**Proprietà del codice** — Nei progetti su misura il codice resta del cliente. Nei prodotti in abbonamento, la piattaforma resta di LML.

**Non riutilizzo, non concorrenza** — Clausole presenti in alcuni contratti di progetto: LML non riusa per altri quello che ha costruito per quel cliente. **Motivo per cui alcuni progetti non sono citabili.**

**NDA** — Accordo di riservatezza, firmato prima dell'analisi approfondita.

**Data residency / on-premise** — La possibilità di tenere i dati in Italia o sul server del cliente. *Al cliente:* "i tuoi dati non escono dall'Italia".
