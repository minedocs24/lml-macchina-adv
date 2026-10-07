---
name: lml-copione-video
description: Scrive i discorsi e i copioni di regia dei video parlati di Ivan Arpino / LML Technologies — dalla ricerca dell'angolo di attualità fino al copione blocco per blocco con ritmo, silenzi cronometrati, zoom, icone e suoni già assegnati alle parole. Usa SEMPRE questa skill quando l'utente chiede di scrivere, strutturare o preparare un video, un discorso, un copione, uno script o un reel, quando chiede "cosa dico nel video", "trovami argomenti per un video", "come lo struttturo", "dimmi dove fare le pause", oppure quando chiede argomenti di tendenza da cui ricavare un contenuto — anche se non nomina la skill, non nomina il copione e dice solo "aiutami con un video", "scrivimi due righe da dire" o "mi serve un contenuto su questo tema". Copre la fase che precede la ripresa; il montaggio effettivo dentro ChatCut lo esegue lml-montaggio-video.
---

# LML — Copione e regia dei video parlati

Sistema di scrittura per i talking head di Ivan Arpino destinati a Instagram, LinkedIn e WhatsApp. Produce due cose: **il discorso** (cosa si dice) e **il copione di regia** (come si dice e cosa ci si costruisce sopra in montaggio).

Il principio guida: **un video, un picco.** Tutto il resto della struttura esiste per portarci e per scaricare dopo. Un video con quattro momenti forti non ne ha nessuno.

Confine con le altre skill:
- **Questa skill** si ferma prima della ripresa. Consegna il copione.
- **`lml-montaggio-video`** prende il girato ed esegue in ChatCut. Le indicazioni prodotte qui sono scritte per essere eseguibili da quella skill senza traduzione.
- **`lml-tech-content-system`** governa lessico e registro verso le persona LML. Va rispettato, ma qui il registro è quello del profilo personale: nessuna vendita, nessuna CTA commerciale.

---

## Pipeline

Le fasi vanno in quest'ordine. Non saltare alla scrittura senza aver fatto la ricerca: un copione costruito su un dato generico si riconosce dalla prima riga.

1. **Ricerca dell'angolo** — cosa si muove adesso, con fonti datate
2. **Scelta** — angolo e formato, decisi dall'utente
3. **Discorso** — il testo parlato, in blocchi
4. **Copione di regia** — ritmo, silenzi, zoom, icone, suoni
5. **Consegna** — file markdown + note editoriali in chat

---

## Fase 1 — Ricerca dell'angolo

Cerca sempre sul web, mai a memoria. Gli argomenti AI-azienda invecchiano in settimane.

**Cosa cercare, in ordine di forza:**

1. **Scadenze normative appena maturate o imminenti.** Sono l'unico tipo di contenuto che genera urgenza reale e datata. Una data è un gancio che si difende da solo.
2. **Equivoci diffusi.** Il gancio più forte non è un dato nuovo: è una cosa che il pubblico crede vera e che è vera a metà. Cerca esplicitamente le semplificazioni che stanno circolando su un tema, non solo il tema.
3. **Numeri di ricerche italiane recenti** (Osservatori Politecnico di Milano, ISTAT, associazioni di categoria) — parlano al tessuto PMI meglio delle survey americane.
4. **Divari** tra ciò che si dichiara e ciò che si fa (adozione vs produzione, investimento vs ritorno). Reggono bene perché il pubblico si riconosce nella metà scomoda.

**Regole non negoziabili sulle fonti:**

- Ogni cifra citata nel video deve venire da una fonte trovata, con la sua data. **Mai inventare percentuali, nemmeno come figura retorica** ("nove volte su dieci", "tre aziende su quattro"). Se serve un'espressione di frequenza, usane una qualitativa.
- Preferisci fonti primarie (comunicati degli Osservatori, testi normativi, report firmati) agli aggregatori.
- Se una scadenza è stata modificata o rinviata, verifica **quale parte** è stata rinviata e quale no. È esattamente lì che si annida l'equivoco da cui nasce il gancio.
- Quando le fonti divergono su un numero, scegli la formulazione più difendibile o riporta il numero senza pseudo-precisione.

**Come presentare la ricerca:** quattro angoli al massimo, ciascuno con il gancio, il dato che lo regge e una riga sul perché funziona. Poi **dichiara la tua preferenza e argomentala** — l'utente si aspetta una scelta, non un menù neutro. Chiudi con un selettore per angolo e formato.

---

## Fase 2 — Formato e durata

| Formato | Durata | Parole parlate |
|---|---|---|
| Reel corto | 25–35s | 60–80 |
| Reel standard | 60–90s | 150–220 |
| Video lungo | 3–5 min | 450–750 |

Calcolo: **~150 parole al minuto** di parlato, **più la somma dei silenzi prescritti** (in un reel standard sono 3–5 secondi complessivi, non trascurabili). Conta sempre e dichiara la durata stimata. Se il testo sfora, non tagliare a caso: indica nel copione **i due punti esatti** dove il testo ripete un concetto già passato.

---

## Fase 3 — L'architettura del discorso

Sette blocchi. Non tutti obbligatori nei formati corti, ma l'ordine sì: è una curva di energia, non un elenco di argomenti.

**0 — Attacco** *(5–8s)*
Enuncia la credenza diffusa, poi smontala a metà. La formula che tiene: *"Hai letto che X. È vero a metà. E la metà che manca è quella che riguarda te."* La prima frase va scritta per essere **buttata via**, non per essere enfatizzata.

**1 — Tensione** *(12–18s)*
Il contesto vero, detto piano, e poi il cambio di marcia. Qui entra la scadenza, la norma, il numero. Isola su una riga da sola la parola-concetto centrale.

**2 — Corpo spiegato** *(15–20s)*
L'unico momento didattico. Volume più basso, tono discorsivo, come se lo si dicesse a una persona sola. Traduce la norma o il dato in conseguenze concrete e riconoscibili.

**3 — L'equivoco** *(15–20s) — PICCO**
Metti in bocca al pubblico la sua obiezione, virgolettata, in un registro leggermente diverso. Poi **fermati.** Il silenzio che segue è il momento in cui lo spettatore si riconosce, e serve un secondo vuoto perché accada. Subito dopo, la parola che ribalta — detta lentissima, isolata.

**4 — Il dettaglio a bassa energia** *(10–12s)*
Volutamente sottotono: una data trascurata, una conseguenza laterale, detta a mezza voce. È il riposo tra il picco e la chiusura. **Se resta alto, il finale non ha da dove salire.**

**5 — Il numero** *(6–10s)*
La cifra che pesa. Lentissima, volume basso, ogni parte staccata da una pausa. Non alzare mai la voce su un numero: si difende da solo e caricarlo lo fa sembrare uno spot.

**6 — Chiusura** *(12–16s)*
Si scarica: velocità e volume scendono. Non vendere. Ribalta il problema in una frase finale che non chiede niente — la formula che funziona è *"il problema non è A, è B"*, dove B è una cosa che il pubblico non aveva considerato. L'ultima frase è la più lenta del video e va lasciata cadere, senza enfasi sull'ultima parola.

---

## Fase 4 — Ritmo e silenzi

**I silenzi vanno recitati, non montati.** Se in ripresa si attacca la frase successiva, in montaggio quel silenzio non esiste più e non si può inventare. Vanno scritti nel copione con la durata e ripetuti nelle note di ripresa.

Notazione: `// 0,5s` su riga propria.

**Durate:**

| Posizione | Durata |
|---|---|
| Silenzio del picco (dopo l'obiezione virgolettata) | 0,6s — il più lungo del video |
| Prima di una data o di una cifra | 0,5s |
| Dopo una parola isolata su riga propria | 0,4–0,6s |
| Stacchi interni di respiro | 0,3–0,35s |
| Testa del video | 0,1s |
| Coda | 0,2–0,25s |

Sotto i 0,3s non prescrivere pause: non si percepiscono e in montaggio si sente il taglio.

**Regole di andatura:**

- **La prima frase corre.** È contesto. Se la si recita con enfasi, il pubblico pensa che il messaggio sia quello.
- **Frenata secca sul cambio di marcia.** Il punto in cui il video passa dal riportare al dire.
- **Gli elenchi accelerano, poi si frena sulla parola operativa.** Tre o quattro voci quasi attaccate, poi stop pieno sul verbo che dice cosa cambia.
- **Il virgolettato cambia registro.** L'obiezione del pubblico va detta più veloce e sbrigativa, con voce d'altri.
- **La parola che ribalta è la più lenta.** Staccata, quasi sillabata.
- **La chiusura decelera progressivamente**, non di colpo.

---

## Fase 5 — Cosa si costruisce sopra

Le indicazioni si ancorano **a parole precise**, mai a intervalli di tempo. Se un elemento non nasce da una parola, non va messo.

### Regole di sottrazione *(vengono prima di tutto il resto)*

Non mettere **nulla** — né icona, né suono, né movimento — in questi quattro punti:

1. **I primi 6–8 secondi.** Solo faccia e sottotitoli. Qualsiasi grafica ruba attenzione alla frase che deve agganciare.
2. **Il silenzio del picco.** Se ci metti qualcosa, hai buttato il picco.
3. **La parola che ribalta il senso.** Qui lavora il sottotitolo da solo, in ambra. Un'immagine se la contende.
4. **Le cifre.** I numeri a schermo sono già l'elemento. Un'icona toglierebbe peso invece di aggiungerlo.

### Zoom

Massimo **uno ogni secondo e mezzo**. Se due picchi sono ravvicinati, ne prende uno solo: **il secondo resta piatto**, due punch vicini si annullano.

- **punch** → sulla parola che gira il senso del discorso
- **slow-push** → un solo movimento continuo sotto tutto il blocco didattico, che si avvicina senza stacchi
- **hold** → sulla chiusa, così l'ultima frase respira invece di finire secca; e sui dettagli a bassa energia, dove un punch sarebbe fuori scala

In un reel standard: 3–4 punch, 1 slow-push, 2 hold. Se ne servono di più, il discorso ha troppi picchi e va riscritto.

### Icone

Una per beat, non una ogni tot secondi. Regole complete in `lml-montaggio-video`; qui contano tre cose in fase di scrittura:

- **Oggetto fisico concreto**, mai forme astratte, lampadine, ingranaggi. Test: coperti i sottotitoli, l'icona da sola deve dire di cosa si parla.
- **Il gesto racconta.** Non compare finita: il calendario perde i fogli, la data si cerchia, lo schema si ramifica, il foglio si compila riga per riga.
- **Fai sistema.** Due icone imparentate a distanza (calendario da parete all'inizio → calendario da tavolo più avanti) fanno sembrare il video una cosa sola. Ripeterne una identica no.

In un reel standard: 6–8 icone.

### Suoni

**Varia sempre.** Quattro effetti identici diventano rumore.

- **Riser** basso in apertura, **tagliato netto** sul primo silenzio: l'orecchio si accorge del vuoto prima che il cervello capisca la frase.
- Lo **stesso riser rovesciato**, in decadenza, sotto l'ultima frase. Chiude il cerchio sonoro senza che nessuno lo noti consapevolmente.
- **Un solo impatto grave** per cifra. Se le cifre sono due, la seconda arriva nuda: è più cattiva così.
- **Pop** sull'ingresso delle icone, **whoosh** su ciò che scivola, **tick** brevi sugli elenchi, **thud** sui timbri, tratti di penna e scratch dove c'è scrittura a mano.
- Sui silenzi prescritti: **muto assoluto**, nessuna coda di riverbero, nessun letto sonoro.

---

## Consegna

Il copione va in un file markdown in `/mnt/user-data/outputs/`, presentato con `present_files`. Non incollarlo interamente in chat: è un documento che si consulta durante la ripresa e dentro ChatCut.

**Struttura del file:**

1. Titolo, durata stimata, formato
2. Legenda della notazione (`//` = silenzio da rispettare in ripresa)
3. Un blocco per sezione, ciascuno con: **timecode → testo parlato con i silenzi inline → RITMO → MONTAGGIO**
4. **Tabella di riepilogo tecnico**: quantità di silenzi, punch, hold, icone, suoni, con i punti di aggancio
5. **L'elemento più sacrificabile**, indicato per nome, se il montato risulta sovraccarico
6. **I due punti di taglio** se serve rientrare nella durata
7. **Note di ripresa**: le pause vanno recitate; restare fermi e in camera durante il silenzio del picco; girare un secondo di margine in testa e in coda

**Nel messaggio in chat**, non elencare cosa hai scritto. Racconta tre o quattro scelte editoriali e il perché: dove sta il picco e come è costruito, dove hai tolto grafica di proposito, cosa tiene insieme il video. Chiudi con l'avvertimento pratico più utile (durata al limite, punto rischioso in ripresa).

---

## Lessico e registro

Persona di riferimento: **titolare o CEO di PMI**. Registro caldo, autorevole, orientato al valore. Si parla di conseguenze, non di tecnologia.

**Da non fare mai:**

- Vendere. Nessuna CTA commerciale, nessun "contattami", nessun servizio nominato.
- Cliché AI: "rivoluzione", "game changer", "il futuro è adesso", "non è fantascienza".
- Percentuali inventate o arrotondate per comodità.
- Enfasi sull'ultima parola della chiusura.
- Aprire con un dato. Si apre con una credenza da smontare; il dato arriva al secondo blocco.

**Da fare:**

- Frasi brevi, una proposizione per riga.
- Parole isolate su riga propria dove serve peso.
- Termini tecnici usati **una volta sola e spiegati subito dopo** — sono il punto in cui lo spettatore si riconosce, non un'occasione per dimostrare competenza.
- Chiudere ribaltando il problema, non riassumendolo.

Palette, font e coordinate delle icone: vedi `lml-montaggio-video`. Tratto crema, estrusione blu notte, ambra come unico accento.
