# Scheda settore — Strutture extra-alberghiere (B&B, case vacanza, piccoli hotel)

**Stato:** BOZZA
**Ultimo aggiornamento:** 15 settembre 2026 · **Skill:** `lml-scheda-settore` v2.0 del 14 settembre 2026
**Radar usato:** `radar/panoramica/2026-09-14.md` (panoramica di tutto il mercato). **Un radar dedicato al ricettivo non esiste.**
**Voce usata:** **nessuna: `voce/ricettivo/` non esiste.**

**Fonti lette:**
- `regole-adv.md` **versione 2.3 del 14 settembre 2026**: §0.1, §2bis, §3.1, §4.2, §5.1, §9, §10.1, §11, §15, §21, §22.1, §23, §26, §27
- `.agents/product-marketing.md` **v1.3, aggiornato il 14 settembre 2026** (il registro delle modifiche in fondo si ferma alla v1.2). Sul ricettivo non contiene nulla di specifico
- `.agents/glossario.md` **versione 1.1 del 14 settembre 2026**: connettori, fasce, WhatsApp
- `radar/panoramica/2026-09-14.md` e `radar/panoramica/pagine.md` del 14 settembre 2026: Readygoone, Hostley
- `settori/ecommerce.md` (BOZZA del 15 settembre 2026), per il confronto del passo 2bis
- Listino ARYA Voice, pagina 11: il modello del conto della chiamata persa

**Aggiornamenti del 15 settembre 2026, approvati da Ivan e non ancora scritti in `regole-adv.md`.** Questa scheda li usa così come sono stati dati:
- **Offerta** delle inserzioni prodotti: "lascia il numero, ti risponde lei adesso". La demo telefonica di ARYA si offre in chat solo a chi risponde al primo messaggio WhatsApp.
- **Modulo** di tipo "maggiore intenzione", con una sola domanda ("quante chiamate o messaggi ricevi in un giorno?") più il campo libero "come ci hai conosciuto?".
- **Tetto di spesa:** **1.000 € per cliente nuovo, 500 € per call fissata**.
- **Punto debole misurato:** da contatto valido a call fissata passa **circa 1 contatto su 10**.

### Cosa manca per confermare

| Cosa manca | Chi risponde |
|---|---|
| La voce del settore (`voce/ricettivo/`). Senza, i passi 2 e 7 restano vuoti | skill `lml-voce-del-settore` |
| Un radar dedicato al ricettivo | skill `lml-radar-inserzioni` |
| Le caselle `[DA CHIEDERE A IVAN]` dei passi 1, 3, 4, 5, 9 e 10 | Ivan |
| Il flusso di ricontatto di ARYA provato con 20 contatti finti (§3.1) | Ivan |

---

## 0. In tre righe

Si vende a strutture ricettive che ricevono richieste di disponibilità al telefono, su WhatsApp e per email, e le perdono quando il titolare è fuori, di notte o in alta stagione. **Non abbiamo nessuna prova di questo settore.** Il valore in gioco è alto: una richiesta persa vale **30-55 €** (stima), perché dietro c'è un soggiorno da **270-560 €**, e una camera rimasta vuota non si recupera il giorno dopo. Il confronto di prezzo qui **non è con un programma di chat economico come nell'e-commerce**:
- nel piccolo B&B è con il titolare stesso, che non costa niente;
- nel piccolo hotel è con una persona in reception.

Il limite vero è un altro: per rispondere "c'è posto?" ARYA deve leggere il calendario, e molte piccole strutture non ne hanno uno collegabile. **Non siamo pronti:** mancano la voce del settore e le risposte di Ivan.

---

## 1. Il cliente giusto

- **Dimensione.** Il settore è fatto quasi tutto di strutture sotto i 5 addetti. In Italia ci sono **232.376 esercizi extra-alberghieri**, e sono esercizi, non imprese:
  - 156.398 alloggi in affitto gestiti come impresa;
  - 35.015 B&B;
  - 21.215 agriturismi.
  
  Gli alberghi sono **32.943** ([ISTAT, Annuario 2025, dati 2024](https://www.istat.it/storage/ASI/2025/capitoli/C19.pdf)). In Puglia gli esercizi extra-alberghieri sono **9.063**: 5.001 appartamenti in affitto, 3.033 B&B, 774 agriturismi. Gli hotel sono **1.070**. La provincia di Bari da sola ha 2.560 strutture extra-alberghiere ([dati ISTAT elaborati dall'Osservatorio Aforisma, agosto 2024](https://www.statoquotidiano.it/03/08/2024/in-puglia-oltre-10mila-strutture-alberghiere-ed-extra-alberghiere-posti-letto-a-quota-302mila/1125788/)).
  
  **Ragionamento, non dato:** dentro la soglia dei 5-50 addetti della §10.1 stanno soprattutto due figure:
  - **il piccolo hotel**, da 10 a 40 camere;
  - **chi gestisce molte case vacanza**, anche per conto di altri proprietari.
  
  Sono anche quelli con più richieste e più lingue. Il B&B familiare con 3 camere resta sotto la soglia. `[DA CHIEDERE A IVAN: il B&B sotto i 5 addetti ma con molte richieste in stagione è un contatto valido?]`
- **Chi decide:** il titolare, da solo. Nelle case vacanza gestite per conto terzi decide il gestore, non il proprietario.
- **Chi risponde oggi:**
  - nel B&B, il titolare dal cellulare, spesso mentre fa altro, a volte mentre fa un altro lavoro;
  - nel piccolo hotel, la reception di giorno; la notte rispondono il portiere notturno, la segreteria o nessuno.
- **Chi subisce e cosa teme:** il receptionist teme "mi sostituisce". Il titolare del B&B non teme per il posto di lavoro: teme che l'ospite senta una macchina invece di lui (ragionamento, da verificare con la voce).
- **Segnale d'acquisto:** le richieste che arrivano mentre il titolare non può rispondere, e le prenotazioni che finiscono sul portale con la commissione.
- **Soglia sotto cui ARYA non serve:** proposta **3 richieste al giorno in alta stagione** `[DA CONFERMARE A IVAN]`. È una stima ricavata dal pareggio del passo 2bis: servono circa 70 richieste perse all'anno in un B&B, e si ipotizza, senza averlo misurato, che una richiesta su quattro vada persa.
- **Stagionalità:** per la Puglia l'alta stagione va da giugno a settembre. Le prenotazioni dell'estate arrivano da gennaio a maggio. **Ragionamento, non dato misurato:** a settembre il titolare pugliese è ancora dentro la stagione e non ha tempo. Ha la testa libera **da metà ottobre a marzo**, cioè quando prepara la stagione e riceve le richieste per l'estate. Questo non coincide con la §15, che mette settembre come mese migliore per tutto il B&B italiano. `[DA DECIDERE CON IVAN: per il ricettivo la finestra di partenza è ottobre-marzo?]`
- **A chi non vendere:**
  - chi riceve tutte le prenotazioni dal portale e nessuna richiesta diretta, perché lì c'è poco da recuperare;
  - chi ha una o due unità e poche richieste;
  - chi tiene il calendario su carta o solo dentro il portale, se la promessa è "ti dice se c'è posto" (passo 3);
  - chi vuole provare gratis.

---

## 2. I momenti d'ingresso

**Non compilabile: manca la voce del settore.** La skill vieta di inventare i momenti al tavolo (regola 8).

Quello che si può già dire, da fonti diverse dalla voce:
- **Hotel.** La panoramica trova **4 inserzioni sopravvissute** rivolte agli hotel, tutte di **Readygoone**, in aria da **139 giorni**. Usano i momenti "quante richieste si fermano prima di diventare prenotazioni", "quanto tempo perde il tuo staff a ripetere le stesse informazioni" e "rispondi a tutti, in ogni lingua, 24 ore su 24". Nella griglia della skill questi momenti stanno nel quadrante **"lo presidiano in 1-2"**: si entra solo con il "e fa".
- **B&B e case vacanza.** Readygoone parla a "proprietari o direttori di hotel", non a chi ha un B&B o una casa vacanza. **Per questi due segmenti il radar non trova nessuno.** Da verificare con un radar dedicato.
- La §10.1 dice che queste strutture "lavorano su WhatsApp": è l'unico indizio già scritto nei nostri documenti.

**Momenti tolti per credibilità:** si decidono con la voce. Un candidato evidente è "l'ospite vuole parlare con il titolare in persona", tipico del B&B familiare.

---

## 2bis. Quanto vale un contatto perso, e contro chi ci confrontiamo

### L'unità giusta: la richiesta di disponibilità rimasta senza risposta

Qui l'unità torna vicina a quella del listino Voice. Là l'unità è la chiamata persa del ristorante: "trenta chiamate perse al mese, uno scontrino medio di trentacinque euro, la metà che sarebbe diventata un ordine: 525 euro". Qui è **la richiesta "c'è posto dal 12 al 15?" arrivata al telefono, su WhatsApp o per email, a cui nessuno risponde in tempo.** Rispetto al ristorante cambiano due cose.

1. **Lo scontrino è un soggiorno, non una cena.** Vale diverse notti, non una.
2. **Chi chiede scrive a più strutture insieme** e prenota con chi risponde per primo, oppure va sul portale.
   
   Le strutture italiane rispondono tardi. Su un campione di 5.000 hotel il tempo medio di risposta a una richiesta di prenotazione è di **1 giorno e quasi 4 ore** ([AlbergatorePro](https://www.albergatorepro.com/blog/tempo-medio-risposta-richiesta-prenotazione): fonte di un fornitore, campione e data non dichiarati, da leggere con cautela).
   
   *In tempo* qui vuol dire **entro un'ora per i messaggi**, e **mentre squilla** per il telefono. È una stima: chi scrive a cinque strutture la sera, entro un'ora ha già una risposta da qualcun altro.

**Una differenza a nostro favore rispetto all'e-commerce.** Una notte non venduta non si rivende domani. Il costo in più di un ospite (pulizie, biancheria, colazione) è piccolo rispetto al prezzo della notte. Per questo **quasi tutto quello che si perde con la prenotazione è guadagno perso, non solo incasso**. Nell'e-commerce, invece, dall'incasso va tolto il costo della merce.

**Una seconda unità, più piccola: la commissione del portale.** Chi non riesce a prenotare diretto spesso prenota la stessa struttura su Booking o Airbnb. La prenotazione non è persa, ma costa:
- **15-18%** su Booking.com, più se si aderisce ai programmi di visibilità;
- circa **15,5%** su Airbnb, con la tariffa a carico del solo host.

Entrambi i valori sono indicativi e dipendono dal contratto di ciascuno ([Dotthouse, 2026](https://www.dotthouse.ai/blog/commissioni-ota-affitti-brevi/); [Lodgify](https://www.lodgify.com/blog/it/commissioni-booking/)). Nelle strutture sotto le 20 camere i portali portano il **30-49% delle prenotazioni nel 27% dei casi**, e **più della metà in un altro 27%** ([dati Hotrec 2023, riportati da Hotel Cinque Stelle](https://www.hotelcinquestelle.cloud/blog/prenotazioni-dirette-vs-ota-una-fotografia-del-mercato/)).

### La formula che il titolare rifà con i suoi numeri

```
Soggiorni che escono dalla porta ogni mese =

    richieste di disponibilità rimaste senza risposta in tempo (al mese)
  × valore di un soggiorno  (prezzo medio a notte × notti medie)
  × quota di richieste che diventano prenotazione

Il secondo conto, da tenere separato:

    prenotazioni arrivate dal portale da ospiti che avevano cercato prima te
  × valore di un soggiorno
  × commissione del portale
```

**Il conto va fatto sull'anno, non sul mese di agosto.** Il canone si paga dodici mesi, mentre le richieste si concentrano in pochi mesi.

**Dove trova i suoi numeri:**

| Numero | Dove lo trova | Come |
|---|---|---|
| Richieste senza risposta in tempo | registro delle chiamate del telefono, WhatsApp, casella email | **Contarle per una settimana:** chiamate perse, messaggi a cui ha risposto dopo più di un'ora, email del giorno prima. Poi moltiplicare per 4. Va fatto una volta in alta stagione e una in bassa |
| Prezzo medio a notte | il suo gestionale o l'estratto del portale (incasso diviso notti vendute) | un numero |
| Notti medie | lo stesso estratto (notti vendute diviso prenotazioni) | se non lo sa, usa 3 |
| Quota che diventa prenotazione | le richieste dirette dell'anno scorso, confrontate con le prenotazioni dirette | se non lo sa, i valori prudenti qui sotto |
| Prenotazioni dal portale di chi aveva cercato prima lui | la sua memoria. Di solito non si sa | **Se non lo sa, questa riga non si calcola** |

### Le quote da usare quando il titolare non le sa (sono **stime**, con il ragionamento)

| Quota | Valore prudente | Ragionamento |
|---|---|---|
| Richiesta di disponibilità → prenotazione, se la risposta arriva in tempo | **10%** (forchetta 10-20%) | Un gestore di hotel italiani dichiara che "tra richieste e prenotazioni" il settore sta "all'8-12%" e i migliori "al 20-25%" ([AlbergatorePro](https://www.albergatorepro.com/blog/tempo-medio-risposta-richiesta-prenotazione): testimonianza, non studio). Nel listino Voice il ristorante usa il 50%: qui la quota è molto più bassa perché chi chiede un soggiorno confronta più strutture e spesso chiede solo il prezzo. Per chi **telefona** la quota è probabilmente più alta, ma non ho trovato un dato italiano: non la alzo |
| Commissione del portale | **15%** | il minimo della forchetta di Booking, vicino alla tariffa unica di Airbnb |

### Il valore di un soggiorno (prezzo misurato, calcolo nostro)

**Notti medie:** **3,34**, media di tutte le strutture italiane nel 2024 ([ISTAT](https://www.istat.it/storage/ASI/2025/capitoli/C19.pdf)). Nel quarto trimestre 2025 la media è scesa a 2,82 ([ISTAT, marzo 2026](https://www.istat.it/comunicato-stampa/flussi-turistici-iv-trimestre-2025/)): in bassa stagione i soggiorni sono più corti. **Il dato separato per il solo extra-alberghiero non l'ho trovato.**

| Tipo di struttura | Prezzo medio a notte (fonte) | Soggiorno (× 3,34 notti) | **Valore di una richiesta persa** (× 10%, stima) | Richieste perse all'anno che pagano il canone Pro (2.268 €) | Commissione su quel soggiorno (15-18%) |
|---|---|---|---|---|---|
| B&B a Bari, aprile 2025 | 81,90 € ([SumUp su dati dell'Osservatorio prezzi del Ministero](https://www.sumup.com/it-it/tap-to-pay/osservatorio-bnb-cashless-sumup/)) | 274 € | **27 €** | 83 | 41-49 € |
| B&B a Bari, secondo trimestre 2025 | 114,50 € ([SumUp, riportato da Sky TG24](https://tg24.sky.it/economia/2025/06/27/turismo-bed-and-breakfast-prezzi-citta)) | 382 € | **38 €** | 59 | 57-69 € |
| Casa vacanza, media italiana 2024 | 132 € (AirDNA, riportato da [Verto AI](https://vertoai.it/dati-affitti-brevi-italia): fonte di un fornitore) | 441 € | **44 €** | 51 | 66-79 € |
| Casa vacanza, estate 2025 | 167 € ([AIGAB e AirDNA, riportato da Sky TG24](https://tg24.sky.it/economia/2025/09/04/affitti-brevi-estate-2025-calo)) | 558 € | **56 €** | 41 | 84-100 € |
| Hotel, camera doppia con colazione, 2025 | 164 € ([AlbergatorePro su 1.500 hotel, riportato da Sky TG24](https://tg24.sky.it/economia/2025/12/16/prezzi-hotel-2025)) | 548 € | **55 €** | 41 | 82-99 € |

In tutti i tipi di struttura bastano **meno di due richieste perse a settimana, sull'anno**, per ripagare il canone Pro. Con la quota al 20% ne basta la metà.

**Perché il canone di riferimento è Pro e non Base.** Per dire se c'è posto e quanto costa, ARYA deve essere collegata al calendario della struttura, e **la fascia Base non include collegamenti** (glossario: 0 in Base, 2 in Pro, 5 in Scale). Con Base ARYA risponde alle domande e prende il messaggio, ma su quel lavoro, come dice la regola qui sotto, una persona compete con noi. È una deduzione dal glossario. `[DA CONFERMARE A IVAN: per una struttura ricettiva la fascia minima è Pro?]` All'anno va aggiunta l'attivazione una tantum, di cui qui non c'è l'importo. `[DA CHIEDERE A IVAN]`

### Un esempio fatto con la formula (esempio, non dato)

B&B con 5 camere in provincia di Bari: 100 € a notte, 3 notti di media, quindi **300 € a soggiorno**. In una settimana d'estate il titolare conta 4 richieste perse, cioè circa **15 al mese**: telefonate mentre accompagnava un ospite, WhatsApp arrivati di sera. In bassa stagione ne conta 1 a settimana, cioè **4 al mese**.

| Riga | Conto | Soggiorni persi |
|---|---|---|
| Sei mesi di stagione | 6 × 15 × 300 € × 10% | **2.700 €** |
| Sei mesi fuori stagione | 6 × 4 × 300 € × 10% | **720 €** |
| **Totale sull'anno** | | **3.420 €**, contro 2.268 € di canone Pro all'anno |
| Secondo conto, se sa che 10 ospiti del portale lo avevano cercato prima | 10 × 300 € × 15% | **450 €** di commissioni |

Con la quota al 20% il primo totale raddoppia. Dall'incasso vanno tolte pulizie e colazione, e il risultato resta sopra il canone. **Il conto va fatto con i numeri suoi, davanti a lui, prima di dire il prezzo**, come dice la pagina 11 del listino Voice.

### Quanto vale un ospite nel tempo

Nel B&B l'ospite che torna, o che ne manda un altro, vale più di un soggiorno. **Non ho trovato un dato italiano affidabile su quanti ospiti tornano: non lo stimo.** Si chiede al titolare nella call.

### Che cosa serve sapere per rispondere

| Tipo di richiesta | Per rispondere basta… | Chi altro può farlo, e a quanto |
|---|---|---|
| "a che ora è il check-in, c'è parcheggio, accettate cani, com'è la colazione" | **le regole della struttura**, scritte una volta | il titolare; la risposta automatica di WhatsApp (un messaggio fisso); i messaggi automatici dei gestionali per case vacanza, per esempio Smoobu da **26-50 € al mese** per struttura, che però raccoglie in un'unica casella solo i messaggi di Airbnb e Booking ([HostRadar, 2026](https://hostradar.eu/en/reviews/smoobu/)) |
| "**c'è posto dal 12 al 15** per due adulti e un bambino? quanto costa?" | **il calendario e le tariffe**, cioè il gestionale o il programma che sincronizza i portali | il titolare; il receptionist; gli assistenti in chat per hotel: Visito da **99 $ al mese**, HiJiffy da **200 $ al mese**, gli altri a preventivo, tutti collegati ai gestionali alberghieri e **nessuno al telefono** ([Visito, luglio 2026](https://www.visitoai.com/en/blog/best-hotel-chatbots-for-independent-hotels): fonte di un fornitore); il portale stesso, dove l'ospite prenota da solo pagando la commissione |
| "prenoto / cambio le date / disdico" | **scrivere nel calendario** | il receptionist; il titolare dal pannello del portale |
| "sono arrivato alle 23 e non trovo le chiavi" | la prenotazione e le istruzioni di arrivo | il titolare svegliato di notte; il portiere notturno |
| telefonata in inglese o in tedesco | tutto quanto sopra, in un'altra lingua | un receptionist che parla le lingue; call center esterni per hotel, con prezzi non pubblicati ([WuBook, 2026](https://wubook.net/blog/call-center-per-hotel)) |

**La regola, scritta come la vuole la skill:**

> Dove per rispondere basta prendere un messaggio, una persona vera costa quanto noi e ispira più fiducia. Dove per rispondere bisogna sapere qualcosa, non c'è confronto.

**Nel ricettivo la richiesta che vale soldi, "c'è posto?", sta nella seconda riga: bisogna sapere qualcosa.** La regola ci dà ragione solo a una condizione: **che il calendario della struttura sia collegabile.** Se il titolare tiene il calendario su carta, o solo dentro l'extranet del portale, ARYA può soltanto prendere il messaggio e passarlo a lui. In quel caso siamo nella prima riga, dove il titolare stesso e i messaggi automatici competono con noi a prezzo zero o quasi.

### Il confronto esplicito con l'e-commerce: contro chi si confronta il prezzo

| | **E-commerce** (`ecommerce.md`) | **Ricettivo** |
|---|---|---|
| **Contro chi si confronta il prezzo** | un **programma di chat economico** (30-100 € al mese) che legge già gli ordini | **piccolo B&B e casa vacanza:** **il titolare stesso**, che non costa niente in cassa, più i messaggi automatici del gestionale (26-50 €). **Piccolo hotel:** **una persona**, il receptionist o il portiere notturno, con un minimo contrattuale di **1.661 € lordi al mese** per un receptionist di 4° livello, circa 1.200 netti ([LavoroTurismo, CCNL Turismo giugno 2025](https://www.lavoroturismo.it/blog/guide/quanto-guadagna-un-receptionist)), a cui si aggiunge il costo per l'albergo. Solo in seconda battuta: gli assistenti in chat per hotel (99-200 $) |
| **L'alternativa che "sa qualcosa" esiste già ed è economica?** | **sì**, ed è ciò che ci penalizza | **solo per gli hotel con un gestionale compatibile**, e senza telefono. Per B&B e case vacanza, nei documenti trovati, no: i loro strumenti mandano messaggi fissi, non rispondono |
| **Il telefono conta?** | poco | **sì**: gli ospiti chiamano, soprattutto per l'ultimo minuto e per l'arrivo. Nessuno degli assistenti in chat per hotel elencati lo copre |
| **Quello che si perde è guadagno o incasso?** | incasso, da cui va tolta la merce | **quasi tutto guadagno**, perché la notte vuota non si rivende |
| **Valore di una richiesta persa** | 7-43 € (stima) | **27-56 €** (stima) |
| **Dove ci penalizza, invece** | — | **il calendario non collegabile** delle strutture più piccole, e **il titolare che risponde gratis**: con lui il confronto non si vince sul prezzo ma con la formula, cioè mostrando quanto costa rispondere tardi |

**In sintesi:** qui la penalità dell'e-commerce non c'è, o c'è molto meno. **"Costa meno di una persona" diventa un argomento vero nel piccolo hotel**, dove l'alternativa è coprire la notte e il fine settimana con del personale, e non una segreteria da 39 €. Nel B&B familiare l'argomento non regge, perché la persona è il titolare. Lì vale solo il conto delle richieste perse, insieme a quello che il titolare si riprende in tempo libero (product-marketing, "Tensione emotiva": la libertà).

### Il conto dall'altra parte: quanto possiamo pagare noi

Il tetto approvato il 15 settembre è di **500 € per call fissata**, e il passaggio da contatto valido a call è di **circa 1 su 10**. Quindi un contatto valido non può costarci più di **50 €**, come nell'e-commerce. Qui la formula ha un vantaggio in chat: il titolare conosce a memoria il prezzo a notte, e il conto si fa con due domande.

---

## 3. Cosa fa ARYA in questo settore (risposte di Ivan del 14 settembre 2026)

Roberto non segue questo progetto: le risposte tecniche su ARYA le dà Ivan. Valgono per tutti i settori finché non cambiano. Il 14 settembre Ivan ha anche detto che ARYA **arriva ai portali di prenotazione**.

| Promessa (nelle parole del cliente) | Si può fare oggi? | Con quale prova | Dove sta il limite |
|---|---|---|---|
| risponde anche di notte e quando sei fuori | **sì** | nessuna di questo settore; Mr. Toner in produzione (**altro settore**) | — |
| risponde al telefono, su WhatsApp, per email e sulla chat del sito | **sì** | — | la voce parte dalla fascia Pro (glossario) |
| risponde alle domande sulla struttura (orari, parcheggio, animali, colazione) | **sì** | — | le regole le scrive LML all'attivazione, con il titolare |
| ti dice se c'è posto e quanto costa | **dipende** | nessuna | solo se il calendario è su un programma collegabile. `[DA CHIEDERE A IVAN: con quali gestionali e programmi di sincronizzazione dei portali esiste già il collegamento?]` |
| prende la prenotazione e la scrive in calendario | **dipende** | nessuna | stesso limite. Il titolare decide se lasciarglielo fare o se ARYA deve solo preparare la richiesta |
| risponde ai messaggi che arrivano su Booking e Airbnb | **dipende** | — | Ivan: "arriva ai portali di prenotazione". Di solito quei messaggi passano da gestionali autorizzati dai portali. `[DA CHIEDERE A IVAN: con quali portali, e attraverso quale programma]` |
| risponde in inglese, tedesco o francese | `[DA CHIEDERE A IVAN]` | — | in Puglia le presenze straniere del 2024 superano del 57% quelle del 2019 ([ISTAT](https://www.istat.it/storage/ASI/2025/capitoli/C19.pdf)): non è un dettaglio |
| manda le istruzioni di arrivo | **sì** | — | il codice di accesso o delle chiavi è un'informazione di sicurezza: **decide il titolare** se ARYA può darlo, e a chi |
| riconosce l'ospite che è già stato da te | **sì, con il gestionale collegato** | — | — |
| passa la conversazione al titolare con tutto quello che è stato detto | **sì** | Mr. Toner (**altro settore**) | — |
| riscrive agli ospiti degli anni scorsi per la stagione nuova | **dipende** | — | ARYA ricontatta (Ivan), ma serve il consenso dell'ospite a ricevere promozioni. `[DA VERIFICARE con chi segue la privacy]` |
| manda il link per pagare la caparra | `[DA CHIEDERE A IVAN]` | — | dipende da cosa permette il gestionale collegato |
| "ti fa risparmiare le commissioni", "X prenotazioni in più" | **no** | nessun numero misurato | §23: non si promettono risultati economici senza un caso documentato |

**Collegamenti esistenti:** le piattaforme e-commerce (non servono qui) e "i portali di prenotazione" (Ivan), senza nomi. `[DA CHIEDERE A IVAN: l'elenco]`
**Collegamenti da costruire:** i gestionali e i programmi di sincronizzazione dei portali usati dalle piccole strutture. Richiedono "qualche ora" ciascuno.
**Quello che resta da verificare struttura per struttura:** dove tiene il calendario il titolare, se quel programma dà l'accesso, e se il titolare ha le credenziali. **Nel ricettivo è la domanda che decide il contratto.** Va fatta nella call, prima del prezzo.

---

## 4. Le prove

| Prova | Tipo | Stato del consenso | Numeri disponibili | Forma anonima |
|---|---|---|---|---|
| Mr. Toner | cliente in produzione, **altro settore**. Si cita come "abbiamo già fatto", mai come "per uno come te" | il nome non si usa mai (decisione del 14/09/2026) | nessuno dei cinque numeri della product-marketing risulta raccolto | "un rivenditore di consumabili in Puglia, una decina di persone" |
| Studio dentistico (implementazione chiusa, §10.1) | **altro settore**, gestione di appuntamenti | il nome non si usa mai | `[DA CHIEDERE A IVAN]` | "uno studio dentistico in provincia di Bari" `[DA CONFERMARE A IVAN]` |
| Registrazione della voce vera | demo | — | `[DA CHIEDERE A IVAN: esiste? in quali lingue?]` | — |

**Nessuna prova di questo settore. Le inserzioni possono solo mostrare il prodotto che funziona.**

**La prova più utile da costruire:** una struttura pugliese, anche di una persona conosciuta, dove contare per una settimana le richieste perse prima di attivare ARYA, e poi rifare la formula. `[DA CHIEDERE A IVAN: c'è una struttura disponibile?]`

---

## 5. Il partner

- **Esiste un partner che ha già dentro molte strutture di questo settore?** `[DA CHIEDERE A IVAN]` I candidati naturali:
  - **i gestionali e i programmi di sincronizzazione dei portali** usati dalle piccole strutture: hanno dentro l'elenco dei clienti e **anche il calendario che ci serve collegare**;
  - **le associazioni di categoria** (B&B, gestori di affitti brevi, albergatori);
  - **i gestori di case vacanza per conto terzi**, che sono insieme cliente e canale.
  
  Nella panoramica compare Hostley, "gestione online strutture ricettive", non profilata.
- **È stato chiesto ai partner dell'accordo quadro se servono il ricettivo?** `[DA CHIEDERE A IVAN: data e risposta]`
- **Decisione:** Meta come supporto oppure Meta a pieno regime. `[DA CHIEDERE A IVAN]`

Nel ricettivo il partner vale doppio: porta i clienti **e** risolve il problema del calendario non collegabile (passo 2bis).

---

## 6. Concorrenti e alternative

| Chi | Promessa più ripetuta | Cosa regala | Dove casca rispetto a noi |
|---|---|---|---|
| **Readygoone**: 4 inserzioni sopravvissute, **139 giorni**, solo hotel. Porta a un **modulo dentro Meta**, la stessa destinazione scelta da noi il 14/09 | "rispondi a tutti, in ogni lingua, 24 ore su 24, fino alla prenotazione", su sito, WhatsApp, Messenger, centralino, QR code e totem. Con il secondo prodotto (Hogen): "smetti di pagare commissioni ai portali" | nessun regalo visto nelle sopravvissute | parla solo agli hotel, non a B&B e case vacanza. **Promette le lingue: noi non sappiamo ancora se possiamo farlo** (passo 3). Cita fonti per i suoi numeri: è più attrezzato di noi sulle prove |
| **Assistenti in chat per hotel** (Visito, HiJiffy e altri). **Non trovati nella Libreria Inserzioni italiana** | rispondere in chat e portare alla prenotazione | — | collegati ai gestionali alberghieri, **nessuno al telefono**; prezzi a preventivo o in dollari |
| **DeepAgent**: il concorrente più attrezzato del radar, oggi senza un verticale ricettivo | "lo configuriamo noi", "agisce dentro il gestionale" | configurazione gratuita dichiarata da 2.000 € | se apre il ricettivo dice le nostre stesse cose con un regalo in più. **Da sorvegliare** |

| Alternativa che sembra ragionevole | La frase che la smonta |
|---|---|
| il titolare che risponde dal cellulare | *da raccogliere nella voce.* L'argomento nostro è il tempo che si riprende (product-marketing, "Tensione emotiva") |
| receptionist o portiere notturno | costa più di 1.661 € lordi al mese per ogni turno da coprire; di notte e nel fine settimana servono più persone |
| call center esterno per hotel | prezzi non pubblicati; **non verificato** |
| messaggi automatici del gestionale | mandano un testo fisso a date fisse, non rispondono alla domanda |
| risposta automatica di WhatsApp | un messaggio fisso, poi niente |
| "tanto prenotano su Booking" | vero, e ogni prenotazione paga il 15-18% (passo 2bis) |

---

## 7. Le obiezioni di questo settore

**Non compilabile: manca la voce del settore.**

Tre obiezioni che il passo 2bis fa prevedere. Vanno **verificate nella voce** e oggi **non hanno una risposta nei materiali LML**:
- *"Il mio calendario è solo su Booking."* Oggi la risposta onesta è "allora ARYA prende la richiesta e la passa a te".
- *"I miei ospiti vogliono parlare con me."* Nel B&B familiare è probabilmente vera, e potrebbe finire fra i momenti tolti per credibilità.
- *"D'inverno non ricevo niente, perché pagare dodici mesi?"*

---

## 8. Il formato

- **Inserzioni sopravvissute rivolte agli hotel (panoramica):** 4, tutte di Readygoone. La prima letta è un **video con una faccia**, una persona su un palco; le altre tre sono "dello stesso stampo", con formato non misurato una per una. **Per B&B e case vacanza: 0.**
- **Risorse nostre già pronte:**
  - registrazione della voce di ARYA `[DA CHIEDERE A IVAN]`;
  - video di Ivan `[DA CHIEDERE A IVAN]`;
  - nessuna struttura dimostrativa: nel ricettivo **non esiste l'equivalente di MineDocs**.
- **Scelta di partenza e motivo:** un video verticale con la faccia di Ivan (§18, §2bis, "segni distintivi"). L'unico concorrente che dura usa il video con una faccia, e noi non abbiamo prove da raccontare. Nel ricettivo il prodotto si mostra bene **al telefono**, con una chiamata che chiede disponibilità: coincide con la demo telefonica approvata il 15/09. *Il formato lo decide la spesa, non questa scheda.*

---

## 9. Prezzo e qualificazione

- **Fascia di prezzo da dire in inserzione:** `[DA CHIEDERE A IVAN]`. Se Pro è la fascia minima (passo 2bis), il prezzo da dire è 189 € al mese, cioè 2.268 € all'anno. Nel ricettivo conviene ragionare sull'anno.
- **La domanda che qualifica** (nel modulo, dal 15/09): "Quante chiamate o messaggi ricevi in un giorno?". **Attenzione:** nel ricettivo la risposta cambia moltissimo fra agosto e febbraio. Soglia proposta: **3 al giorno in alta stagione** `[DA CONFERMARE A IVAN]`.
- **Le tre domande della chat** (§3.1), adattate al settore. Servono a rifare la formula e a capire se il calendario si può collegare:
  1. Quante richieste ricevi in un giorno d'estate, e da dove arrivano (telefono, WhatsApp, email)?
  2. Dove tieni il calendario delle prenotazioni?
  3. Quanto costa più o meno una notte da te?

---

## 10. I cancelli

| Condizione | Stato | Note |
|---|---|---|
| Radar da meno di 30 giorni | **in parte** | la panoramica del 14/09 c'è; un radar dedicato al ricettivo no |
| Voce fatta | **no** | `voce/ricettivo/` non esiste |
| Cosa fa ARYA: confermato | **in parte** | confermato da Ivan il 14/09 (Roberto non segue il progetto). Restano aperti le lingue, i portali e l'elenco dei gestionali collegati |
| Almeno una prova del settore, o decisione di partire senza | **no** | `[DA CHIEDERE A IVAN: si parte mostrando solo il prodotto? sì / no / dopo una struttura di prova]` |
| Partner verificato (§22.1) | **no** | `[DA CHIEDERE A IVAN]` |
| Settore riconosciuto nella §10.1 | **sì** | è il settore n. 4, senza referenza. Resta da decidere se valgono le strutture sotto i 5 addetti |
| Chi risponde ai contatti e in quanto tempo (§11) | **no** | il primo contatto lo fa ARYA su WhatsApp, ma il flusso non è ancora provato con 20 contatti finti (§3.1, §26). Dopo ARYA chiama Brian Razzi (§11); l'archivio contatti oggi lo vede solo Ivan |
| Massimo due campagne attive (§0.1) | **sì** | su lml-adv non c'è nessuna campagna (report del 15/09) |

**Esito: BOZZA.** Delle otto caselle, due sono "sì", due "in parte" e quattro "no".

---

## 11. Da segnalare a Ivan

1. **Nel ricettivo la penalità dell'e-commerce non c'è.** Il prezzo non si confronta con un programma di chat economico. Si confronta **con una persona** nel piccolo hotel, dove "costa meno di una persona" è un argomento vero, e **con il titolare stesso** nel B&B familiare, dove l'argomento non regge e vale solo la formula.
2. **Il limite vero è il calendario.** "C'è posto?" vale soldi solo se ARYA può leggere il calendario, e le strutture più piccole spesso non ne hanno uno collegabile. **È la prima domanda da fare nella call, e il motivo per cui un gestionale del settore come partner vale doppio.**
3. **Una richiesta persa vale 27-56 € (stima)**, più di quanto valga nell'e-commerce, e quasi tutto è guadagno perché la notte vuota non si rivende. Sull'anno bastano **meno di due richieste perse a settimana** per ripagare il canone Pro.
4. **Il cliente giusto dentro il settore è probabilmente il piccolo hotel o chi gestisce molte case vacanza**, non il B&B familiare: sono quelli dentro i 5-50 addetti, con più richieste e più lingue.
5. **Readygoone presidia gli hotel da 139 giorni** con un modulo dentro Meta, cioè la nostra stessa destinazione, e **promette le lingue**. Prima di entrare negli hotel va chiarito se ARYA risponde in inglese e in tedesco. **B&B e case vacanza invece risultano liberi** nel radar.
6. **La finestra per partire sembra ottobre-marzo, non settembre.** In Puglia a settembre la stagione è ancora in corso. È una decisione da prendere in deroga alla §15.
7. **Il canone di dodici mesi contro una stagione di quattro** è un'obiezione prevedibile che non ha risposta nei nostri materiali.

---

## 12. Storico

| Data | Cosa è cambiato | Chi |
|---|---|---|
| 15/09/2026 | Prima stesura, in BOZZA. Compilato per primo il passo 2bis (la prenotazione persa), con il confronto esplicito con la scheda e-commerce, su richiesta di Ivan. Passi 2 e 7 vuoti perché manca la voce del settore | Claude, su richiesta di Ivan |
