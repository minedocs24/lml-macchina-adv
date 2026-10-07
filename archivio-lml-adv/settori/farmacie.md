# Scheda settore — Farmacie

**Stato:** BOZZA
**Ultimo aggiornamento:** 15 settembre 2026 · **Skill:** `lml-scheda-settore` v2.0 del 14 settembre 2026
**Radar usato:** `radar/panoramica/2026-09-14.md` (panoramica di tutto il mercato). **Un radar dedicato alle farmacie non esiste.**
**Voce usata:** **nessuna: `voce/farmacie/` non esiste.**

> ⚠️ **Le farmacie non sono fra gli otto settori presidiati della §10.1 di `regole-adv.md`.** Oggi un contatto di una farmacia non è un contatto valido. Per aprire il settore serve una modifica della §10.1 approvata da Ivan. Questa scheda serve a decidere se vale la pena chiederla.

**Fonti lette:**
- `regole-adv.md` **versione 2.3 del 14 settembre 2026**: §0.1, §2bis, §3.1, §4.2, §5.1, §10.1, §11, §15, §21, §22.1, §23, §26, §27
- `.agents/product-marketing.md` **v1.3, aggiornato il 14 settembre 2026** (il registro delle modifiche in fondo si ferma alla v1.2). Sulle farmacie non dice niente; ci sono i riferimenti di mercato sulle richieste risolte senza una persona
- `.agents/glossario.md` **versione 1.1 del 14 settembre 2026**: connettori, fasce, WhatsApp
- `radar/panoramica/2026-09-14.md` e `radar/panoramica/pagine.md` del 14 settembre 2026, per leia.pharma
- `settori/ecommerce.md` e `settori/ricettivo.md`, BOZZE del 15 settembre 2026, per il confronto
- Listino ARYA Voice, pagina 11: il modello del conto della chiamata persa e del costo di una chiamata gestita da una persona

**Aggiornamenti del 15 settembre 2026, approvati da Ivan e non ancora scritti in `regole-adv.md`.** In questa scheda li uso così come sono stati dati:
- offerta: "lascia il numero, ti risponde lei adesso", con la demo telefonica solo per chi risponde su WhatsApp;
- modulo "maggiore intenzione", con una sola domanda più il campo "come ci hai conosciuto?";
- tetto: **1.000 € per cliente, 500 € per call**;
- passaggio da contatto valido a call: **circa 1 su 10**.

### Cosa manca per confermare

| Cosa manca | Chi risponde |
|---|---|
| **Decidere se le farmacie entrano nella §10.1** | Ivan |
| **Una verifica legale** su dati sanitari, WhatsApp e assistente automatico con i pazienti (passo 2ter) | un legale che conosca la sanità e la privacy |
| La voce del settore (`voce/farmacie/`). Senza di essa i passi 2 e 7 restano vuoti | skill `lml-voce-del-settore` |
| Un radar dedicato alle farmacie | skill `lml-radar-inserzioni` |
| Le caselle `[DA CHIEDERE A IVAN]` dei passi 1, 3, 4, 5 e 9 | Ivan |
| Il flusso di ricontatto di ARYA provato con 20 contatti finti (§3.1) | Ivan |

---

## 0. In tre righe

**Sulla vendita persa il conto non regge.** Lo scontrino medio è di circa 30 €. Chi non trova risposta al telefono spesso passa comunque in farmacia, perché è sotto casa. I servizi prenotabili sono pochi: in media circa 7 prestazioni di telemedicina al mese per farmacia.

Il conto regge solo su altre due unità:
- **il tempo del personale al banco**, interrotto dal telefono;
- **il cliente abituale che cambia farmacia**. Questa però è invisibile e non si può misurare.

**Il confronto di prezzo è in salita, peggio che nell'e-commerce.** Esistono già assistenti WhatsApp fatti apposta per le farmacie, italiani, da 99 € al mese e con prova gratuita.

**In più il settore ha vincoli di legge che negli altri due non ci sono:**
- i dati sulla salute;
- il divieto di promozioni sui servizi sanitari;
- il consiglio sul farmaco, che spetta solo al farmacista.

Non ci sono prove di questo settore e il settore non è nella §10.1.

---

## 1. Il cliente giusto

- **Dimensione.** In Italia ci sono **20.295 farmacie** convenzionate con il servizio sanitario e circa **101.000 addetti**, cioè **5 addetti per farmacia in media**. Il fatturato del 2025 è di 27,9 miliardi ([Federfarma, "La farmacia italiana", riportato da Farmacista33, luglio 2026](https://www.farmacista33.it/industria-e-mercati/33480/rapporto-confcommercio-federfarma-i-dati-su-numero-e-fatturati-delle-farmacie-convenzionate.html)). Una farmacia fattura in media **1,4 milioni** e batte **198 scontrini al giorno** ([IQVIA a Cosmofarma, riportato da Pharmacy Scanner, aprile 2025](https://pharmacyscanner.it/scontrino-medio-produttivita-fatturato-nelle-organizzate-performance-spesso-migliori/)). In **Puglia** le farmacie sono **1.280** ([Farmacia News, giugno 2025](https://www.farmacianews.it/telemedicina-in-puglia-oltre-4-500-prestazioni-effettuate-nel-primo-mese/)).
  **Il settore sta proprio sulla soglia dei 5 addetti:** circa la metà delle farmacie è dentro il target 5-50 della §4.2. È una stima dalla media, non un dato sulla distribuzione.
- **Chi decide:** il titolare, farmacista, da solo. Nelle catene e nelle reti decide la sede centrale.
- **Chi risponde oggi:** il farmacista o il commesso al banco, **mentre serve un cliente**.
- **Chi subisce e cosa teme:** il collaboratore al banco. È un ragionamento, da verificare con la voce: più che "mi sostituisce", può temere che l'assistente dia una risposta sbagliata su un farmaco, che poi ricade su di lui.
- **Segnale d'acquisto:** il telefono che interrompe il banco. È la stessa promessa di leia.pharma: "le chiamate non devono interrompere il lavoro al banco" (radar).
- **Soglia proposta:** **20 chiamate o messaggi al giorno** `[DA CONFERMARE A IVAN]`. È una stima dal conto del tempo del passo 2bis: sotto questa soglia il tempo recuperato non paga il canone.
- **Stagionalità:** è un ragionamento, non un dato. Il picco è d'inverno, con le sindromi influenzali e le campagne di vaccinazione di ottobre e novembre. D'estate ci sono i turni e le ferie. Il momento per vendere sarebbe **settembre-ottobre**, prima del picco, in linea con la §15.
- **A chi non vendere:**
  - farmacie rurali con poche chiamate;
  - chi vuole che l'assistente dia consigli sui farmaci (passo 2ter);
  - chi vuole mandare promozioni sui servizi o sui farmaci (passo 2ter);
  - chi vuole provare gratis: qui i concorrenti la prova la regalano.

---

## 2. I momenti d'ingresso

**Non si può compilare: manca la voce del settore** (regola 8).

Quello che si può già dire:
- l'unico concorrente visto nel radar, **leia.pharma**, usa il momento "le chiamate non devono interrompere il lavoro al banco". Ha 3 inserzioni con **7 giorni** di vita: è **rumore**, non una sopravvissuta;
- **nessuna inserzione sopravvissuta** si rivolge alle farmacie.

**Momenti da togliere per credibilità, già adesso:**
- **"il cliente chiede un consiglio su un farmaco o su un sintomo".** Non è un momento nostro, per legge e per deontologia (passo 2ter);
- **"il cliente ha un'urgenza".** Non è un momento nostro, per l'AI Act.

---

## 2bis. Quanto vale un contatto perso, e contro chi ci confrontiamo

### Le unità possibili, una per una

In farmacia una chiamata può essere quattro cose diverse. Le ho contate tutte, perché **la vendita singola, da sola, non basta**.

| Unità | Cosa succede se nessuno risponde | Valore per la farmacia |
|---|---|---|
| **1. "Ce l'avete X?"** (disponibilità di un prodotto) | una parte dei clienti va in un'altra farmacia; **molti passano comunque**, perché la farmacia è vicina e abituale | basso: scontrino di circa 30 €, con margine piccolo |
| **2. "Posso prenotare l'holter / l'ECG?"** (servizio) | il cliente prenota altrove | medio, ma **i servizi sono pochi** |
| **3. "Mi prenotate la visita al CUP?"** | il cliente va di persona o chiama il CUP | quasi zero: in Puglia il cittadino paga **2 €** a prenotazione ([Leccenews24, 2017](https://www.leccenews24.it/politica/prenotare-una-visita-al-cup-se-vai-in-farmacia-devi-pagare-2-euro.htm)). **Quanto di quei 2 € resti alla farmacia non l'ho trovato.** Inoltre ARYA non può entrare nel sistema della Regione al posto del farmacista (passo 3) |
| **4. Il telefono che squilla mentre si serve al banco** | il farmacista lascia il cliente davanti a sé, oppure lascia squillare | **è il tempo del personale**: il primo conto della pagina 11 del listino Voice |

### Unità 1 — la vendita persa: **il conto non regge**

```
richieste di disponibilità senza risposta (al mese)
× scontrino medio
× quota di clienti che sarebbe andata altrove
× margine
```

- **Scontrino medio:** "poco meno di 30 €" (IQVIA, aprile 2025). Nel 2024 il rapporto fra fatturato e 736 milioni di ingressi dà circa 35 €, ma comprende i farmaci pagati dal servizio sanitario.
- **Quota che sarebbe andata altrove:** **50%**. È una **stima generosa**: nel listino Voice si usa lo stesso valore per la telefonata al ristorante, ma in farmacia il cliente abituale spesso passa lo stesso.
- **Margine:** **30%**. È una **stima**, da una fonte che non cita i dati ([BusinessOnline, 2025](https://www.businessonline.it/articoli/quanto-guadagna-una-farmacia-mediamente-ricavi-lordi-e-utili-netti-medi.html)). Sui farmaci pagati dal servizio sanitario la remunerazione è fissata per legge. **Non ho letto la tabella** (il sito Federfarma non si è aperto).

**Una richiesta persa vale circa 15 € di incasso e 4,50 € di guadagno** (stima).
Per ripagare il canone Pro (189 € al mese) servono **42 vendite perse al mese**, quasi **2 al giorno**, *che sarebbero davvero andate a un'altra farmacia*. Su 198 clienti al giorno è meno dell'1%. Sulla carta sembra poco, ma **nessun titolare può verificarlo**: non sa chi ha chiamato, non l'ha trovato e non è venuto. Con la quota più realistica, sotto il 50%, servono molte più vendite. **Detto chiaramente: su questa unità il conto non regge in modo che un titolare ci creda.**

### Unità 2 — il servizio perso: **non regge da solo**

- **Prezzo:** un holter cardiaco privato costa **74 €** in una farmacia che pubblica il listino ([Farmacia Carli](https://www.farmaciacarli.it/products/holter-cardiaco): un solo esempio, non una media). **Una media nazionale dei prezzi di ECG e holter in farmacia non l'ho trovata.**
- **Volume:** i due principali fornitori di telemedicina per farmacie hanno fatto nel 2024 circa **80 prestazioni all'anno per farmacia**, cioè **meno di 7 al mese** (MedEA: 245.845 prestazioni su 3.000 farmacie; HTN: 658.756 su 8.312). In Italia sono oltre 900.000 prestazioni ([Farmacia News](https://www.farmacianews.it/farmacia-dei-servizi-telemedicina-e-monitoraggio-cardiovascolare/)).
- **In Puglia** 850 farmacie su 1.280 fanno telemedicina **per i cittadini con la prescrizione del medico**. Nel primo mese hanno fatto 4.500 prestazioni. **Quanto riceve la farmacia per ogni prestazione non l'ho trovato** (Farmacia News, giugno 2025).

Una prenotazione persa vale **37 € di incasso** (74 € × 50%, stima). Per pagare il canone ne servono **5 al mese sull'incasso**, e **circa 10 se il guadagno è la metà** (stima). **Una farmacia media ne fa meno di 7 in tutto. Non regge da sola.** Può reggere solo in una farmacia che vive di servizi, e questa è una nicchia.

### Unità 3 — il CUP: **non regge**

Anche se la farmacia incassasse tutti i 2 €, servirebbero **95 prenotazioni perse al mese**. Inoltre il lavoro sul sistema della Regione lo fa il farmacista con le sue credenziali. **Non è un argomento di vendita per noi.**

### Unità 4 — il tempo del personale: **l'unico conto che regge ed è misurabile**

È il primo conto della pagina 11 del listino Voice: **una chiamata gestita da una persona costa 1,35 €**, con un costo orario pieno di 25-28 € e tre minuti a telefonata.

```
chiamate e messaggi al giorno × giorni di apertura × 1,35 €
× quota che l'assistente chiude da solo
```

- **Quota chiusa da solo: 70%.** È il riferimento di mercato della product-marketing per le richieste di routine, come orari e stato dell'ordine. Viene dai fornitori, quindi va letto al ribasso.
- **Giorni di apertura:** 26 al mese.

| Chiamate e messaggi al giorno | Tempo del personale al mese | Tempo recuperato (70%) | Rispetto al canone Pro (189 €) |
|---|---|---|---|
| 10 | 351 € | **246 €** | pari, se si aggiunge la quota a risultato |
| 20 | 702 € | **491 €** | regge |
| 40 | 1.404 € | **983 €** | regge bene |

**Quante chiamate riceve una farmacia al giorno non l'ho trovato.** Il titolare lo legge nel registro del telefono. Il costo orario di 25-28 € è quello del listino. Un farmacista collaboratore può costare di più: **non l'ho verificato sul contratto di lavoro delle farmacie.**

**Il limite di questo conto:** il tempo recuperato diventa denaro solo se il personale lo usa per vendere al banco o per erogare servizi. Oppure se si evita di prendere una persona in più. **È un conto sul tempo, non sulla cassa.**

### Unità 5 — il cliente abituale che cambia farmacia: regge sulla carta, ma non si vede

- In Italia ci sono circa **12 ingressi in farmacia all'anno per abitante** (736 milioni di ingressi nel 2024 su 59 milioni di abitanti; fonte Federfarma via Farmacista33).
- Un cliente abituale vale circa **360 € all'anno di incasso e 108 € di guadagno** (stima: 12 × 30 € × 30%).
- **Bastano 21 clienti abituali persi all'anno** per pagare il canone Pro.

È l'argomento più forte sulla carta ed è esattamente il "costo invisibile" della product-marketing: **nessuna farmacia sa quanti clienti ha perso per una telefonata**. Non si può mettere in un'inserzione come numero (§23). Si può usare solo in chiamata, come domanda.

### Che cosa serve sapere per rispondere

| Tipo di richiesta | Per rispondere basta… | Chi altro può farlo, e a quanto |
|---|---|---|
| "siete aperti? siete di turno?" | gli orari e i turni | la scheda Google, i siti dei turni, la risposta automatica di WhatsApp: **gratis** |
| "ce l'avete X? me lo mettete da parte?" | **il gestionale di farmacia** (per esempio CGM Wingesfar, fra i più diffusi) | **assistenti WhatsApp fatti per le farmacie, italiani:** Farmakom da **99 a 199 € al mese** più **500 € di attivazione**, "integrato con il tuo gestionale", **14 giorni gratis** ([Farmakom](https://www.farmakom.it/whatsapp-ai/)); leia.pharma, con prova gratuita (radar); AssistenteFarmacia e Neurapharm, prezzo non pubblicato |
| "prenoto l'holter / la misurazione" | l'agenda dei servizi | gli stessi assistenti; i sistemi di prenotazione dei fornitori di telemedicina (non verificato); il personale al banco |
| "mi prenotate il CUP?" | il sistema della Regione, con le credenziali del farmacista | **solo il farmacista** |
| "posso prendere X con Y? ho questo sintomo" | **il farmacista** | **nessun assistente automatico deve farlo** (passo 2ter) |

**La regola, scritta come la vuole la skill:**

> Dove per rispondere basta prendere un messaggio, una persona vera costa quanto noi e ispira più fiducia. Dove per rispondere bisogna sapere qualcosa, non c'è confronto.

**In farmacia la regola va corretta due volte.**
- **Sulla riga "bisogna sapere qualcosa"** (disponibilità, prenotazioni) il confronto c'è, ed è peggiore che nell'e-commerce: l'alternativa è **un prodotto verticale per farmacie, italiano, collegato al gestionale, allo stesso prezzo di ARYA o meno, con la prova gratuita**.
- **Sulla riga "bisogna sapere di più"** (consiglio sul farmaco) non c'è nessun confronto, perché **non lo può fare nessun assistente automatico, noi compresi**.

### Il confronto con le altre due schede: contro chi si confronta il prezzo

| | **E-commerce** | **Ricettivo** | **Farmacie** |
|---|---|---|---|
| **Contro chi si confronta il prezzo** | un programma di chat generico da 30-100 € al mese che legge gli ordini | piccolo hotel: **una persona** (minimo 1.661 € lordi al mese per turno); B&B: **il titolare stesso**, gratis | **assistenti WhatsApp fatti per le farmacie**, 99-199 € al mese + 500 € di attivazione, **con prova gratuita**; e il personale al banco, che risponde comunque durante l'orario |
| **L'alternativa è fatta per quel settore?** | no, è generica | per gli hotel sì (chat da 99-200 $), per B&B e case vacanza no | **sì, ed è italiana** |
| **Il telefono conta?** | poco | molto | **molto**. Per i concorrenti visti non è chiaro se coprano la voce: Farmakom e AssistenteFarmacia parlano di WhatsApp. È un possibile spazio per noi, **da verificare nel radar** |
| **Valore di una richiesta persa** | 7-43 € (stima) | 27-56 € (stima) | **circa 4,50 € di guadagno** sulla vendita (stima); **il conto regge solo sul tempo del personale** |
| **Vincoli di legge in più** | privacy del carrello | privacy dei ricontatti | **dati sanitari, divieto di promozioni, consiglio riservato al farmacista, AI Act sul triage** |
| **Per noi** | in salita | in piano negli hotel, in salita nei B&B | **in salita ripida**, e con un freno legale |

### Il conto dall'altra parte: quanto possiamo pagare noi

Con **500 € per call** e un passaggio da contatto valido a call di **circa 1 su 10**, un contatto valido non può costare più di **50 €**, come negli altri settori. In più qui c'è un fatto: **i concorrenti verticali regalano 14 giorni**, mentre noi non abbiamo prova gratuita e chiediamo un contratto di 24 mesi. È prevedibile che il passaggio a call sia **peggiore** di 1 su 10. È una stima, non un dato.

---

## 2ter. Vincoli di legge e di deontologia

> **Questa sezione non è un parere legale.** È il riassunto di fonti pubbliche lette oggi. Prima di aprire il settore va fatta verificare da un legale.

### La nostra pubblicità alle farmacie

**Le inserzioni di LML si rivolgono ai titolari, non ai pazienti, e non parlano di farmaci:** in sé non sono pubblicità sanitaria. **Da verificare:** se Meta tratta come "salute" le campagne che nominano le farmacie. Esistono regole di Meta sulla pubblicità legata alla salute; **non le ho lette** e non so se si applicano a chi vende software alle farmacie.

### Quello che ARYA non può fare per conto della farmacia

| Vincolo | Fonte | Cosa vuol dire per ARYA |
|---|---|---|
| **Niente offerte, sconti o promozioni sui servizi sanitari.** Le comunicazioni devono essere solo informative. Il divieto vale anche per le farmacie e vigilano gli Ordini | Legge 145/2018, comma 525, modificato dal "decreto salva infrazioni" (DL 69/2023, legge 103/2023) ([Farmacista33, agosto 2023](https://www.farmacista33.it/politica-sanitaria/27467/promuovere-servizi-sanitari-nuove-regole-sulla-pubblicita-il-decreto-salva-infrazioni-e-legge.html)) | **Il "ricontatta e manda le promozioni" del caso rivenditore non si trasferisce.** ARYA può ricordare un appuntamento, non promuovere un servizio sanitario. Federfarma ha indicato come probabilmente vietati perfino i punti della carta fedeltà sui servizi |
| **La pubblicità dei medicinali al pubblico** è ammessa solo per quelli senza ricetta, con dei limiti e con un'autorizzazione del Ministero | D.Lgs. 219/2006, articoli 115 e 118 ([testo AIFA](https://www.aifa.gov.it/sites/default/files/d.lgs_.n._219_2006_e_s.m.i..pdf), non letto per intero) | Nessun messaggio promozionale su farmaci mandato da ARYA senza una verifica caso per caso |
| **Il consiglio sul farmaco e la dispensazione spettano al farmacista.** Obbligo di segreto professionale e di riservatezza; divieto di iniziative che limitino la libera scelta della farmacia | Codice deontologico dei farmacisti (FOFI). **Il testo vigente non si è aperto: ho letto una versione del 2000** ([fog.it](https://www.fog.it/fogliani/giancarlo/deontologia.htm)), quindi non cito i numeri degli articoli | ARYA **non dà consigli** su farmaci, dosi, interazioni o sintomi: passa sempre al farmacista |
| **I dati sulla salute sono una categoria particolare.** Anche "avete l'insulina X?" o "prenoto un holter" rivela qualcosa sulla salute di chi scrive | GDPR, articolo 9 | Serve una base giuridica, LML nominata **responsabile del trattamento** (art. 28) e probabilmente una **valutazione d'impatto** (art. 35). **Da verificare con un legale** |
| **WhatsApp e le ricette:** il Garante non ha inserito WhatsApp fra gli strumenti adatti per inviare le ricette, per le "notevoli problematicità" delle app di messaggistica | Garante privacy, riportato da [Accademia Italiana Privacy, marzo 2023](https://www.accademiaitalianaprivacy.it/dettaglioNews.asp?id=767) | **ARYA non riceve e non manda ricette né codici di ricetta su WhatsApp** |
| **Il caso già scritto nelle nostre regole:** due farmacie online svedesi sanzionate per circa 4,4 milioni per dati inviati a Meta senza consenso | `regole-adv.md` §23 | Vale doppio qui: niente tracciamento Meta sui dati della farmacia |
| **Il triage dei pazienti in emergenza è un uso "ad alto rischio"** | AI Act, Allegato III, punto 5, lettera d ([testo ufficiale](https://ai-act-service-desk.ec.europa.eu/en/ai-act/annex-3)) | ARYA **non valuta urgenze**: a chi descrive un malore risponde di chiamare il 118 e passa la conversazione |
| **Dire che risponde un assistente automatico** | AI Act, articolo 50, già in `regole-adv.md` §3.1 | Vale anche verso i pazienti della farmacia |
| **In sanità l'intelligenza artificiale è un supporto: la decisione resta al professionista, e il paziente va informato dell'uso** | Legge 23 settembre 2025, n. 132, in vigore dal 10 ottobre 2025 ([sintesi dello Studio Legale Testa](https://studiolegalegiacomotesta.it/2025/10/30/la-legge-23-settembre-2025-n-132-sullintelligenza-artificiale-le-disposizioni-relative-alla-sanita/)). **Il testo di legge non l'ho letto: i numeri degli articoli nelle sintesi non sono verificati** | Rafforza le due righe sopra. **Da verificare con un legale** se una farmacia che usa ARYA per le prenotazioni dei servizi ricade in questi obblighi |
| **Un software che dà indicazioni su diagnosi o terapia può essere un dispositivo medico** | Regolamento UE 2017/745. **Non verificato su ARYA** | Un motivo in più per non dare consigli |

**La conseguenza pratica:** in farmacia ARYA può fare **meno cose** che negli altri settori, e **proprio le cose che valgono di più per il titolare** (consiglio e promozioni) sono vietate o rischiose.

---

## 3. Cosa fa ARYA in questo settore (risposte di Ivan del 14 settembre 2026, filtrate dal passo 2ter)

| Promessa (nelle parole del cliente) | Si può fare oggi? | Con quale prova | Dove sta il limite |
|---|---|---|---|
| risponde al telefono e su WhatsApp mentre sei al banco | **sì** | nessuna di questo settore; Mr. Toner (**altro settore**) | la voce parte dalla fascia Pro |
| dice gli orari e i turni | **sì** | — | — |
| dice se un prodotto c'è | **dipende** | nessuna | serve il collegamento al gestionale di farmacia. `[DA CHIEDERE A IVAN: con quali gestionali di farmacia esiste o si può costruire un collegamento? CGM Wingesfar e gli altri danno l'accesso?]` |
| mette da parte il prodotto e avvisa quando è pronto | **dipende** | nessuna | stesso limite; è un dato sanitario (passo 2ter) |
| prenota un servizio in agenda (holter, misurazioni) | **dipende** | nessuna | serve un'agenda collegabile. `[DA CHIEDERE A IVAN]` |
| ricorda l'appuntamento | **sì**, con il consenso | — | è un dato sanitario: da verificare con il legale |
| passa la conversazione al farmacista | **sì** | Mr. Toner (**altro settore**) | — |
| prenota al CUP | **no** | — | è il sistema della Regione, con le credenziali del farmacista |
| riceve o manda ricette | **no** | — | Garante (passo 2ter) |
| consiglia un farmaco o valuta un sintomo | **no** | — | deontologia, AI Act, dispositivi medici |
| manda promozioni su servizi sanitari o farmaci | **no** | — | L. 145/2018 c. 525 e D.Lgs. 219/2006 |
| "ti fa vendere di più" | **no** | nessun numero misurato | §23 |

**Quello che resta da verificare farmacia per farmacia:** se il gestionale dà l'accesso, se il fornitore del gestionale lo fa pagare, e se la farmacia ha già un fornitore di telemedicina con la sua agenda.

---

## 4. Le prove

| Prova | Tipo | Stato del consenso | Numeri disponibili | Forma anonima |
|---|---|---|---|---|
| Mr. Toner | cliente in produzione, **altro settore**: si cita come "abbiamo già fatto" | il nome non si usa mai | nessuno dei cinque numeri raccolto | "un rivenditore di consumabili in Puglia, una decina di persone" |
| Studio dentistico (implementazione chiusa, §10.1) | **altro settore**, ma **sanitario**: il caso più vicino per dati sanitari e prenotazioni | il nome non si usa mai | `[DA CHIEDERE A IVAN]` | `[DA CHIEDERE A IVAN]` |

**Nessuna prova di questo settore. Le inserzioni potrebbero solo mostrare il prodotto che funziona.**

---

## 5. Il partner

- **Esiste un partner con molte farmacie dentro?** `[DA CHIEDERE A IVAN]` Qui i candidati sono **forti e concentrati:**
  - i fornitori di gestionali per farmacia, che hanno anche il dato della disponibilità;
  - i fornitori di telemedicina, che hanno l'agenda dei servizi e migliaia di farmacie (MedEA 3.000, HTN oltre 8.000);
  - le reti e le catene di farmacie;
  - Federfarma provinciale.
- **È stato chiesto ai partner dell'accordo quadro?** `[DA CHIEDERE A IVAN]`
- **Decisione:** Meta come supporto oppure a pieno regime. `[DA CHIEDERE A IVAN]`

**Qui la §22.1 pesa più che altrove.** Un settore con pochi grandi fornitori che hanno già dentro migliaia di clienti si apre da un partner, non da un'inserzione. La pubblicità diretta a 20.000 farmacie, con un conto che non regge sulla vendita, è la strada più cara.

---

## 6. Concorrenti e alternative

| Chi | Promessa più ripetuta | Cosa regala | Dove casca rispetto a noi |
|---|---|---|---|
| **leia.pharma** — 3 inserzioni, 7 giorni, **rumore** (radar) | "le chiamate non devono interrompere il lavoro al banco"; "risponde anche su WhatsApp" | prova gratuita | non profilato a fondo; da riguardare al prossimo radar |
| **Farmakom WhatsApp AI** — non visto nel radar | disponibilità dal gestionale, prenotazioni, vendita su WhatsApp | **14 giorni gratis** | 99-199 € + 500 € di attivazione. **La "vendita diretta via WhatsApp" dei farmaci va letta con la regola sulla vendita a distanza: non verificato.** Voce non dichiarata |
| **AssistenteFarmacia, Neurapharm** — non visti nel radar | FAQ, prenotazioni, promozioni su WhatsApp | demo | fanno "marketing WhatsApp" e promozioni: **rischio sul comma 525** (passo 2ter). Voce non dichiarata |

| Alternativa che sembra ragionevole | La frase che la smonta |
|---|---|
| il personale al banco che risponde | *da raccogliere nella voce*. Il conto del tempo (unità 4) |
| risposta automatica di WhatsApp, scheda Google con gli orari | copre solo gli orari |
| assistente WhatsApp per farmacie | **non ho una frase che lo smonti.** Il possibile vantaggio (telefono, configurazione fatta da noi) va verificato |

---

## 7. Le obiezioni di questo settore

**Non si può compilare: manca la voce del settore.**

Tre obiezioni prevedibili, **senza risposta nei materiali LML:**
- *"C'è già il WhatsApp per farmacie, e me lo fanno provare gratis."*
- *"E se dice una cosa sbagliata su un farmaco?"* La risposta onesta è: non ne parla, passa a te.
- *"I dati dei miei pazienti dove vanno?"* Il fatto che i dati restino in Italia aiuta (product-marketing), ma su WhatsApp e sui dati sanitari serve la verifica legale.

---

## 8. Il formato

- **Inserzioni sopravvissute rivolte alle farmacie:** 0. Il formato delle 3 di leia.pharma non è misurato.
- **Risorse nostre:** voce di ARYA `[DA CHIEDERE A IVAN]`, video di Ivan `[DA CHIEDERE A IVAN]`, nessuna farmacia dimostrativa.
- **Scelta di partenza:** nessuna. **Il settore non è nella §10.1**, e la strada suggerita dal passo 5 è il partner, non Meta. *In ogni caso il formato lo decide la spesa, non questa scheda.*

---

## 9. Prezzo e qualificazione

- **Fascia di prezzo:** `[DA CHIEDERE A IVAN]`. Serve almeno la fascia Pro, per la voce e per il collegamento al gestionale. Concorrenti: 99-199 € più 500 € di attivazione, con prova gratuita.
- **La domanda che qualifica:** "Quante chiamate o messaggi ricevi in un giorno?" Soglia proposta: **20** `[DA CONFERMARE A IVAN]`.
- **Le tre domande della chat, adattate** (servono al conto del tempo):
  1. Quante telefonate arrivano mentre servite al banco?
  2. Che gestionale usate?
  3. Fate servizi su prenotazione (holter, misurazioni, telemedicina)?

---

## 10. I cancelli

| Condizione | Stato | Note |
|---|---|---|
| Radar da meno di 30 giorni | **in parte** | la panoramica del 14/09 c'è; un radar dedicato no |
| Voce fatta | **no** | — |
| Cosa fa ARYA: confermato | **in parte** | risposte di Ivan del 14/09, ristrette dai vincoli di legge; gestionali di farmacia non verificati |
| Almeno una prova del settore, o decisione di partire senza | **no** | `[DA CHIEDERE A IVAN]` |
| Partner verificato (§22.1) | **no** | `[DA CHIEDERE A IVAN]`. Qui è la strada principale |
| Settore riconosciuto nella §10.1 | **no** | **le farmacie non sono fra gli otto settori.** Serve una modifica approvata |
| Chi risponde ai contatti e in quanto tempo (§11) | **no** | il flusso di ARYA non è ancora provato con 20 contatti finti |
| Massimo due campagne attive (§0.1) | **sì** | nessuna campagna su lml-adv |
| **Verifica legale** (cancello aggiunto per questo settore) | **no** | passo 2ter |

**Esito: BOZZA.** Su nove cancelli: uno "sì", due "in parte", sei "no".

---

## 11. Da segnalare a Ivan

1. **Sulla vendita persa il conto non regge.** Una richiesta vale circa 4,50 € di guadagno (stima). I servizi sono meno di 7 al mese per farmacia. Il CUP vale 2 €. **Regge solo il conto del tempo al banco**, da 20 chiamate al giorno in su, ed è un conto sul tempo, non sulla cassa.
2. **Il prezzo si confronta con assistenti WhatsApp fatti per le farmacie, italiani, da 99 € al mese e con prova gratuita.** È la situazione peggiore delle tre schede.
3. **Le cose che valgono di più per un titolare sono vietate o rischiose per un assistente automatico:** consigli sui farmaci, promozioni sui servizi, ricette su WhatsApp. Anche il "ricontatta e manda promozioni" del caso rivenditore qui non si può fare.
4. **Il settore non è nella §10.1.** Aprirlo richiede una tua modifica approvata e una verifica legale che negli altri settori non serve.
5. **Se si vuole entrare, la strada è un partner**: un gestionale di farmacia o un fornitore di telemedicina con migliaia di farmacie. Non Meta.
6. **L'unico spazio possibile è il telefono.** I concorrenti visti parlano di WhatsApp; da verificare con un radar dedicato se qualcuno copre la voce.

---

## 12. Storico

| Data | Cosa è cambiato | Chi |
|---|---|---|
| 15/09/2026 | Prima stesura, in BOZZA. Passo 2bis compilato per primo, su cinque unità, con un verdetto esplicito: sulla vendita il conto non regge. Aggiunti il passo 2ter (vincoli di legge e deontologia), il confronto con le schede e-commerce e ricettivo, e un nono cancello (verifica legale). Passi 2 e 7 vuoti perché manca la voce | Claude, su richiesta di Ivan |
