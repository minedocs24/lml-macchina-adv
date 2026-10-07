# Modello — Verbale di montaggio

File: `montaggi/<settore>/<blocco>-<AAAA-MM-GG>.md`. Uno per montaggio, mai sovrascritto.

---

# Montaggio — [settore] · [B n - angolo] · [data]

**Stato finale: TUTTO IN PAUSA** · Spesa a oggi: 0 €

| | |
|---|---|
| Pacchetto | inserzioni/[settore]/[blocco].md |
| Collaudo | collaudi/[settore]/[blocco]-[data].md — **VERDE** il [ ] |
| Sì di Ivan | il [ ], testuale: "[ ]" |
| Account usato | [numero] — [nome] — valuta [ ] |
| Campagne attive in tutto dopo questo montaggio | [ ] su 2 |

**Fonti lette:** regole-adv.md v[ ] del [ ] · parametri.md verificato il [ ]

## 0. Fondamenta

| Controllo | Esito |
|---|---|
| Account visti dal connettore | [elenco] |
| Account atteso presente | sì / **no → fermato** |
| Minimo di budget dell'account | [ ] centesimi/giorno |
| Numero della pagina LML | [ ] |
| Metodo di pagamento presente | |

## 1. Le scritture

Una riga per scrittura, in ordine. **Ogni riga ha la sua rilettura.**

### S1 — Campagna

**Parametri inviati:**
```
campaign_name: "..."
objective: ...
buying_type: AUCTION
campaign_daily_budget: 1000      ← 10,00 €
special_ad_categories: []
```
**Presentati a Ivan il:** [ ] · **Sì ricevuto:** [ ]
**Numero restituito:** [ ]
**Obiettivi di ottimizzazione validi restituiti:** [elenco] · **consigliato:** [ ]

**Rilettura:**
| Controllo | Atteso | Trovato | Esito |
|---|---|---|---|
| Nome | | | |
| Stato | PAUSED | | |
| Budget giornaliero | 1000 cent = 10 € | | |

### S2 — Gruppo

**Parametri inviati:**
```
ad_set_name: "..."
campaign_id: ...
optimization_goal: CONVERSATIONS
destination_type: WHATSAPP
promoted_object: {"page_id":"..."}
billing_event: IMPRESSIONS
targeting: {"geo_locations":{"countries":["IT"]}}
dsa_beneficiary: LML Technologies S.r.l.
dsa_payor: LML Technologies S.r.l.
```
**Sì ricevuto:** [ ] · **Numero restituito:** [ ]

**Rilettura:**
| Controllo | Atteso | Trovato | Esito |
|---|---|---|---|
| Nome | | | |
| Stato | PAUSED | | |
| Destinazione | WHATSAPP | | |
| Pubblico | solo Italia, nessun interesse | | |
| Budget sul gruppo | nessuno | | |
| Dichiarazione europea | LML Technologies S.r.l. | | |

### S3 — File caricati

| File | Tipo | Identificativo / numero | Stato |
|---|---|---|---|
| | immagine | | |
| | video | | pronto / **in lavorazione** |

**Copertina del video:** scelta / ricavata dal primo fotogramma — **controllata:** [ ]

### S4…Sn — Creatività e inserzioni

Per ciascuna:

**[C n] — nome inserzione:** `B[n]-[angolo]-C[n]-[formato]-[gancio]`
- Numero della pagina dentro la creatività: [ ]
- File usato: [ ]
- Testo principale: **copiato dal pacchetto** sì/no
- Titolo: **copiato dal pacchetto** sì/no
- Pulsante: Invia messaggio
- Messaggio di apertura: "[ ]" — contiene il blocco: [ ]
- **Numero restituito:** [ ]

**Rilettura:** nome [ ] · stato PAUSED [ ] · creatività collegata [ ]

## 2. Le anteprime

| Inserzione | Posizione | Indirizzo | Titolo intero? | Messaggio prima del taglio? | Niente coperto? |
|---|---|---|---|---|---|
| C1 | feed mobile | | | | |
| C1 | storie | | | | |
| C1 | Reels | | | | |

**Indirizzi da aprire, da incollare nella risposta a Ivan:**
- …

## 3. Errori e scarti

| Cosa | Errore | Cosa ho fatto |
|---|---|---|

**Entità di scarto da eliminare a mano da Ivan** (Claude non può eliminare):
| Nome | Numero | Perché |
|---|---|---|

## 4. Cosa serve per attivare

- [ ] Anteprime viste da Ivan
- [ ] Chi risponde ai contatti, e in quali fasce
- [ ] Tetto di spesa impostato **dentro Meta**
- [ ] Campagne attive: al massimo due
- [ ] Sì esplicito di Ivan **all'attivazione** (decisione separata da questo montaggio)

## 5. Da segnalare a Ivan

- …
