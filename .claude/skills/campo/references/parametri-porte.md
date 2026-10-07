# Parametri del connettore Meta — per le due porte

**Letti il 7/10/2026 dalle descrizioni degli strumenti del connettore Meta Ads, senza nessuna chiamata.** I parametri per
WhatsApp di settembre sono in `.claude/skills/archivio/lml-montaggio-campagna/references/parametri.md` (verificati il 13/09/2026).
Se il connettore cambia, questo file si rilegge e si ridata con un file nuovo. **Non fidarsi della memoria.**

## Regole per ogni chiamata
- Account senza il prefisso `act_`: `2214221312473862` (lml-adv). Mai Minedocs.
- `client_conversation_id`: 20 caratteri fra lettere e cifre, generato alla prima chiamata e ripetuto identico.
- `advertiser_request`: le parole di Ivan copiate, non riassunte. Mai dati personali.
- **Modalità bozza**: creare campagna, gruppo e inserzione mette tutto nella bozza di Gestione inserzioni (stato DRAFT).
  Niente è pubblicato finché qualcuno chiama `ads_activate_entity`, che pubblica **attivo**. **Campo non lo chiama mai.**
- Rilettura dopo ogni creazione: `ads_get_ad_entities` con l'ID restituito, chiedendo i campi scritti più
  `effective_status`. Nel verbale si scrive quello che torna, non quello che si è mandato.
- In `ads_update_entity` oggi sono accettati `ARCHIVED` e `DELETED` (definitivo). **Campo non li manda mai.**

## Campagna — `ads_create_campaign`
| Cosa | Parametro | Nota |
|---|---|---|
| Nome | `campaign_name` | formato §8 |
| Obiettivo | `objective` | solo valori nuovi: `OUTCOME_LEADS`, `OUTCOME_TRAFFIC`… (i vecchi sono rifiutati) |
| Acquisto | `buying_type` | `AUCTION` |
| Budget giornaliero | `campaign_daily_budget` | in centesimi, **solo** l'importo giornaliero scritto nel pacchetto approvato |
| Categorie speciali | `special_ad_categories` | `[]` |
| Tetto totale | `campaign_spend_cap` | solo se scritto nel pacchetto approvato; altrimenti lo imposta Ivan |

La risposta contiene `valid_optimization_goals` e `recommended_optimization_goal`: l'ottimizzazione del gruppo si sceglie
**da quella lista**. Budget sulla campagna = niente budget sul gruppo (viene rifiutato).

## Gruppo — `ads_create_ad_set`
Comuni alle due porte: `ad_set_name`, `campaign_id`, `billing_event: IMPRESSIONS`,
`targeting: {"geo_locations":{"countries":["IT"]}}` (nessun interesse; posizioni automatiche),
`dsa_beneficiary` e `dsa_payor`: `LML Technologies S.r.l.`. Non passare `attribution_spec` né budget.

| Porta | Obiettivo campagna | `optimization_goal` (se nella lista) | `destination_type` | `promoted_object` |
|---|---|---|---|---|
| Pagina Arya | `OUTCOME_LEADS` o `OUTCOME_TRAFFIC` (lo dice il piano) | `LANDING_PAGE_VIEWS` / `LINK_CLICKS`; `OFFSITE_CONVERSIONS` solo con il pixel verificato | `WEBSITE` | `{"pixel_id":"…"}` per le conversioni; il pixel parte solo dopo il consenso (§23) |
| Modulo Meta | `OUTCOME_LEADS` | `LEAD_GENERATION` | da leggere al primo montaggio (non scritto nelle descrizioni per il modulo) | `{"page_id":"…"}`; la pagina deve avere accettato i termini dei moduli (`leadgen_tos_accepted`, da `ads_get_ad_account_pages`) |

Il minimo di budget si legge da `ads_get_ad_accounts` (`min_daily_budget_cents`).

## Inserzione — `ads_create_ad`
- `ad_name`, `ad_set_id`, `creative` con **una sola** fonte: `creative_id` esistente, oppure `object_story_spec` con
  **`page_id` sempre** (senza: "Facebook Page is Missing").
- Immagine: `link_data` con `image_hash` (da `ads_get_ad_images`), `link` = indirizzo della pagina Arya, `message`.
- Video: `video_data` **vuole una copertina** (`image_hash` o `image_url`); con `link_description` serve anche
  `call_to_action`.
- Modulo: il modulo si crea in Gestione inserzioni (nel connettore non c'è uno strumento per crearlo). Come si collega
  alla creatività **non è nelle descrizioni lette**: si legge al primo montaggio e si scrive qui con la data.
- Le creatività non si modificano: per cambiare testo o file, creatività nuova e inserzione nuova.

## Anteprime — `ads_get_ad_preview`
Senza l'account. ID dell'inserzione o della creatività. Posizioni: feed mobile, storie, Reels (almeno queste tre).
Restituisce un indirizzo da dare a Ivan.

## Da verificare al primo montaggio vero (e scrivere qui, con la data)
1. `destination_type` e collegamento del modulo per la seconda porta.
2. Il pixel della pagina Arya: esiste, è intestato a LML, parte dopo il consenso (§0.1: "da verificare o da rifare").
3. Come l'indirizzo della pagina porta il nome di campagna e inserzione, perché il contatto entri nel CRM con la sua
   provenienza (§3.1). Se la pagina non lo legge, va in "Cosa non so".
