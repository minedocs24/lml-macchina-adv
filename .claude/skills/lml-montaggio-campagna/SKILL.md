---
name: lml-montaggio-campagna
description: Monta su Meta una campagna LML Technologies partendo da un pacchetto inserzione collaudato e approvato — campagna, gruppo, creatività e inserzioni verso WhatsApp, create sempre in pausa, una scrittura alla volta, con i parametri esatti del connettore e una rilettura di verifica dopo ognuna. Usa SEMPRE questa skill quando l'utente chiede di creare, caricare, montare o "mettere su Meta" una campagna, un gruppo di inserzioni o un'inserzione, quando dice "carichiamo la campagna", "creala in pausa", "mettila su", oppure quando un pacchetto inserzione è passato al collaudo con esito verde. NON sostituisce la skill meta-scrittura-sicura, che resta invariata e governa ogni singola scrittura su Meta: questa la richiama e le si appoggia. Non attiva mai niente: l'attivazione è una decisione separata di Ivan.
---

# Montaggio della campagna su Meta

**Versione 1.0 — 13 settembre 2026.** Crea entità su Meta, sempre in pausa. Non attiva, non spende, non elimina.

## Una precisazione, perché conta

Esiste già una skill installata, **`meta-scrittura-sicura`**, che è la procedura da seguire per ogni scrittura su Meta. **Non va modificata.** Da questa sessione non è leggibile — è installata dal lato Cowork — quindi non è stata duplicata né riscritta: sarebbe stato un lavoro alla cieca.

Questa skill copre una cosa diversa: **il montaggio completo di una campagna**, dal pacchetto approvato alle inserzioni caricate. Dove si tratta di eseguire una singola scrittura, **si appoggia a `meta-scrittura-sicura`**: quella dice *come si scrive in sicurezza*, questa dice *cosa si monta e in che ordine*.

Prima volta che si usa da Cowork: leggere `meta-scrittura-sicura` e togliere da qui gli eventuali doppioni. La sovrapposizione non è un errore, ma è spreco.

## A cosa serve, in una riga

Trasformare un pacchetto approvato in una campagna reale su Meta, senza che si perda un nome, senza che qualcosa parta attivo, e con la certezza che quello che c'è dentro Meta è davvero quello che è stato approvato.

## Prima di cominciare — sempre, in quest'ordine

1. **Riverificare a quali account risponde il connettore.** È già cambiato una volta. Se l'account atteso non compare, **fermarsi**: non si monta su un account diverso da quello deciso.
2. `collaudi/<settore>/<blocco>-<data>.md` — **esito VERDE**. Giallo o rosso: non si monta.
3. **Il sì esplicito di Ivan** su questo montaggio. Un "procedi" generico su un piano non vale.
4. `inserzioni/<settore>/<blocco>.md` — il pacchetto: nomi, testi, messaggio di apertura, creatività.
5. `regole-adv.md` §8 (nomi), §9 (tetti), §24bis (stato tecnico).
6. **Contare le campagne attive.** Se questa sarebbe la terza, fermarsi (§0.1).

Dichiara versione e data di ogni file letto.

## Le regole della macchina, verificate

Lette dallo strumento a settembre 2026. Da riverificare se il connettore cambia: vedi `references/parametri.md` per l'elenco completo.

**I nomi dei parametri ingannano, e in due modi diversi.**
- Quando si **crea**: `campaign_name`, `ad_set_name`, `ad_name`, `campaign_daily_budget`.
- Quando si **modifica**: i nomi sono quelli dell'interfaccia di Meta, non quelli di creazione: `name`, `daily_budget`. Passare `campaign_name` a una modifica viene **rifiutato**.

**Tutto nasce in pausa da solo.** Campagne, gruppi e inserzioni vengono creati in pausa dal server: non è solo una nostra regola, è il valore predefinito. Buona notizia, ma si verifica lo stesso.

**Non si può eliminare.** Lo stato "eliminato" viene rifiutato e forzato a "in pausa". Quasi ogni errore è reversibile. **Irreversibili solo la spesa e la pubblicazione.**

**I budget sono in centesimi.** 10 € al giorno si scrive `1000`. Sbagliare un fattore cento è l'errore più caro possibile: **si rilegge sempre il numero prima di inviare**, e si verifica dopo.

**C'è un minimo di budget per valuta.** Va letto dall'account prima di impostare: per l'euro risultava 0,87 € al giorno. Sotto quel valore la creazione viene rifiutata.

**Le creatività non si modificano.** Per cambiare un testo, un titolo o un'immagine si crea una creatività nuova e un'inserzione nuova che la usa. Non si "corregge" un'inserzione esistente.

**La dichiarazione europea è obbligatoria.** Puntando all'Italia servono il beneficiario e il pagante: si scrivono espliciti, `LML Technologies S.r.l.` per entrambi. Se si omettono, Meta li riempie da solo con il nome del business — che potrebbe non essere quello giusto.

**Il pubblico ampio è già acceso.** Meta applica da sé l'allargamento del pubblico ai gruppi nuovi, e in quel caso l'età diventa un suggerimento, non un limite. Per noi va bene: il pubblico deve essere largo (§0.1). **Non si inventano mai identificativi di interessi**: o sono veri e forniti, o si usa solo la geografia.

**Le posizioni si scelgono dopo.** Il gruppo si crea senza forzare le posizioni: si lascia decidere a Meta, e si controlla nelle anteprime.

## Cosa entra e cosa esce

**Entra:** settore, blocco, e il sì di Ivan.

**Esce:**
- le entità su Meta, **tutte in pausa**;
- `montaggi/<settore>/<blocco>-<data>.md` — il verbale, secondo `references/verbale-montaggio.md`: ogni scrittura, i parametri inviati, il numero restituito, l'esito della rilettura;
- gli indirizzi delle anteprime, uno per posizione.

In chat: cosa è stato creato, in pausa, con i numeri, e **cosa serve per attivare**.

---

## Il montaggio, in sei passi

Si fa **una scrittura alla volta**, e dopo ognuna si rilegge. Mai due creazioni di fila senza verifica in mezzo.

### Passo 1 — Le fondamenta

- Riverificare gli account del connettore.
- Leggere il **minimo di budget** dell'account.
- Recuperare il **numero della pagina** LML: serve dentro le creatività e dentro il gruppo, ed è la causa numero uno di rifiuto quando manca.
- Verificare che l'account sia quello giusto, in euro, con il metodo di pagamento.

### Passo 2 — La campagna

Prima di scrivere, **presentare a Ivan i parametri esatti** e attendere il sì:

| Parametro | Valore |
|---|---|
| Nome | `ARYA - Call fissate - <Settore> - <mese anno>` |
| Obiettivo | quello che ammette le conversazioni (vedi `parametri.md`) |
| Tipo di acquisto | asta |
| Budget giornaliero | **1000** centesimi = 10 € |
| Categorie speciali | nessuna |

**La risposta alla creazione contiene l'elenco degli obiettivi di ottimizzazione validi** per quell'obiettivo, e quello consigliato. **Si legge quella lista e si usa un valore da lì**, invece di indovinare: un valore non valido viene corretto d'ufficio dal server, e il gruppo finisce ottimizzato per una cosa che non abbiamo scelto.

Poi si rilegge la campagna e si verifica: nome, stato in pausa, budget in centesimi giusto.

### Passo 3 — Il gruppo

Un gruppo solo, un angolo solo.

| Parametro | Valore |
|---|---|
| Nome | `<Settore> - Italia - Largo - B<n>-<angolo>` |
| Ottimizzazione | **conversazioni** (dalla lista del passo 2) |
| Destinazione | **WhatsApp** |
| Oggetto promosso | il numero della pagina — **obbligatorio** con WhatsApp |
| Addebito | impressioni |
| Pubblico | **solo geografia: Italia.** Nessun interesse |
| Beneficiario e pagante | `LML Technologies S.r.l.` |
| Budget | **niente qui**: sta sulla campagna |
| Finestra di attribuzione | **non toccare**: il valore predefinito va bene |
| Fasce orarie | non impostare, salvo decisione di Ivan |

Poi rilettura: nome, in pausa, destinazione WhatsApp, pubblico largo, nessun budget doppio.

### Passo 4 — I file

Le immagini e i video approvati si caricano nell'account. Due cose:

- **Il video ha un tempo di lavorazione.** Finché non risulta pronto, non si può usare in un'inserzione. Si aspetta e si verifica, non si tira a indovinare.
- Le immagini restituiscono un identificativo che va usato nelle creatività.

### Passo 5 — Le creatività e le inserzioni

Una per volta, tre o quattro in tutto, tutte dello stesso angolo.

Ogni creatività porta:
- **il numero della pagina** — se manca, l'inserzione viene rifiutata;
- il file (immagine o video);
- il testo principale e il titolo, **copiati dal pacchetto senza riscriverli**;
- il pulsante **"Invia messaggio"**;
- il **messaggio di apertura della chat**, quello precompilato, con dentro il nome del blocco.

Nome dell'inserzione: `B<n>-<angolo>-<C1|C2|C3>-<formato>-<gancio in due parole>`.

Dopo ognuna: rilettura, e **anteprima**.

### Passo 6 — Le anteprime, e il verbale

Si chiede l'anteprima di ogni inserzione per **almeno tre posizioni**: feed mobile, storie, Reels. L'anteprima restituisce un indirizzo: **va messo nella risposta a Ivan**, perché è il modo in cui lui apre l'anteprima nel browser.

Si controlla che:
- il titolo non sia tagliato;
- il testo dica il messaggio prima del taglio;
- nel verticale niente sia coperto dall'interfaccia;
- il pulsante sia quello giusto.

Poi si scrive il verbale e si riassume in chat.

---

## Se qualcosa va storto

| Cosa succede | Cosa fare |
|---|---|
| Una scrittura viene rifiutata | **Non ritentare uguale.** Leggere l'errore, capire quale parametro, correggere, ripresentare a Ivan |
| Un'entità nasce sbagliata | Metterla in pausa (già lo è), rinominarla `SCARTO-<data>`, e **chiedere a Ivan di eliminarla a mano**: Claude non può eliminare |
| Il testo di un'inserzione è sbagliato | Creatività nuova e inserzione nuova. Non si corregge una creatività |
| Il video non è ancora pronto | Aspettare e verificare. Non si carica un'inserzione con un file non pronto |
| Il connettore non vede l'account | **Fermarsi.** Preparare i parametri esatti e passarli a Ivan, che li esegue a mano da Gestione inserzioni |
| L'anteprima non si apre subito dopo la creazione | Riprovare una volta usando l'identificativo della creatività invece che dell'inserzione. Se l'errore parla di accesso, il problema è l'account: si segnala |

## Regole vincolanti

1. **Solo da un collaudo VERDE e con il sì esplicito di Ivan.** Un "procedi" su un piano non vale come sì sulle singole scritture.
2. **Tutto in pausa.** L'attivazione è una decisione separata, in un momento separato.
3. **Una scrittura alla volta, e una rilettura dopo ognuna.** Non si dice che una cosa è stata fatta senza averla riletta.
4. **Nomi di creazione e nomi di modifica sono diversi.** Vedi `parametri.md`.
5. **I budget sono in centesimi**, e si rileggono prima e dopo.
6. **Il numero della pagina sta dentro ogni creatività e dentro il gruppo.**
7. **Mai identificativi di interessi inventati.** Solo geografia.
8. **Mai eliminare**: non si può. Si mette in pausa, si rinomina, si segnala.
9. **I testi si copiano dal pacchetto**, non si riscrivono al momento. Se un testo non convince, torna al collaudo.
10. **Non si modifica `meta-scrittura-sicura`.** Si richiama.
11. **Se il connettore risponde a un account inatteso, ci si ferma.**

## Cosa serve per attivare — non lo fa questa skill

L'attivazione è un'altra decisione, e va presa con davanti:
- il collaudo verde e le anteprime viste;
- la conferma che **qualcuno risponde** ai contatti, e in quali fasce (§11): una campagna che produce chat senza risposta brucia contatti pagati;
- il tetto di spesa impostato **dentro Meta**, non solo sulla carta (§9);
- il conto delle campagne attive: al massimo due.

## Dove si scrive

```
montaggi/
  rivenditori/
    B1-lunedi-mattina-2026-09-25.md
```

Da Cowork si scrive direttamente; dalla chat si consegna il file. File di appoggio, rilettura, copia sul file buono.

## Cosa fa dopo, e chi

Con tutto in pausa e le anteprime viste, la decisione di attivare è di Ivan. Da lì in poi lavorano il **semaforo mattutino** e la **lettura dei numeri**, che riportano l'esito del blocco nella coda degli angoli.

Va segnalato subito in chat: un account inatteso; una scrittura rifiutata due volte per lo stesso motivo; un'entità di scarto da eliminare a mano; un'anteprima in cui il messaggio sparisce in una posizione.
