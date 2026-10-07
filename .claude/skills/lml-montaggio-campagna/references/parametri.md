# I parametri del connettore Meta — letti, non ricordati

**Verificati il 13 settembre 2026** leggendo le descrizioni degli strumenti del connettore. Se il connettore cambia, questo file va riletto e ridatato. **Non fidarsi della memoria: qui i nomi ingannano.**

## Regole che valgono per ogni chiamata

- **Identificativo di conversazione**: ogni chiamata al connettore Meta ne vuole uno, di 20 caratteri fra lettere e cifre. Si genera alla prima chiamata della conversazione e si **ripete identico** su tutte le successive. Non è un numero di account e non contiene dati personali.
- **Richiesta dell'inserzionista**: va riportata **con le parole di Ivan**, copiate, non riassunte e non tradotte in gergo tecnico.
- L'account si scrive **senza il prefisso `act_`**.
- Gli strumenti di creazione sono di un partner esterno: richiedono che l'utente abbia dato il consenso all'uso del connettore.

## Creare la campagna

Obbligatori: account, nome, obiettivo, tipo di acquisto.

| Cosa | Parametro | Valore per noi |
|---|---|---|
| Nome | `campaign_name` | `ARYA - Call fissate - <Settore> - <mese anno>` |
| Obiettivo | `objective` | **solo valori nuovi**: `OUTCOME_AWARENESS`, `OUTCOME_TRAFFIC`, `OUTCOME_ENGAGEMENT`, `OUTCOME_LEADS`, `OUTCOME_SALES`, `OUTCOME_APP_PROMOTION`. I vecchi (`LINK_CLICKS`, `CONVERSATIONS`, `REACH`…) vengono **rifiutati** |
| Tipo di acquisto | `buying_type` | `AUCTION` |
| Budget giornaliero | `campaign_daily_budget` | **`1000`** = 10 € |
| Categorie speciali | `special_ad_categories` | `[]` |

**Quale obiettivo per WhatsApp.** Le conversazioni sono ammesse sotto più obiettivi. Per una campagna che deve produrre conversazioni da cui nascono call, i candidati sono `OUTCOME_ENGAGEMENT` e `OUTCOME_LEADS`. **Non si sceglie a memoria:** la risposta alla creazione della campagna contiene `valid_optimization_goals` e `recommended_optimization_goal`. Si legge quella lista e si usa un valore da lì. Un valore non valido **viene sostituito d'ufficio** dal server con quello predefinito, e il gruppo finisce ottimizzato per una cosa che non abbiamo scelto.

**Budget sulla campagna o sul gruppo.** Mettendo `campaign_daily_budget` il budget sta sulla campagna, ed è quello che Meta consiglia. In quel caso **non si può** passare un budget al gruppo: viene rifiutato. Con un gruppo solo la differenza è nulla, e tenere il budget sulla campagna rende più semplice controllare il tetto di 10 € al giorno.

## Creare il gruppo

Obbligatori: account, nome, campagna, addebito, obiettivo di ottimizzazione, pubblico.

| Cosa | Parametro | Valore per noi |
|---|---|---|
| Nome | `ad_set_name` | `<Settore> - Italia - Largo - B<n>-<angolo>` |
| Campagna | `campaign_id` | dal passo prima |
| Ottimizzazione | `optimization_goal` | `CONVERSATIONS` — **se è nella lista restituita dalla campagna** |
| Destinazione | `destination_type` | **`WHATSAPP`** — obbligatorio con le conversazioni |
| Oggetto promosso | `promoted_object` | `{"page_id":"<numero della pagina>"}` — **obbligatorio** con WhatsApp. Se manca, Meta lo indovina dall'account: non lasciarglielo indovinare |
| Addebito | `billing_event` | `IMPRESSIONS` |
| Pubblico | `targeting` | `{"geo_locations":{"countries":["IT"]}}` |
| Beneficiario | `dsa_beneficiary` | `LML Technologies S.r.l.` |
| Pagante | `dsa_payor` | `LML Technologies S.r.l.` |
| Budget | — | **niente**: sta sulla campagna |
| Attribuzione | `attribution_spec` | **non passare**: il valore predefinito va bene |

**Cose da sapere:**
- **L'allargamento del pubblico è acceso di default** sui gruppi nuovi. Con quello acceso, età minima e massima diventano suggerimenti, non limiti. Per noi va bene: vogliamo il pubblico largo. Se servisse un limite vero di età, si disattiva esplicitamente.
- **Mai inventare identificativi di interessi.** Sono numeri veri, lunghi. Se non li abbiamo, si usa solo la geografia. Numeri finti vengono rifiutati.
- **Con l'Italia la dichiarazione europea è obbligatoria.** Omettendola, Meta la riempie con il nome del business: potrebbe non essere quello giusto.
- Il **minimo di budget per valuta** si legge dall'account prima di impostare. Per l'euro risultava 87 centesimi al giorno.

## Caricare i file

Uno strumento solo per immagini e video, da file locale o da indirizzo pubblico.

- Da file locale: si apre un'interfaccia in cui Ivan sceglie il file.
- Da indirizzo: serve un collegamento **diretto e pubblico**. Non funzionano i collegamenti condivisi di Drive, Dropbox o Canva che chiedono l'accesso.
- Le immagini restituiscono un identificativo da usare nella creatività.
- **I video hanno una lavorazione asincrona.** Finché lo stato non è "pronto" non si possono usare. Si verifica, non si tira a indovinare.

## Creare l'inserzione

Obbligatori: account, nome, gruppo, e la creatività.

La creatività va scritta dentro il parametro `creative`, e deve contenere **una sola** fonte:
- un identificativo di creatività già esistente, **oppure**
- un post già pubblicato, **oppure**
- la creatività scritta lì per lì.

In quest'ultimo caso **serve sempre il numero della pagina**: se manca, l'inserzione viene rifiutata con l'errore "Pagina Facebook mancante". È l'errore più comune.

Per le immagini si preferisce l'**identificativo dell'immagine** all'indirizzo: è il campo canonico. Per i video, se non si passa una copertina, Meta la ricava dal primo fotogramma — **da controllare**, perché il primo fotogramma è il gancio.

**Le creatività non si modificano mai.** Per cambiare testo, titolo, immagine o pulsante: creatività nuova, inserzione nuova.

## Modificare qualcosa

Qui i nomi cambiano, ed è la trappola principale.

| Cosa | Quando si crea | Quando si modifica |
|---|---|---|
| Nome campagna | `campaign_name` | **`name`** |
| Nome gruppo | `ad_set_name` | **`name`** |
| Nome inserzione | `ad_name` | **`name`** |
| Budget giornaliero | `campaign_daily_budget` | **`daily_budget`** |
| Tetto di spesa | `campaign_spend_cap` | **`spend_cap`** |
| Inizio e fine | `campaign_start_time` / `campaign_stop_time` | **`start_time`** / **`stop_time`** |

Passare un nome di creazione a una modifica viene **rifiutato**. Non si può nemmeno spostare un'entità sotto un altro genitore.

## Le anteprime

- Lo strumento delle anteprime **non vuole l'account**: passarlo lo fa fallire.
- Si passa l'identificativo dell'inserzione **oppure** quello della creatività.
- Posizioni: feed mobile, feed desktop, Instagram, storie Instagram, Reels Instagram, colonna destra, Messenger, Threads.
- Restituisce un **indirizzo** che va messo nella risposta a Ivan, testuale: è il modo in cui lui la apre.
- Se l'inserzione è appena stata creata e l'anteprima fallisce, si riprova **una volta** con l'identificativo della creatività. Se l'errore parla di accesso all'account, riprovare è inutile: si segnala.

## Lo storico delle modifiche

Esiste uno strumento che legge il registro delle modifiche dell'account: chi ha cambiato cosa e quando, comprese le modifiche fatte da Meta. **Si usa per verificare**, dopo un montaggio o quando qualcosa non torna. È in sola lettura.

## Cosa non si può fare

- **Eliminare.** Lo stato "eliminato" viene rifiutato e forzato a "in pausa".
- **Modificare una creatività.**
- **Cambiare l'obiettivo di una campagna** a un valore vecchio.
- **Mettere un budget sul gruppo** se la campagna ne ha già uno.
- **Riparentare** un gruppo o un'inserzione.
