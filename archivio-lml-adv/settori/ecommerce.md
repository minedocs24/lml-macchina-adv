# Scheda settore — E-commerce con negozio proprio

**Stato:** BOZZA
**Ultimo aggiornamento:** 15 settembre 2026 · **Skill:** `lml-scheda-settore` v2.0 del 14 settembre 2026
**Radar usato:** `radar/panoramica/2026-09-14.md` (panoramica di tutto il mercato). **Un radar dedicato all'e-commerce non esiste.**
**Voce usata:** **nessuna — `voce/ecommerce/` non esiste.**

**Fonti lette:**
- `regole-adv.md` **versione 2.3 del 14 settembre 2026** — §0.1, §2bis, §3.1, §4.2, §5.1, §9, §10.1, §11, §15, §17, §21, §22.1, §23, §26, §27, §28
- `.agents/product-marketing.md` **v1.3, aggiornato il 14 settembre 2026** (nota: il registro delle modifiche in fondo al file si ferma alla v1.2)
- `.agents/glossario.md` **versione 1.1 del 14 settembre 2026** — connettori, fasce, WhatsApp
- `radar/panoramica/2026-09-14.md` — panoramica del 14 settembre 2026 (il file dichiara di aver letto regole-adv v2.1 e product-marketing v1.2)
- `radar/archivio/2026-09-14-rivenditori/2026-09-14.md` — solo la parte sui concorrenti (Spoki), che il file stesso dichiara ancora valida
- `numeri/settimana/2026-09-15.md` e `numeri/direttore/2026-09-15.md` — per lo stato della catena
- Listino ARYA Voice (OneDrive, `Company/Commerciale/Prodotti/Suite ARYA`), pagine 10-11 — il modello del conto della chiamata persa

**Aggiornamenti del 15 settembre 2026, approvati da Ivan, non ancora scritti in `regole-adv.md`** — usati in questa scheda così come dati:
- offerta dichiarata delle inserzioni prodotti: "lascia il numero, ti risponde lei adesso"; demo telefonica di ARYA offerta in chat solo a chi risponde al primo messaggio WhatsApp;
- modulo di tipo "maggiore intenzione", con una sola domanda ("quante chiamate o messaggi ricevi in un giorno?") più il campo libero "come ci hai conosciuto?";
- tetto: **1.000 € per cliente nuovo, 500 € per call fissata**;
- punto debole misurato: da contatto valido a call fissata, **circa 1 su 10**.

### Cosa manca per confermare

| Cosa manca | Chi risponde |
|---|---|
| La voce del settore (`voce/ecommerce/`): senza, i passi 2 e 7 restano vuoti | skill `lml-voce-del-settore` |
| Un radar dedicato all'e-commerce (la panoramica dice solo "zero inserzioni") | skill `lml-radar-inserzioni` |
| Le caselle `[DA CHIEDERE A IVAN]` dei passi 3, 4, 5, 9 e 10 | Ivan |
| La verifica privacy sul messaggio a chi ha lasciato il carrello (passo 3) | chi segue la privacy per LML |
| Il flusso di ricontatto di ARYA provato con 20 contatti finti (§3.1) | Ivan |

---

## 0. In tre righe

Negozi online con un sito proprio, da 5 a 50 persone, che ricevono ogni giorno domande su chat, WhatsApp ed email e le perdono di sera, nel fine settimana e nei giorni di picco. **Nessuna prova di un cliente e-commerce: c'è solo il nostro negozio MineDocs**, e non sappiamo ancora se ARYA ci gira sopra. Nel mercato italiano nessun concorrente fa pubblicità agli e-commerce con inserzioni che durano; però qui l'alternativa economica che legge gli ordini esiste già (i programmi di chat delle piattaforme), e il nostro "rispondiamo e facciamo" pesa meno che altrove. **Non pronti:** manca la voce del settore e mancano le risposte di Ivan su prova e partner.

---

## 1. Il cliente giusto

- **Dimensione:** 5-50 addetti (§4.2). ⚠️ Le imprese italiane di commercio elettronico sono **43.379** nel 2024, più che triplicate in dieci anni, e sono **"prevalentemente micro e piccole imprese"** ([InfoCamere-Unioncamere, luglio 2025](https://www.businessonline.it/news/ecommerce-e-aziende-in-italia-dati-e-statistiche-degli-ultimi-10-anni-da-infocamere-unioncamere_n77832.html)). Quante abbiano almeno 5 addetti **non l'ho trovato**. È probabile che la maggior parte stia sotto: per quelle vale il passo 9, cioè **decide il volume dei messaggi, non il numero di addetti**. `[DA CHIEDERE A IVAN: un negozio con 3 persone e 20 messaggi al giorno è un contatto valido?]` — oggi la §10.1 dice di no.
- **Chi decide:** il titolare, da solo. **Chi risponde oggi:** il titolare stesso dal telefono, oppure una persona che fa insieme spedizioni e assistenza. **Chi subisce e cosa teme:** quella persona — il primo pensiero resta "mi sostituisce" (product-marketing, Personas).
- **Segnale d'acquisto:** non l'interesse per l'AI, ma i messaggi che restano lì la sera e la domenica. **Soglia sotto cui ARYA non serve:** proposta **5 messaggi al giorno**, stima ricavata dal pareggio del passo 2bis `[DA CONFERMARE A IVAN]`.
- **Stagionalità:** il picco è **novembre-dicembre** (Black Friday e Natale), poi i saldi di gennaio e luglio. Ragionamento, non dato misurato: durante il picco il titolare non ha tempo di attivare niente. **Il momento per vendere è prima del picco — settembre e ottobre —** che coincide con i mesi migliori della §15.
- **A chi non vendere:** chi vende solo su Amazon o altri marketplace (il cliente e i messaggi sono del marketplace, non suoi); chi riceve pochi messaggi; chi vuole provare gratis (non c'è prova gratuita); chi ha lo scontrino molto basso e pochi messaggi — il conto del passo 2bis non torna.

---

## 2. I momenti d'ingresso

**Non compilabile: manca la voce del settore.** La skill vieta di inventare i momenti al tavolo (regola 8): ogni momento deve citare una frase vera.

Quello che si può dire già, da fonti che non sono la voce:
- la §5.1 di `regole-adv.md` ha già scritto il momento dell'e-commerce: il carrello che si svuota la sera per una domanda senza risposta. Il passo 2bis qui sotto lo conferma con i dati: è la stessa unità di misura;
- il radar dice che **nessuno** presidia l'e-commerce (0 sopravvissute, 0 in scala). Quando la voce ci sarà, ogni momento frequente cadrà nel quadrante "nessuno lo presidia" — ma leggere il passo 6 prima di festeggiare.

**Momenti tolti per credibilità:** da decidere con la voce.

---

## 2bis. Quanto vale un contatto perso, e contro chi ci confrontiamo

### L'unità giusta: la domanda che arriva prima dell'ordine e resta senza risposta

Nel listino ARYA Voice (pagina 11) l'unità è la **chiamata persa**: "trenta chiamate perse al mese, uno scontrino medio di trentacinque euro, la metà che sarebbe diventata un ordine: 525 euro". Nell'e-commerce il telefono squilla poco. L'unità equivalente è un'altra, e si trova guardando **perché i carrelli si svuotano**.

**Il carrello si svuota spesso per una domanda.** Su 100 carrelli pieni, circa **70** non diventano un ordine (media di 50 studi, [Baymard Institute](https://baymard.com/lists/cart-abandonment-rate)). Il 42% di chi abbandona "stava solo guardando": quello non si recupera. Gli altri se ne vanno per motivi che sono quasi tutti **una domanda**:

| Perché abbandonano (Italia, [Doofinder, luglio 2025](https://www.ninja.it/consumatori-online-nel-2025-lo-studio-di-doofinder/)) | Quota | La domanda che c'è sotto |
|---|---|---|
| Spese di spedizione alte | 55,6% | "quanto costa spedire a …? sopra quale cifra è gratis?" |
| Tempi di consegna lunghi o incerti | 44,1% | "se ordino oggi, arriva entro sabato?" |
| Resi e rimborsi difficili | 38,9% | "se la taglia non va, come faccio il cambio?" |
| Timori sul pagamento | 36,5% | "posso pagare alla consegna / con bonifico?" |
| Sfiducia nel venditore | 31,4% | "ma siete un negozio vero? vi posso chiamare?" |

Nello stesso studio, **il 33,9% degli acquirenti italiani vuole assistenza rapida via chat o WhatsApp**, e il 26,8% un numero di telefono diretto.

**Le due unità, quindi, sono:**

1. **La domanda prima dell'acquisto rimasta senza risposta in tempo.** Chi scrive "arriva entro sabato?" ha già scelto il prodotto. Se la risposta arriva il mattino dopo, ha già comprato altrove. *In tempo* qui vuol dire **entro dieci minuti**: è la soglia che la maggioranza dei clienti considera "risposta immediata" (dato HubSpot riportato da [Gorgias](https://www.gorgias.com/blog/live-chat-statistics) — fonte di un fornitore, da leggere al ribasso).
2. **Il carrello abbandonato di cui il negozio ha il recapito** (email o telefono lasciati al pagamento). Questo si può recuperare **scrivendo per primi** — e scrivere per primi è quello che ARYA fa (passo 3), con un limite di consenso.

La terza richiesta tipica — **"dov'è il mio ordine?"** — non fa perdere l'ordine, che è già pagato. Fa perdere **tempo** e, se resta senza risposta, **la recensione e il secondo acquisto**. Si conta a parte, come costo, non come vendita persa.

### La formula che il titolare rifà con i suoi numeri

```
Ordini che escono dalla porta ogni mese =

    domande prima dell'acquisto rimaste senza risposta entro 10 minuti (al mese)
  × scontrino medio
  × quota che sarebbe diventata ordine

  + carrelli abbandonati di cui hai l'email o il telefono (al mese)
  × scontrino medio
  × quota che un messaggio avrebbe recuperato
```

**Dove trova i suoi numeri:**

| Numero | Dove lo trova | Come |
|---|---|---|
| Domande senza risposta entro 10 minuti | chat del sito, WhatsApp, email, messaggi Instagram | **Contarle per una settimana** e moltiplicare per 4: quelle arrivate la sera, nel fine settimana, o a cui ha risposto dopo più di dieci minuti. Conta solo chi chiedeva qualcosa *prima* di comprare |
| Scontrino medio | il pannello del negozio (valore medio dell'ordine, oppure incasso del mese diviso numero di ordini) | un numero, già calcolato dalla piattaforma |
| Carrelli abbandonati con recapito | il pannello del negozio: su alcune piattaforme c'è una pagina apposta, su altre serve un'estensione | se non li vede, **questa riga non si calcola** — si usa solo la prima |
| Quota che sarebbe diventata ordine | la sua esperienza; in mancanza, i valori prudenti qui sotto | — |

Se ha già le email automatiche che richiamano i carrelli, **nella seconda riga conta solo quelli che le email non recuperano** — noi quella differenza non l'abbiamo mai misurata.

**Se vuole il conto sul guadagno e non sull'incasso**, moltiplica il totale per il suo margine. Nell'e-commerce le spese di spedizione e i resi mangiano molto: il conto sull'incasso da solo esagera.

### Le quote da usare quando il titolare non le sa — **stime**, con il ragionamento

| Quota | Valore prudente | Ragionamento |
|---|---|---|
| Domanda prima dell'acquisto → ordine, se la risposta arriva subito | **20%** (forchetta 10-30%) | Nel listino Voice, per la telefonata al ristorante, si usa il 50%. Online è più bassa: il concorrente è a un clic, e una parte di chi chiede sta solo confrontando (il 42% degli abbandoni è "stavo solo guardando", Baymard). I fornitori di chat dicono che chi usa la chat compra 2,8 volte più spesso degli altri ([Gorgias](https://www.gorgias.com/blog/live-chat-statistics), che cita un altro fornitore): numero non verificabile, non lo usiamo |
| Carrello abbandonato → recuperato con un messaggio | **5%** | Le email automatiche di recupero portano a un ordine nel **3,3%** dei casi in media e nel **7,7%** per i negozi migliori (143.000 flussi, dati 2023, [Klaviyo](https://www.klaviyo.com/blog/abandoned-cart-benchmarks)). Un messaggio che risponde alla domanda dovrebbe fare meglio di un'email, ma **nessuno l'ha misurato per noi**: si resta a metà fra media e migliori |

### Lo scontrino medio, per comparto — dato misurato

Osservatorio eCommerce B2c Netcomm-Politecnico di Milano, 2026 ([comunicato del 28 maggio 2026](https://www.giornaledellepmi.it/lecommerce-b2c-di-prodotto-in-italia-nel-2026-raggiunge-i-426-miliardi-di-euro-6-rispetto-al-2025/); [Osservatori.net](https://www.osservatori.net/comunicato/ecommerce-b2c/ecommerce-b2c-di-prodotto-in-italia/)):

| Comparto | Scontrino medio | **Valore di una domanda persa** (× 20%, stima) | Domande perse al mese che pagano il canone Pro da 189 € (sull'incasso) |
|---|---|---|---|
| Bellezza e farmacia | 37 € | **7,40 €** | 26 (quasi una al giorno) |
| Abbigliamento | 115 € | **23,00 €** | 9 |
| Enogastronomia | 136 € | **27,20 €** | 7 |
| Arredamento e casa | 152 € | **30,40 €** | 7 |
| Informatica ed elettronica | 213 € | **42,60 €** | 5 |

Sull'incasso il canone si ripaga con pochissime domande. **Sul guadagno il conto cambia:** con un margine del 30% (ipotesi dell'esempio, non un dato) servono circa 28 domande perse al mese nell'abbigliamento e **86 nella bellezza** — quasi tre al giorno. Nell'elettronica i margini sono di solito più bassi del 30%: lì il conto va fatto solo con il margine vero del titolare.

Perché il canone di riferimento è Pro e non Base: per dire a che punto è un ordine o se un prodotto c'è, ARYA deve essere collegata alla piattaforma del negozio, e **la fascia Base non include collegamenti** (glossario: 0 in Base, 2 in Pro, 5 in Scale). È una deduzione dal glossario `[DA CONFERMARE A IVAN: per un e-commerce la fascia minima è Pro?]`. Al canone va aggiunta l'attivazione una tantum, di cui questa scheda non ha l'importo per ARYA Care `[DA CHIEDERE A IVAN]`.

### Un esempio fatto con la formula — esempio, non dato

Negozio di abbigliamento, 8 persone. In una settimana conta 10 domande arrivate la sera o nel weekend, quindi **40 al mese**. Il pannello gli mostra **100 carrelli abbandonati al mese** con l'email lasciata.

| Riga | Conto | Ordini persi al mese |
|---|---|---|
| Domande senza risposta | 40 × 115 € × 20% | **920 €** |
| Carrelli con recapito | 100 × 115 € × 5% | **575 €** |
| **Totale sull'incasso** | | **1.495 €** |
| Sul guadagno, se il margine è il 30% | 1.495 € × 30% | **circa 450 €** — più del doppio del canone Pro |

Con le quote alla forchetta bassa (10% e 3%) la prima riga scende a 460 €. **Il conto va fatto con i numeri suoi, davanti a lui, prima di dire il prezzo** — come dice pagina 11 del listino Voice.

### Quanto vale un cliente nel tempo

La formula conta **un ordine solo**: è la versione prudente. Chi ricompra vale di più (scontrino × ordini in un anno × anni). **Non ho trovato un dato italiano affidabile su quante volte ricompra il cliente di un e-commerce: non lo stimo.** Si chiede al titolare nella call.

### Che cosa serve sapere per rispondere

| Tipo di richiesta | Per rispondere basta… | Chi altro può farlo, e a quanto |
|---|---|---|
| "quanto costa la spedizione, come si fa il reso, posso pagare alla consegna" | **le regole del negozio**, scritte una volta | la risposta automatica di WhatsApp Business (gratis, ma un messaggio fisso e poi niente); i programmi di chat delle piattaforme, alcuni gratuiti; Tidio da 29-59 $ al mese, con la parte automatica da 39 $ al mese per 50 conversazioni ([Chatarmin, 2026](https://chatarmin.com/en/blog/tidio-pricing)) |
| "c'è la taglia M, arriva entro sabato, è compatibile con…" | **il catalogo e le giacenze della piattaforma** | gli stessi programmi di chat, se il titolare li configura; Tidio mostra lo stato dell'ordine nella chat dal piano Growth |
| "dov'è il mio ordine, l'ho ricevuto rotto, cambio l'indirizzo" | **la piattaforma e il corriere, collegati** | programmi di assistenza fatti per l'e-commerce (in inglese, configurati dal titolare); un addetto |
| scrivere per primi a chi ha lasciato il carrello | **il recapito, il consenso, la piattaforma** | le email automatiche di recupero, spesso già incluse; Spoki per le campagne WhatsApp (passo 6) |
| rispondere al telefono | tutto quanto sopra, a voce | una persona |

**La regola, scritta come la vuole la skill:**

> Dove per rispondere basta prendere un messaggio, una persona vera costa quanto noi e ispira più fiducia. Dove per rispondere bisogna sapere qualcosa, non c'è confronto.

**Nell'e-commerce la regola va letta con una correzione, e va detta.** Qui quasi tutte le richieste stanno nella seconda riga — bisogna sapere qualcosa — e questo è un bene: ARYA ha già tutte le piattaforme e-commerce collegate (Ivan, 14 settembre). **Ma nell'e-commerce il concorrente che "sa qualcosa" esiste già e costa poco:** sono i programmi di chat collegati alla piattaforma. Il confronto di prezzo che il titolare ha in testa non è la segretaria esterna da 39 €: è il programma di chat da 30-100 € al mese. **Su "risponde e sa dov'è l'ordine" vendiamo in salita.** Dove non c'è confronto è altrove: **la configurazione la facciamo noi** (quei programmi la lasciano al titolare, che non la fa — product-marketing, "Dove cascano"), **lo stesso assistente su chat, WhatsApp, email e telefono**, e **il messaggio in uscita a chi ha lasciato il carrello**.

### Il conto dall'altra parte: quanto possiamo pagare noi

Con il tetto approvato il 15 settembre — **500 € per call fissata** — e il passaggio misurato da contatto valido a call di **circa 1 su 10**, un contatto valido di questo settore non può costarci più di **50 €**. Il giorno che il passaggio sale a 2 su 10, il tetto per contatto valido sale a 100 €. È il numero da migliorare prima di tutti gli altri, e la formula qui sopra è lo strumento che lo migliora: **dà ad ARYA, in chat, un motivo concreto per fissare la call** ("facciamo il conto con i tuoi numeri").

---

## 3. Cosa fa ARYA in questo settore — risposte di Ivan del 14 settembre 2026

Roberto non segue questo progetto: le risposte tecniche su ARYA le dà Ivan. Valgono per tutti i settori finché non cambiano.

| Promessa (nelle parole del cliente) | Si può fare oggi? | Con quale prova | Dove sta il limite |
|---|---|---|---|
| risponde anche di sera e la domenica | **sì** | nessuna di un e-commerce; Mr. Toner in produzione (**altro settore**) | — |
| risponde in meno di un secondo | **sì, solo se il valore di oggi lo conferma** | tempo misurato dentro ARYA (Ivan) | product-marketing: il giorno che sale, la frase si toglie. `[DA CHIEDERE A IVAN: valore attuale e se è misurato di continuo]` |
| ti dice a che punto è il tuo ordine | **sì** | nessuna in produzione su un e-commerce | il negozio deve dare l'accesso alla sua piattaforma; il dettaglio della spedizione dipende da cosa espone il corriere |
| ti dice se il prodotto c'è e quanto costa | **sì** | nessuna | vale quanto è aggiornato il catalogo della piattaforma |
| risponde su WhatsApp, Telegram, chat del sito ed email | **sì** | — | la chat Instagram e Messenger non sono nelle risposte del 14 settembre `[DA CHIEDERE A IVAN]` |
| risponde anche al telefono | **sì** | — | voce da Pro in su (glossario) |
| riconosce il cliente che ha già comprato | **sì** | — | tramite la piattaforma collegata |
| passa a una persona con tutto quello che è stato detto | **sì** | Mr. Toner (**altro settore**) | — |
| cambia l'indirizzo, apre il reso, annulla l'ordine | **sì, dove la piattaforma lo permette** | nessuna | sono modifiche agli ordini: **decide il titolare** quali lasciargliene fare |
| scrive a chi ha lasciato il carrello | **dipende** | nessuna | ARYA legge i contatti e li contatta (Ivan). Ma su WhatsApp serve il **consenso** della persona e un messaggio approvato da Meta (glossario); chi non ha comprato non è ancora un cliente, e scrivergli senza consenso è un rischio privacy. **`[DA VERIFICARE con chi segue la privacy]`** |
| "aumenta le vendite del X%", "recupera X carrelli su 10" | **no** | nessun numero misurato | §23: niente risultati promessi senza un caso documentato |

**Collegamenti esistenti:** tutte le piattaforme e-commerce (Ivan, 14 settembre). Quali siano per nome non è scritto `[DA CHIEDERE A IVAN: l'elenco, per poterle nominare]`.
**Collegamenti da costruire:** i gestionali di magazzino dietro al negozio, "qualche ora" ciascuno.
**Cosa non fa ancora e non si promette:** niente di nuovo rispetto alla tabella; la colonna "no" e le celle "dipende" non entrano in nessuna inserzione.
**Quello che resta da verificare negozio per negozio:** se la piattaforma del cliente dà l'accesso, e se il titolare ha le credenziali. Per le piattaforme più diffuse l'accesso di solito si genera dal pannello; per i siti fatti su misura da un'agenzia dipende dall'agenzia.

---

## 4. Le prove

| Prova | Tipo | Stato del consenso | Numeri disponibili | Forma anonima |
|---|---|---|---|---|
| MineDocs | **nostro negozio, non un cliente** | — | `[DA CHIEDERE A IVAN: ARYA risponde sul sito o sul WhatsApp di MineDocs? Da quando?]` | non serve: è nostro, si può dire "l'abbiamo messa prima sul nostro negozio online" |
| Mr. Toner | cliente in produzione, **altro settore** — si cita come "abbiamo già fatto", mai come "per uno come te" | nome mai usato (decisione del 14/09/2026) | dei cinque numeri della product-marketing, nessuno risulta raccolto | "un rivenditore di consumabili in Puglia, una decina di persone" |
| Registrazione della voce vera | demo | — | `[DA CHIEDERE A IVAN: esiste?]` | — |

**Nessuna prova di questo settore. Le inserzioni possono solo mostrare il prodotto che funziona.**

**La prova più utile da costruire è MineDocs**, perché permette di rifare la formula del passo 2bis con numeri veri: domande arrivate fuori orario in una settimana, scontrino medio, carrelli abbandonati. Se ARYA non ci gira ancora, **contare prima di attivarla** dà il "prima" del caso (product-marketing, Proof Points).

---

## 5. Il partner

- **Esiste un partner con parco clienti in questo settore?** `[DA CHIEDERE A IVAN]`. I candidati naturali sono **le agenzie che costruiscono e mantengono negozi online** (hanno dentro l'elenco dei clienti e la loro fiducia), i fornitori di spedizioni e pagamenti, le associazioni di categoria del commercio elettronico.
- **Chiesto ai partner dell'accordo quadro se servono l'e-commerce?** `[DA CHIEDERE A IVAN — data e risposta]`
- **Decisione:** Meta come supporto / Meta a pieno regime — `[DA CHIEDERE A IVAN]`

Da tenere presente: tre concorrenti hanno aperto nello stesso mese un programma per rivenditori (radar panoramica, §12). Il canale partner che la §22.1 mette prima della pubblicità se lo stanno costruendo gli altri.

---

## 6. Concorrenti e alternative

**Nel radar, nessuna inserzione sopravvissuta né in scala è rivolta all'e-commerce** (panoramica del 14/09, tabella 5ter). La panoramica stessa avverte: può voler dire che nessuno ci ha provato, o che qualcuno ha provato e ha smesso. Con il conto del passo 2bis in mano, la lettura più probabile è la prima **per gli assistenti telefonici** (nell'e-commerce il telefono conta poco) e la seconda **non si può escludere per le chat**, che hanno già strumenti economici dentro le piattaforme.

| Chi | Promessa più ripetuta | Cosa regala | Dove casca rispetto a noi |
|---|---|---|---|
| **Spoki** — l'unico che parla agli e-commerce, sopravvissuta da 125 giorni (radar rivenditori, parte concorrenti) | "fai pubblicità su WhatsApp, vendi di più" — "+30% vendite", "oltre 4.000 ecommerce e negozi" | prova gratuita | vende **campagne in uscita**, non risposte: il messaggio parte, la domanda che torna indietro resta al titolare |
| **Tidio** (e simili) — in product-marketing fra i concorrenti diretti, **invisibile nella Libreria Inserzioni** | chat con risposte automatiche collegata al negozio | piano gratuito | la configurazione la fa il titolare; la parte automatica si paga a pacchetti di conversazioni; non prende il telefono |
| **DeepAgent** — il concorrente più attrezzato del radar, non ancora sull'e-commerce | "lo configuriamo noi", "agisce dentro il gestionale" | setup gratuito dichiarato da 2.000 € | se apre un verticale e-commerce, dice le nostre stesse cose con un regalo in più. **Da sorvegliare** |

| Alternativa che sembra ragionevole | La frase che la smonta |
|---|---|
| persona part-time | copre 20 ore su 168; la sera e la domenica, quando arrivano le domande, non c'è (product-marketing) — frase del cliente: *da raccogliere nella voce* |
| servizio clienti esterno con persone | costo e orari **non verificati** per l'e-commerce `[da cercare nella voce]` |
| risposta automatica di WhatsApp Business | manda un messaggio fisso, poi niente |
| programma di chat della piattaforma | **è il confronto vero di questo settore** (passo 2bis): costa poco, legge gli ordini, ma va configurato e seguito dal titolare |
| email automatiche di recupero carrello | spesso già attive: recuperano 3-8 carrelli su 100; non rispondono alla domanda che ha fatto abbandonare |

---

## 7. Le obiezioni di questo settore

**Non compilabile: manca la voce del settore.** La skill chiede le obiezioni dalla casella "Dubbio" della voce, non dalla lista generica.

Due obiezioni che il passo 2bis fa prevedere, **da verificare nella voce** e oggi **senza una risposta nei materiali LML**:
- *"Ho già la chat della piattaforma, gratis."*
- *"Le email per i carrelli le mando già."*

---

## 8. Il formato

- **Sopravvissute nel radar (tutti i settori, pagine nuove della panoramica):** video 7 · immagini 2 · caroselli 0 · con una faccia 2 su 2 misurate (le altre 7 non misurate). **Rivolte all'e-commerce: 0.**
- **Risorse nostre già pronte:** MineDocs come negozio da mostrare nelle demo e nei video (glossario) · registrazione della voce di ARYA `[DA CHIEDERE A IVAN]` · video di Ivan `[DA CHIEDERE A IVAN]`
- **Scelta di partenza e motivo:** video verticale con la faccia di Ivan (§18, §2bis "segni distintivi"), perché nel radar i formati che durano sono in maggioranza video e nessuna prova di settore è disponibile da raccontare. Per l'e-commerce il prodotto si mostra meglio **sullo schermo del telefono** (la chat che risponde) che al telefono. — *la decide la spesa, non questa scheda.*

---

## 9. Prezzo e qualificazione

- **Fascia di prezzo da dire in inserzione:** `[DA CHIEDERE A IVAN]` — se Pro è la fascia minima per un e-commerce (passo 2bis), il prezzo da dire è 189 €, non 98 €.
- **La domanda che qualifica** (nel modulo, dal 15/09): "Quante chiamate o messaggi ricevi in un giorno?" — soglia proposta: **5 al giorno** — stima: nell'abbigliamento, con margine al 30%, il canone si ripaga con circa una domanda persa al giorno; se una domanda su cinque arriva fuori orario o riceve risposta tardi (ipotesi, non misurata), servono circa 5 messaggi al giorno in tutto `[DA CONFERMARE A IVAN]`. Nella bellezza e farmacia, con lo scontrino a 37 €, la soglia andrebbe alzata.
- **Le tre domande della chat** (§3.1), adattate — servono a rifare la formula con i numeri del titolare e a dare ad ARYA un motivo per fissare la call:
  1. Da dove arrivano i messaggi, e quanti arrivano la sera o nel fine settimana?
  2. Su che piattaforma è il negozio?
  3. Qual è più o meno lo scontrino medio?

---

## 10. I cancelli

| Condizione | Stato | Note |
|---|---|---|
| Radar da meno di 30 giorni | **in parte** | panoramica del 14/09 sì; radar dedicato all'e-commerce no |
| Voce fatta | **no** | `voce/ecommerce/` non esiste |
| Cosa fa ARYA: confermato | **sì** | da Ivan il 14/09 (Roberto non segue il progetto); restano le caselle aperte del passo 3 |
| Almeno una prova del settore, o decisione di partire senza | **no** | nessuna prova; `[DA CHIEDERE A IVAN: si parte mostrando solo il prodotto? sì / no / dopo MineDocs]` |
| Partner verificato (§22.1) | **no** | `[DA CHIEDERE A IVAN]` |
| Settore riconosciuto nella §10.1 | **sì** | settore n. 1, referenza MineDocs. Da decidere se valgono anche i negozi sotto i 5 addetti |
| Chi risponde ai contatti e in quanto tempo (§11) | **no** | il primo contatto lo fa ARYA su WhatsApp, ma il flusso non è ancora provato con 20 contatti finti (§3.1, §26). Oggi i contatti delle campagne dell'agenzia sono richiamati in media dopo 24,6 ore. La persona che chiama dopo ARYA: Brian Razzi (§11) — l'archivio è accessibile solo a Ivan |
| Massimo due campagne attive (§0.1) | **sì** | zero campagne su lml-adv (report del 15/09) |

**Esito: BOZZA.** Quattro caselle su otto sono "no" o "in parte".

---

## 11. Da segnalare a Ivan

1. **Mancano la voce e il radar dedicato all'e-commerce.** Questa scheda li anticipa sulla parte economica, che non dipende da loro; i momenti d'ingresso e le obiezioni restano vuoti finché non ci sono.
2. **L'unità della richiesta persa nell'e-commerce è la domanda prima dell'ordine senza risposta entro 10 minuti, più il carrello abbandonato con recapito.** Coincide con la frase che la §5.1 aveva già scritto per l'e-commerce: i dati la confermano.
3. **Il "rispondiamo e facciamo" qui vale meno che negli altri settori.** Nell'e-commerce esistono già programmi di chat economici che leggono gli ordini. Il confronto di prezzo del titolare è con loro, non con una segretaria. Dove non c'è confronto: configurazione fatta da noi, stesso assistente su tutti i canali compreso il telefono, messaggio in uscita a chi ha lasciato il carrello.
4. **Il messaggio a chi ha lasciato il carrello è la promessa più forte e la più fragile:** senza consenso non si può mandare. Va verificata con chi segue la privacy **prima** di entrare in qualunque materiale.
5. **La fascia minima per un e-commerce sembra Pro (189 €), non Base (98 €),** perché Base non include collegamenti. Cambia il prezzo da dire in inserzione e il conto del pareggio.
6. **Nella bellezza e farmacia il conto regge a fatica** (scontrino medio 37 €: servono quasi tre domande perse al giorno per ripagare il canone sul guadagno). Se si apre l'e-commerce, meglio i comparti con scontrino sopra i 100 €.
7. **MineDocs può diventare la prima prova vera in pochi giorni:** contare per una settimana le domande fuori orario e i carrelli abbandonati, poi attivare ARYA e rifare il conto.
8. **Il momento per vendere all'e-commerce è adesso, settembre-ottobre, prima del picco di novembre-dicembre.** Se la scheda non si chiude entro ottobre, la finestra naturale si sposta a gennaio.

---

## 12. Storico

| Data | Cosa è cambiato | Chi |
|---|---|---|
| 15/09/2026 | Prima stesura, in BOZZA. Compilato per primo il passo 2bis (conto della richiesta persa) su richiesta di Ivan, con i dati di mercato e gli aggiornamenti del 15 settembre. Passi 2 e 7 vuoti per mancanza della voce del settore | Claude, su richiesta di Ivan |
