---
name: lml-coda-angoli
description: Trasforma una scheda settore CONFERMATA di LML Technologies in una coda ordinata di angoli pubblicitari — ognuno con momento d'ingresso, promessa ammessa, prova, obiezione a cui risponde e livello di consapevolezza del cliente — e dice quale angolo entra in campo adesso, quali aspettano e perché; poi, blocco dopo blocco, riordina la coda in base ai risultati. Usa SEMPRE questa skill quando l'utente chiede "quale angolo usiamo", "con cosa partiamo", "che gancio proviamo", "la coda degli angoli", "cosa testiamo dopo", "il prossimo blocco", "l'angolo ha funzionato?", oppure quando una scheda settore passa a CONFERMATA o un blocco di campagna finisce — anche se non nomina la skill e dice solo "adesso decidiamo cosa dire ai rivenditori". È il quarto anello della catena pubblicitaria LML: dopo la scheda settore, prima del pacchetto inserzione. Non scrive testi e non tocca Meta.
---

# Coda degli angoli — cosa diciamo, in che ordine, e perché uno alla volta

**Versione 1.0 — 13 settembre 2026.** Scrive solo file nella cartella di lavoro. Non produce testi di inserzione. Non tocca Meta.

## A cosa serve, in una riga

La scheda settore dice cosa possiamo promettere e quali momenti sono liberi. Questa skill sceglie **cosa dire per primo**, mette il resto in fila, e tiene il registro di cosa ha funzionato — così dopo tre blocchi sappiamo *"gli angoli sul lunedì mattina funzionano"*, non *"l'inserzione 47 ha vinto"*.

## Le tre cose che la ricerca dice, e che governano tutto

**1. Un angolo non è una variante.** Chi fa questo mestiere separa sempre due cose: il **concetto** (un angolo diverso: altro momento, altra promessa, altra obiezione) e la **variante** (stesso angolo, cambia un dettaglio: il gancio, l'immagine, il titolo). Si provano i concetti per trovare quello che apre un pubblico; si provano le varianti per spremere un concetto che funziona. Confonderli è l'errore più comune.

**2. Con il nostro budget, un angolo alla volta.** Per giudicare un concetto servono circa 50 conversioni (regole-adv §17, e tutte le fonti di settore). A 10 € al giorno per campagna non ci sono i soldi per far correre due angoli l'uno contro l'altro: si farebbe rumore, non un test. Quindi **un angolo entra in campo per un blocco**, con tre o quattro creatività diverse dello stesso angolo dentro lo stesso gruppo, e Meta sceglie quale mostrare. Fra un blocco e l'altro cambia l'angolo. È lento, ma dopo ogni blocco sappiamo una cosa vera.

**3. Il livello di consapevolezza decide cosa può dire il gancio.** È lo schema di Eugene Schwartz (1966), ancora lo standard: il cliente può essere **inconsapevole** del problema, **consapevole del problema** ma non delle soluzioni, **consapevole delle soluzioni** ma non di noi, **consapevole di noi**, o **pronto**. Un'inserzione che parla di ARYA a chi non sa nemmeno che esistono assistenti telefonici AI viene ignorata; una che spiega il problema a chi ha già visto tre concorrenti annoia. La regola per il pubblico freddo di Meta: **il gancio parla del problema o della soluzione, mai del prodotto.** Il prodotto arriva dopo, nella chat.

## Prima di cominciare — leggi sempre

1. `settori/<settore>.md` — **deve essere CONFERMATA.** Se è BOZZA, fermati: la coda si costruisce solo su promesse ammesse.
2. `regole-adv.md`: §0.1, §5.1, §17, §18 (una creatività prova una cosa sola; 70/30), §20, §23, §26.
3. `.agents/product-marketing.md`: "Differentiation" (il nostro argomento è "rispondiamo e facciamo") e "Objections".
4. `voce/<settore>/` — l'ultima scheda: le frasi esatte dei momenti e dei dubbi.
5. `angoli/<settore>.md` — la coda precedente e gli esiti dei blocchi, se esistono.
6. Se un blocco è appena finito: la lettura dei numeri di quel blocco (dal report ADV).

Dichiara versione e data di ogni file letto.

## Cosa entra e cosa esce

**Entra:** il settore; la scheda settore confermata; eventualmente l'esito dell'ultimo blocco.

**Esce:** `angoli/<settore>.md` — un file solo per settore, aggiornato, con: la coda (massimo 5 angoli), l'angolo in campo, il registro dei blocchi con esito, gli angoli scartati con il motivo. Modello in `references/modello-coda.md`.

In chat: l'angolo proposto per il prossimo blocco, in cinque righe, con le tre cose (cosa cambia · quanto costa · cosa succede se non lo faccio). **La scelta finale è di Ivan.**

---

## Passo 1 — Comporre gli angoli candidati

Un angolo è una riga con **sei campi**, tutti presi dalla scheda settore e dalla voce, nessuno inventato:

| Campo | Da dove viene | Regola |
|---|---|---|
| **Momento** | scheda §2, quadranti | preferire "frequente e libero"; poi "frequente, presidiato da 1-2" |
| **Promessa** | scheda §3, colonna "sì" | **solo** dalla colonna "sì". Altrimenti l'angolo non esiste |
| **Prova** | scheda §4 | caso dello stesso settore > demo con voce vera > nessuna |
| **Obiezione a cui risponde** | voce, casella "Dubbio" | frase esatta |
| **Consapevolezza** | giudizio dalla voce e dal radar | problema / soluzione / prodotto (vedi `references/tipi-di-angolo.md`) |
| **Perché noi e non loro** | scheda §6 e radar | in una riga: cosa dice questo angolo che i concorrenti sopravvissuti non dicono |

Si compongono **tutti gli angoli possibili** (di solito 8-15), poi si scremano.

## Passo 2 — Scremare

Si scarta, e si scrive perché:
- ogni angolo la cui promessa non sta nella colonna "sì";
- ogni angolo senza prova, **salvo** decisione esplicita di Ivan nella scheda (§4: "partire senza prova, mostrando il prodotto");
- ogni angolo che coincide con la promessa più ripetuta dei concorrenti sopravvissuti **senza** aggiungere il "e fa" (§Differentiation: "chiamate perse" è già di Ambrogio; "risponde e fissa l'appuntamento" no);
- ogni angolo che parla del prodotto a un pubblico freddo (consapevolezza "prodotto" o "pronti" non si usa nel primo blocco, perché non esiste ancora un pubblico caldo — §0.1);
- ogni angolo che usa una parola di `customer-language.md` "da evitare" nella promessa.

Gli scartati restano nel file, con il motivo e la data: se cambia la scheda (un consenso arriva, ARYA impara una cosa nuova), si riaprono.

## Passo 3 — Ordinare

I sopravvissuti si ordinano con **quattro criteri, in quest'ordine**. Il primo che discrimina decide; i successivi rompono i pareggi.

1. **Il momento**: frequente e libero prima di tutto.
2. **La prova**: stesso settore prima della demo, demo prima di niente.
3. **La consapevolezza**: per il primo blocco, "problema" o "soluzione". "Prodotto" va in coda per quando esisterà un pubblico che ci ha già incontrato.
4. **La distanza dai concorrenti**: fra due angoli pari, quello che nessun sopravvissuto dice.

Ne restano al massimo **cinque** in coda. Gli altri si scrivono a parte come "riserva".

## Passo 4 — L'angolo in campo, e cosa prova il blocco

Il primo della coda entra in campo. Per il blocco si scrive, **prima** di produrre qualunque creatività:

- **Cosa prova questo blocco:** l'angolo. È l'unica variabile fra questo blocco e il prossimo.
- **Cosa non cambia:** settore, pubblico, destinazione (WhatsApp), budget, le tre domande della chat.
- **Le 3-4 creatività dentro il blocco** sono **varianti dello stesso angolo**: stessa promessa, stessa prova, stesso momento. Cambia l'esecuzione: un video con la faccia, la registrazione di ARYA, una tavola. Serve a non dipendere da una sola esecuzione — non a confrontare angoli.
- **Il gancio** di ogni creatività si scrive nel pacchetto inserzione, non qui. Ma la regola è già decisa: **parla del momento, non di ARYA.**
- **Quando si giudica:** non prima di 7 giorni pieni e 50 conversazioni (§26). Se dopo 21 giorni le 50 non arrivano, si giudica lo stesso, e si scrive che il giudizio è debole.
- **Cosa vuol dire "ha funzionato":** il costo per **contatto valido** (§10), non per chat. Il termine di paragone è il blocco precedente e il riferimento italiano (§17). Per il primo blocco non c'è confronto: il primo blocco misura, non giudica.

Il blocco riceve un **numero** e un **nome** che finisce nel nome della campagna e in ogni creatività: `B1-lunedi-mattina`, `B2-ordine-nel-gestionale`. È così che i numeri tornano indietro attaccati all'angolo.

## Passo 5 — Dopo il blocco: riordinare

Quando arriva la lettura dei numeri del blocco:

| Esito | Cosa fa la coda |
|---|---|
| **Ha funzionato** (costo per contatto valido sotto il riferimento, o migliore del blocco prima) | L'angolo resta in campo; il prossimo blocco prova **varianti** dell'angolo (70% del lavoro creativo, §18) e **un** angolo nuovo entra in coda per il blocco dopo (30%). L'angolo va nel registro come "provato: funziona", con i numeri |
| **Non ha funzionato** | L'angolo esce, va nel registro come "provato: non funziona", con i numeri e la lettura più probabile (era il momento? la promessa? l'esecuzione?). Il secondo della coda entra in campo. **Nessuna variante di un angolo che non ha funzionato** |
| **Giudizio debole** (meno di 50 conversazioni) | Si scrive così. L'angolo resta un blocco in più **solo** se il costo per chat è in linea; altrimenti si passa al secondo |
| **Le creatività si sono consumate** (frequenza sopra 3, costo che sale da 7 giorni, §20) ma l'angolo ha funzionato | Non è l'angolo: è l'esecuzione. Varianti nuove dello stesso angolo |

La coda si riordina **solo per quello che i numeri dicono**, non per stanchezza dell'angolo o per una nuova idea. Le nuove idee entrano come candidati al Passo 1, e passano la scrematura come tutti.

---

## Regole vincolanti

1. **Solo da schede CONFERMATE.** Mai da una bozza, mai da memoria.
2. **La promessa viene solo dalla colonna "sì".** È la regola che protegge da §23 e dall'AI Act: se non è lì, non si dice.
3. **Un angolo per blocco.** Le creatività dentro un blocco sono varianti dello stesso angolo. Mai due angoli nello stesso gruppo.
4. **Nessun testo.** L'angolo è una riga d'argomento in sei campi. Il gancio, il testo, il titolo li scrive il pacchetto inserzione.
5. **Il gancio parla del momento, non del prodotto.** Per il pubblico freddo, sempre.
6. **Massimo cinque in coda.** Il resto è riserva.
7. **Si riordina solo sui numeri.** Un angolo cambia stato quando arriva la lettura del blocco, non prima.
8. **Gli scartati restano scritti**, con il motivo. Un motivo può cadere.
9. **La scelta finale è di Ivan.** La skill propone il primo della coda con le tre cose; la campagna la crea la skill di scrittura sicura solo dopo il suo sì.

## Cadenza

Si costruisce quando la scheda settore diventa CONFERMATA. Si riapre **a ogni fine blocco** (ogni 2-3 settimane per settore aperto) e ogni volta che la scheda settore cambia. Non si riapre "perché sono passati dieci giorni".

## Dove si scrive

```
angoli/
  rivenditori.md
  e-commerce.md
```

Un file per settore, aggiornato, con il registro dei blocchi in fondo. Da Cowork si scrive direttamente; dalla chat si consegna il file. File di appoggio, rilettura, copia sul file buono.

## Cosa fa dopo, e chi

Il **pacchetto inserzione** prende l'angolo in campo — i sei campi e il nome del blocco — e scrive ganci, testi, titoli, messaggio di apertura della chat, per 3-4 creatività. Il **collaudo** verifica che ogni creatività dica la promessa dell'angolo e nient'altro. La **scrittura sicura su Meta** crea la campagna col nome del blocco. La **lettura dei numeri** riporta l'esito qui, attaccato al numero del blocco.

Va segnalato subito in chat: una scheda settore che torna BOZZA mentre un blocco è in campo (la promessa in campo potrebbe non reggere più); un angolo funzionante che coincide con un messaggio nuovo di tre concorrenti (il radar lo dirà: bisogna muoversi sulle varianti prima che diventi lingua comune); un blocco che arriva a 21 giorni senza 50 conversazioni (il problema può essere il pubblico o il budget, non l'angolo).
