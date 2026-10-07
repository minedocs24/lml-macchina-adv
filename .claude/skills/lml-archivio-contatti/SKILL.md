---
name: lml-archivio-contatti
description: Governa l'archivio dei contatti pubblicitari di LML Technologies — come ogni conversazione WhatsApp nata da un'inserzione entra nell'archivio portandosi dietro il blocco e l'inserzione da cui viene, quali stati esistono e chi li cambia, come si tiene pulito, cosa si conserva e per quanto, e come i contatti buoni tornano a Meta. Usa SEMPRE questa skill quando l'utente parla dell'archivio contatti, del CRM della pubblicità, di "dove finiscono i contatti", "da quale inserzione arriva questo contatto", "come li segniamo", "quanti ne abbiamo di buoni", di stati dei contatti, di pulizia dell'archivio, di quanto tempo si tengono i dati, o di rimandare a Meta i contatti validi. È l'undicesimo anello della catena pubblicitaria LML: senza di esso la lettura dei numeri si ferma alle chat e nessun angolo può essere giudicato. Non contatta nessuno e non scrive su Meta senza approvazione.
---

# Archivio contatti — dove finisce quello che abbiamo pagato

**Versione 1.0 — 13 settembre 2026.** Governa la struttura e le regole dell'archivio. Non contatta nessuno. Non scrive su Meta senza il sì di Ivan.

## A cosa serve, in una riga

Un contatto che arriva senza sapere **da quale inserzione viene** è un contatto pagato e sprecato a metà: si può ancora vendergli qualcosa, ma non insegna niente. Questa skill fa in modo che ogni conversazione porti con sé la sua provenienza, e che il suo destino — scartato, call fissata, cliente — torni indietro attaccato a quel blocco.

Senza questo pezzo, la §26 vieta di giudicare le campagne: sapremmo quante chat portano, non quali valgono. E la coda degli angoli resterebbe per sempre un'opinione.

## Come si sa da dove viene un contatto — il fatto tecnico

Questo è il pezzo che tiene in piedi tutto, e va capito bene.

Quando una persona tocca il pulsante di un'inserzione e si apre WhatsApp, **Meta attacca al primo messaggio un pacchetto di informazioni sull'inserzione**. Arriva insieme al messaggio, automaticamente, senza che nessuno debba chiedere niente. Contiene:

| Cosa arriva | A cosa serve |
|---|---|
| **Un codice del clic** (Meta lo chiama *ctwa_clid*) | È l'unico modo di dire a Meta, più tardi, "questo contatto era buono". Lo genera Meta e **non si può inventare** |
| **Il numero dell'inserzione** | Dice esattamente **quale creatività** ha portato quella persona: non la campagna, la singola inserzione |
| Il titolo e il testo dell'inserzione | Servono a far partire la conversazione dal punto giusto |
| Il tipo di file (immagine o video) e il collegamento al post | Utili al controllo |
| Il messaggio di apertura precompilato | Conferma quale versione ha visto |

**Tre cose che vanno sapute:**

1. **Arriva solo con il primo messaggio.** Se non viene salvato lì, è perso: nei messaggi successivi non c'è più.
2. **Alcune piattaforme lo buttano via.** È un problema documentato: il pacchetto arriva da Meta ma la piattaforma di mezzo non lo passa a chi deve usarlo. **Va verificato con una prova vera**, non dato per scontato. È la prima domanda per Roberto.
3. **Se non c'è, il contatto è organico.** Qualcuno che ha trovato il numero da solo, o da un QR, o perché glielo ha passato un collega. **Non è un errore ed è un contatto prezioso**: semplicemente non viene dalla pubblicità, e va segnato così. Fingere che venga da un'inserzione gonfia i numeri e fa imparare a Meta la cosa sbagliata.

E una conseguenza pratica che le fonti segnalano: **la prima risposta deve usare quello che il cliente ha appena visto.** Se l'inserzione parlava del lunedì mattina e ARYA risponde "Ciao, come possiamo aiutarti?", si butta via il gancio appena pagato, e la percentuale di chi abbandona al secondo messaggio sale parecchio. Il pacchetto contiene il titolo dell'inserzione proprio per questo.

## Prima di cominciare — leggi sempre

1. `regole-adv.md`: §10 (contatto valido), §10.1 (i settori riconosciuti), §11 (chi risponde e in quanto tempo), §12 (consenso e ricontatto), §13 ("come ci hai conosciuto"), §24 (i dati non stanno solo dentro Meta), §26.
2. `angoli/<settore>.md` — i blocchi in corso, per sapere quali nomi devono comparire.
3. `settori/<settore>.md` — la soglia di qualificazione del settore.
4. Il file dell'archivio, se esiste.

Dichiara versione e data di ogni file letto.

## Le regole che governano l'archivio

**1. Un contatto, una riga, un posto solo.** L'archivio è l'unica copia buona. Se lo stesso contatto sta anche in un foglio di qualcuno, prima o poi i due divergono e nessuno sa quale vale.

**2. Pochi stati, definiti prima.** Le fonti convergono: fra sei e dieci stati, e definiti **prima** che arrivi il primo contatto, non dopo. Sotto trovi i nostri.

**3. Chi cambia uno stato è una persona sola.** Per ogni passaggio c'è un responsabile. Due persone che segnano lo stesso contatto in modi diversi producono numeri che non tornano.

**4. Un contatto arriva con il suo contesto, o non arriva.** Un contatto senza provenienza, senza le risposte alle domande di qualificazione e senza la data, è una riga che non serve a niente.

**5. La qualificazione la fa una persona, non un punteggio.** Nella letteratura la distinzione è fra un contatto che *sembra* buono e uno che *una persona ha verificato parlandoci*. Per noi: la chat porta il contatto al livello "valido"; solo la call lo porta più avanti.

**6. I dati escono da Meta.** §24: l'archivio vive fuori, e i numeri si leggono da lì. Meta dice quante chat, non quante ne valgono.

## Gli stati

Sette, più due terminali. In questo ordine.

| Stato | Vuol dire | Chi lo mette |
|---|---|---|
| **nuovo** | La conversazione è arrivata, nessuno ha ancora parlato | automatico |
| **in lavorazione** | Si sta parlando, la qualificazione non è finita | chi risponde |
| **scartato** | Non è un cliente per noi. **Sempre con il motivo** | chi risponde |
| **valido** | Ha superato le tre domande: settore, volume, chi decide | chi risponde |
| **call fissata** | C'è un appuntamento con data e ora | chi risponde |
| **call fatta** | L'incontro è avvenuto | chi fa la call |
| **non ora** | Interessato ma non adesso. **Con la data del ricontatto** | chi fa la call |
| **attivazione** | È diventato cliente | Ivan |
| **perso** | Dopo la call, non se ne fa niente. **Con il motivo** | chi fa la call |

**Il numero che conta è "valido"** (§10). Le chat non sono contatti; i contatti validi sì. **Il numero che conta davvero è "call fissata"**, perché è l'obiettivo dichiarato della campagna.

**"scartato" e "perso" vogliono sempre il motivo**, da una lista corta: volume troppo basso, settore fuori, non è il titolare, cercava altro, fornitore, studente, nessuna risposta. Senza il motivo non si impara niente, e il motivo più frequente è spesso un'indicazione su come stringere il pubblico o il testo.

## I campi

Divisi in tre gruppi: quelli che arrivano da soli, quelli che si raccolgono parlando, quelli che si aggiungono dopo.

### Arrivano da soli, dal primo messaggio

| Campo | Note |
|---|---|
| Data e ora del primo messaggio | |
| Numero di telefono | È il dato personale principale: vedi la sezione sui dati |
| **Codice del clic** | Serve solo per il ritorno a Meta. **Non si guarda e non si usa per altro** |
| **Numero dell'inserzione** | |
| **Blocco e angolo** | Ricavati dal nome dell'inserzione, oppure dal messaggio di apertura |
| Titolo dell'inserzione visto | |
| **Provenienza** | `inserzione` oppure `organico` |

### Si raccolgono parlando

| Campo | Da dove |
|---|---|
| Nome e azienda | chat |
| **Settore** | chat — la §10.1 lo richiede, e i moduli dell'agenzia non lo chiedevano: è stato un buco vero |
| **Chiamate o messaggi al giorno** | la domanda che qualifica |
| Chi è (titolare, direzione, dipendente) | il segnale più forte che abbiamo visto: fra i contatti buoni il titolare c'era nel 52% dei casi contro il 30% |
| Cosa vorrebbe automatizzare | |
| **Consenso al ricontatto** | §12 |

### Si aggiungono dopo

| Campo | Quando |
|---|---|
| Stato, e data di ogni cambio | sempre |
| Motivo dello scarto o della perdita | scartato / perso |
| Data e ora della call | call fissata |
| Esito della call | call fatta |
| **"Come ci hai conosciuto?"** a testo libero | in call, non in chat (§13) |
| Data del prossimo ricontatto | non ora |
| Tempo dalla prima risposta | automatico se possibile |

**Il tempo di risposta va misurato.** La §11 lo chiama la leva col ritorno più alto di tutto il documento, e non costa un euro. La base è uno studio del 2007 di James Oldroyd (MIT Sloan, con InsideSales, oltre 15.000 contatti e 100.000 chiamate): rispondere entro 5 minuti invece che entro 30 rende **100 volte** più probabile raggiungere la persona e **21 volte** più probabile qualificarla. Un articolo successivo sulla *Harvard Business Review* (2011, 2.241 aziende) ha trovato che la risposta media arrivava dopo 42 ore e che un'azienda su quattro non rispondeva mai. Sono numeri americani e di quasi vent'anni fa, ma nessuno studio dopo li ha smentiti nella direzione. Nei dati dell'agenzia era zero su 152: nessuno richiamato entro 5 minuti. Se l'archivio non lo registra, non lo si può migliorare.

## Il ritorno a Meta

Meta impara da quello che gli si dice. Se non gli si dice niente, ottimizza per **portare tante chat**, non per portare quelle giuste — e il costo per contatto buono sale settimana dopo settimana anche quando il costo per chat scende. È esattamente quello che era successo: 4,51 € per contatto contro **33 € per contatto buono**.

Per rimandare indietro un contatto buono serve il **codice del clic** salvato al primo messaggio. Senza quello, il ritorno viene accettato ma non collegato all'inserzione: non serve a niente e sporca i numeri.

Due strade, e la decisione è di Ivan:

| | Come funziona | Cosa comporta |
|---|---|---|
| **A mano, ogni settimana** | Ivan invia l'elenco dei validi | Semplice, nessuna scrittura automatica. Più lento a insegnare |
| **Automatico dalla piattaforma** | La piattaforma manda l'evento appena il contatto diventa valido | Impara più in fretta. **Richiede un'eccezione scritta in regole-adv**, perché oggi ogni scrittura su Meta vuole il sì di Ivan |

**Regola in ogni caso: si rimanda indietro solo quello che è successo davvero.** Mai un contatto organico spacciato per pubblicitario, mai un "valido" che non lo è. Gonfiare quel numero insegna a Meta a portare più gente come quella sbagliata.

## I dati personali

L'archivio contiene numeri di telefono, nomi e aziende. Non è un dettaglio.

- **Accesso limitato** a chi lavora davvero i contatti.
- **L'informativa sta nel primo messaggio** della chat, con il collegamento (§12).
- **Il consenso al ricontatto è un campo**, non una supposizione. Chi non lo dà si può richiamare per quella conversazione, non inserire in invii successivi. È lo stesso errore già visto: in una lista di 87 indirizzi, 43 avevano detto no.
- **Quanto si tiene:** va deciso da Ivan con chi segue la privacy, e **scritto nell'archivio stesso**. Un archivio senza una scadenza cresce per sempre.
- **Il codice del clic** non è un dato commerciale: serve solo al ritorno a Meta. Non si usa per altro, non si esporta, e si cancella con il resto.
- **Le frasi dei clienti** che finiscono nella scheda voce vanno prese **senza il nome e senza l'azienda**.

## La manutenzione

Poca e regolare, meglio che tanta e mai.

**Ogni settimana**, insieme al report:
- contatti fermi in "nuovo" o "in lavorazione" da più di 3 giorni;
- call fissate e non fatte — è il caso peggiore: contatto pagato, tempo speso, e la persona si è sentita dare buca;
- contatti senza provenienza: quanti, e **se sono tanti c'è un problema tecnico**, non un caso;
- "non ora" con il ricontatto scaduto.

**Ogni mese:**
- doppioni sullo stesso numero;
- righe senza settore o senza volume: sono contatti che non si possono contare;
- confronto fra quanti contatti dice Meta e quanti ce ne sono in archivio. **Se ballano, si scopre perché.** È già successo: 154 importati contro 166 dichiarati.

## La prova, prima di partire

Prima della prima campagna, **20 conversazioni finte** (è già nella scaletta), con questo scopo in più:

1. Il pacchetto della provenienza arriva e viene salvato? **È la verifica che vale più di tutte.**
2. Lo stesso numero che scrive due volte fa una riga o due?
3. Un contatto da scartare finisce in "scartato" con il motivo?
4. Il tempo di risposta viene registrato?
5. Un contatto organico viene segnato come organico?

Finché queste cinque cose non passano, la campagna produce contatti che non insegnano niente.

## Regole vincolanti

1. **Ogni contatto porta la sua provenienza, o è segnato organico.** Mai inventata.
2. **Il codice del clic si salva al primo messaggio** o è perso.
3. **Un contatto, una riga, un posto solo.**
4. **Scartato e perso vogliono il motivo.**
5. **"Valido" lo mette una persona**, dopo le tre domande. Non un automatismo.
6. **Si rimanda a Meta solo quello che è successo davvero.**
7. **L'archivio non si esporta fuori** dalla cartella ad accesso limitato.
8. **La skill non contatta nessuno** e non scrive su Meta senza il sì di Ivan.
9. **Non si cambia uno stato al posto di chi lo possiede.** Se una riga sembra sbagliata, si segnala.

## Cosa entra e cosa esce

**Entra:** una domanda sull'archivio, o il momento della manutenzione.

**Esce:** la struttura dell'archivio se non c'è ancora (`references/struttura-archivio.md`), il rapporto di manutenzione, oppure la risposta alla domanda. E le segnalazioni.

## Cosa fa dopo, e chi

La **lettura dei numeri** prende da qui i contatti validi e le call per blocco, e li porta nella **coda degli angoli**. Il **semaforo mattutino** legge da qui le chat senza risposta e le call saltate. La **voce del settore** prende da qui le frasi vere dei clienti, senza nomi.

Va segnalato subito in chat: contatti senza provenienza sopra il 10% (è un problema tecnico); una call fissata e non fatta; il tempo di risposta che sfora i 30 minuti, perché la §17 blocca gli aumenti di budget quando succede; un motivo di scarto che si ripete (il pubblico o il testo vanno stretti); un consenso mancante su un contatto che qualcuno vuole ricontattare.
