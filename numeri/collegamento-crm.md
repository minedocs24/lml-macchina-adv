# Collegamento con il CRM LML — come i Numeri leggono i contatti

> **Superato il 10/10/2026** dalla decisione 21: la guida al CRM ora è `conoscenza/crm-statistiche.md` (connettore
> «LML CRM · Statistiche», sola lettura). Questo file resta come storia: è stato scritto senza il connettore.

Versione del 7/10/2026. Il CRM LML è **l'unico posto dei contatti** (CLAUDE.md): richieste, trattative, clienti.
L'Excel di settembre (`Archivio-contatti-LML.xlsx`) va in pensione.
**Solo lettura.** La macchina non scrive niente nel CRM: niente creazioni, modifiche, cambi di fase, note, offerte, invii.
Questo file è stato scritto guardando **la descrizione** degli strumenti dei connettori, **senza chiamarli**: nessun dato del CRM è stato letto.

## Da dove si legge
| Cosa | Connettore | Strumenti (solo lettura) | Cosa dà |
|---|---|---|---|
| Richieste di contatto | `lml-commerciale` | `elenco_richieste`, `scheda_richiesta` | richieste con canale, stato, assegnataria, termine, consensi, conteggi |
| Trattative (demo, offerte, chiusure) | `lml-commerciale` | `elenco_trattative`, `scheda_trattativa`, `cronologia`, `elenco_offerte` | fase, valore, chiusura prevista, prossimo passo, attività, offerte firmate |
| Numeri commerciali | `lml-commerciale` | `i_miei_numeri` (vista "tutti") | vinto, tasso di vittoria, pipeline, nuove trattative, perse, mese per mese |
| Clienti e canoni | `LML Piattaforma Clienti` | `elenco_canoni`, `panoramica_clienti` | canoni attivi, da attivare, in disdetta, a rischio; importi |

## Cosa ne ricavano i Numeri ogni settimana
Solo **conteggi e somme**, mai nomi, telefoni o email (decisione 9). Negli archivi si scrivono al massimo gli ID.

| Numero | Come si conta | Strumento |
|---|---|---|
| Contatti nuovi | richieste create nella settimana, per canale e per inserzione di provenienza | `elenco_richieste` (stato "tutte") |
| Contatti validi | richieste in stato "qualificata" o "convertita" | `elenco_richieste` |
| Scartati / spam | richieste "scartata" e "spam" | `elenco_richieste` |
| Tempo di prima risposta | dalla creazione della richiesta al primo contatto | `scheda_richiesta` / `cronologia` — **oggi non garantito, vedi sotto** |
| Demo | trattative entrate nella fase "demo" (o con un'attività "demo") nella settimana | `elenco_trattative`, `cronologia` |
| Clienti nuovi | trattative vinte / offerte firmate nella settimana | `elenco_trattative` (stato "vinte"), `elenco_offerte` ("firmata") |
| Canoni mensili | somma dei canoni attivi dei clienti Arya | `elenco_canoni` (stato "attivi") |
| Costo per cliente | spesa pubblicitaria (Meta e Google) ÷ clienti nuovi attribuiti alle inserzioni | spesa da Meta/Google + CRM |

Una riga a settimana va in `numeri/storico.csv` (spesa, contatti, demo, clienti, costo per cliente, canoni).

## Cosa manca oggi per farlo
Dalla descrizione degli strumenti risulta che:
1. **Il canale non distingue la pubblicità.** I canali previsti sono SITO, WEBINAR, ARYA_CARE, PARTNER, SEGNALATORE, MANUALE, IMPORT:
   non c'è **Meta**, **Google**, né "pagina Arya" (numero, chat di prova, fatti richiamare) o "modulo Meta".
2. **Non c'è l'inserzione di provenienza.** Nessun campo per campagna, gruppo, inserzione (ID di Meta o di Google) o parametri del link.
   Senza questo non si può dire quale idea o quale pezzo ha portato il contatto: è il pezzo che serve al Piano e alla Regia.
3. **Non è chiaro dove sta la "demo".** Le richieste hanno gli stati nuova / in lavorazione / qualificata / convertita / scartata / spam;
   le trattative hanno fasi e pipeline, ma dalla descrizione non risulta una fase o un'attività "demo" fissa.
4. **Il tempo di prima risposta** non è un campo: va ricostruito dalla cronologia, se il primo contatto di ARYA viene registrato.
5. **Il collegamento richiesta → trattativa → cliente → canone** passa da due connettori diversi (`lml-commerciale` e Piattaforma Clienti):
   serve una chiave comune per contare quanti canoni nascono dalla pubblicità.
6. **Il ritorno dei contatti buoni a Meta** (conversioni di qualità) richiede che il CRM conservi l'identificativo del contatto di Meta.
   Si fa solo con il sì di Ivan.

## Cosa chiedere ai tecnici
1. Aggiungere ai canali delle richieste: **META_MODULO**, **PAGINA_ARYA_TELEFONO**, **PAGINA_ARYA_CHAT**, **PAGINA_ARYA_RICHIAMATA**,
   **GOOGLE** (o un campo "sorgente pubblicitaria").
2. Aggiungere alla richiesta i campi di provenienza: **piattaforma, campagna, gruppo, inserzione (ID)**, e i parametri del link (utm_source,
   utm_campaign, utm_content) per chi arriva dalla pagina Arya; per il modulo Meta, l'ID del contatto (lead) consegnato da Meta.
3. Registrare in cronologia il **primo contatto di ARYA** con data e ora, così il tempo di prima risposta si calcola da solo.
4. Una **fase "demo fissata"** (e "demo fatta") nella pipeline Arya, uguale per tutti i commerciali.
5. Una **chiave comune** fra la trattativa vinta nel CRM e il canone nella Piattaforma Clienti, con il prodotto (Voice, Customer Care, a-Mail).
6. Che il connettore permetta di **filtrare per data di creazione** (oggi le richieste si leggono "dalle più recenti", 20 per pagina).
7. Un accesso di sola lettura per le automazioni dei Numeri, che non possa scrivere.

## Cosa non so
- Come sono impostate oggi le fasi delle pipeline e se esiste già una fase "demo": va verificato con una lettura di prova, con il sì di Ivan.
- Se le richieste che arrivano da ARYA Care portano già con sé qualche dato di provenienza.
- Se il connettore `lml-commerciale` usato dalle automazioni vedrà tutte le richieste o solo quelle della persona collegata
  ("visibili alla persona"): per i conteggi serve la vista di tutti.
