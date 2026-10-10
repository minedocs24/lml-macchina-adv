# L'offerta di Arya — specchio del listino e delle promozioni del CRM

**Questo file non si scrive a mano** (decisione 22). È lo specchio di `elenco_promozioni` del connettore
«LML CRM · Statistiche» (`conoscenza/crm-statistiche.md`) e lo aggiorna **l'Osservatorio ogni lunedì**.
Se il CRM e questo file non dicono la stessa cosa, **vale il CRM**: il Collaudo legge `elenco_promozioni` direttamente.

**Ultima lettura:** 2026-10-10 · listino `2026-10` «Listino ottobre 2026», valido dal 2026-10-01.
Importi IVA esclusa. Nel CRM sono in millesimi di euro: qui sono convertiti in euro.
Cosa fa Arya, funzione per funzione: `conoscenza/arya-oggi.md`.
La versione del 7/10/2026 scritta a mano è nella storia dell'archivio (git); le sue regole sono le decisioni 3, 10, 14, 15, 20.

## Promozioni attive e future
| Codice (`promo=`) | Nome | Dal | Al | Prodotti | Prova | Attivazione | Requisiti | Posti | Posti rimasti | Predefinita |
|---|---|---|---|---|---|---|---|---|---|---|
| `LANCIO` | Offerta di lancio | 2026-10-01 | nessuna scadenza nel CRM | tutta la suite | 15 giorni | inclusa | referenza completa | 10 | 10 | sì |

Testo della promozione nel CRM: «Offerta di lancio per i primi 10 clienti: 15 giorni di prova gratuita e attivazione inclusa.»
Link degli annunci che la citano: pagina degli annunci (CLAUDE.md, "Impostazioni") + `?promo=LANCIO` (decisione 23).
Occupano un posto solo le prove in corso e i clienti. Con meno di 3 posti rimasti, i Numeri avvisano Ivan.

## Listino in vigore

### ARYA Voice — telefono
| Voce | Base | Pro | Scale |
|---|---|---|---|
| Messa in servizio (una volta) | 1.900 € | 3.500 € | 5.900 € |
| Canone al mese | 129 € | 249 € | 490 € |
| Chiamata risolta | 0,69 € | 0,55 € | 0,45 € |
| Chiamata passata | 0,35 € | 0 € | 0 € |
| Minuto oltre il quinto | 0,19 € | 0,19 € | 0,19 € |
| Linea aggiuntiva, al mese | 35 € | 29 € | 25 € |
| Numero aggiuntivo, al mese | 5 € | 5 € | 5 € |
| Collegamento standard oltre gli inclusi, al mese | 49 € | 49 € | 49 € |
| Collegamento su misura, sviluppo (una volta) | 900 € | 900 € | 900 € |
| Collegamento su misura, presidio, al mese | 79 € | 79 € | 79 € |
| Durata · recesso | 24 mesi · 60 giorni | 24 mesi · 60 giorni | 24 mesi · 60 giorni |

### ARYA Customer Care — chat e WhatsApp
| Voce | Base | Pro | Scale |
|---|---|---|---|
| Messa in servizio (una volta) | 1.500 € | 2.900 € | 4.900 € |
| Canone al mese | 98 € | 189 € | 290 € |
| Conversazione risolta | 0,30 € | 0,22 € | 0,15 € |
| Conversazione passata | 0,15 € | 0 € | 0 € |
| Conversazione risolta con chiavi AI del cliente | — | — | 0,08 € |
| Connettore oltre gli inclusi, al mese | 49 € | 49 € | 49 € |
| Connettore proprietario, sviluppo (una volta) | 900 € | 900 € | 900 € |
| Connettore proprietario, presidio, al mese | 79 € | 79 € | 79 € |
| Durata · recesso | 24 mesi · 60 giorni | 24 mesi · 60 giorni | 24 mesi · 60 giorni |

### a-Mail — email
| Voce | Start | Crescita | Impresa |
|---|---|---|---|
| Messa in servizio (una volta) | 1.900 € | 3.500 € | 5.900 € |
| Canone al mese | 129 € | 249 € | 490 € |
| Email con esito utile | 0,20 € | 0,15 € | 0,10 € |
| Casella aggiuntiva, al mese | 6 € | 5 € | 4 € |
| Durata · recesso | 24 mesi · 60 giorni | 24 mesi · 60 giorni | 24 mesi · 60 giorni |

### ARYA Food (nel listino del CRM; **non** è fra i prodotti della macchina in CLAUDE.md)
| Voce | Base | Pro | Scale |
|---|---|---|---|
| Messa in servizio | non indicata nel CRM | non indicata nel CRM | non indicata nel CRM |
| Canone al mese | 79 € | 149 € | 249 € |
| Chiamate comprese · chiamata in più | 120 · 0,49 € | 280 · 0,45 € | 500 · 0,42 € |
| Chat WhatsApp, canone al mese | 15 € | 29 € | 49 € |
| Chat comprese · chat in più | 100 · 0,19 € | 200 · 0,17 € | 400 · 0,15 € |
| Comandi del titolare, canone al mese | 9 € | 15 € | 25 € |
| Comandi compresi · comando in più | 50 · 0,20 € | 100 · 0,18 € | 200 · 0,15 € |
| Linea aggiuntiva, al mese | — | 29 € | 25 € |
| Durata · recesso | 24 mesi · 60 giorni | 24 mesi · 60 giorni | 24 mesi · 60 giorni |

Negli annunci ARYA Food **non entra** finché Ivan non lo aggiunge ai prodotti (CLAUDE.md) e `arya-oggi.md` non lo descrive.

## Le condizioni, dalle decisioni di Ivan (non cambiano con il listino)
- **Durata 24 mesi**, con **recesso libero** dando **60 giorni di preavviso** (decisione 3; nel CRM: 24 e 60 per tutte le fasce).
- **Messa in servizio** fino a **3 rate** (decisione 3).
- **Canone bloccato per 24 mesi**: vale solo per il canone, non per i consumi (decisione 20).
- **Offerta di lancio**: primi 10 clienti Arya **in tutto, su tutta la suite** (decisione 15); in cambio la referenza completa
  — logo, caso studio con mezz'ora registrata, referenza telefonica, verifica dei risultati a 90 giorni (decisione 14).
  Si rivede al controllo di fine dicembre 2026 (decisione 3).

Come dirlo: "Per i primi dieci clienti la partenza è inclusa e lo provi quindici giorni prima di firmare." Non dire "gratis per sempre",
non dire "sconto": i prezzi sono questi per tutti.

## Cosa comprende ogni fascia (dai listini PDF del 7/10/2026: **non** è in `elenco_promozioni`)
Non sono prezzi: sono quantità e casi in cui non si paga. Restano qui finché il CRM non li riporta.
- **ARYA Voice:** chiamate in contemporanea comprese 2 / 6 / 12; numeri compresi 1 / 2 / 5; collegamenti a programmi esterni
  compresi — / 2 / 5. Non si pagano: chiamate sotto i 30 secondi, la stessa persona che richiama entro 30 minuti, chiamate mute
  o pubblicitarie, chiamate perse per un nostro guasto. Il numero del cliente resta suo: si imposta una deviazione.
- **Customer Care:** operatori nel pannello illimitati; collegamenti compresi — / 2 / 5. Non si pagano: saluti e messaggi fuori
  tema, il messaggio di benvenuto, la stessa domanda riaperta entro 6 ore.
- **a-Mail:** caselle comprese 10 / 30 / 100; email in errore o con azione rifiutata gratis; newsletter, notifiche e ricevute
  scartate prima e non pagate; oltre 100 caselle si quota a progetto.
- **Consumo** solo quando Arya chiude la richiesta da sola; nessun minimo; tetto di spesa impostato dal cliente nel pannello.

## Cosa non si promette
- Prezzi o promozioni che non sono in `elenco_promozioni` il giorno del collaudo, o scaduti, o con zero posti rimasti
  (decisione 22). Per esempio i **pacchetti prepagati con sconto del 15%** dei PDF: nel CRM non ci sono.
- Risultati economici garantiti, o percentuali di miglioramento senza un caso documentato.
- La prova gratuita oltre i primi 10 clienti, o più lunga di quanto dice la promozione, o dopo la firma.
- Funzioni non "vendibili" in `arya-oggi.md`: risposta in meno di un secondo, stesso numero su WhatsApp Business e Arya,
  collegamento del numero da soli.
- Sulla fascia più bassa ciò che è compreso solo dalle fasce superiori (voce e immagini in chat, riconoscimento del chiamante,
  collegamenti, voce su misura e report direzionale solo Scale).
- Chiamate in uscita automatiche (richiami, promemoria, campagne) e numeri verdi: fuori listino.
- a-Mail: analisi degli allegati e notifiche fuori dal pannello.
- Il prezzo di un collegamento su misura prima della verifica tecnica.
- Un "prezzo di listino" più alto da cui si fa lo sconto: non esiste.

## Listini PDF da aggiornare
I tre PDF in `Company/Commerciale/Prodotti/Suite ARYA/` dicono cose superate dalle decisioni di Ivan (elenco del 7/10/2026:
due colonne listino/lancio, 12 mesi, "nessuna prova gratuita", collegamento 1.200 €, "risponde in meno di un secondo").
I PDF originali non si modificano da qui: li aggiorna chi ne è responsabile.

## Registro delle letture
| Data | Listino | Promozioni | Chi | Cosa è cambiato |
|---|---|---|---|---|
| 2026-10-10 | 2026-10 (dal 2026-10-01) | LANCIO (10 posti, 10 rimasti) | prima lettura, sessione di collegamento al CRM | prima versione specchio; prezzi uguali alla versione a mano del 7/10/2026 |

## Cosa non so
- La data di fine dell'offerta di lancio: nel CRM è vuota; la decisione 3 dice che si rivede a fine dicembre 2026.
- La rateizzazione della messa in servizio e il canone bloccato non sono campi del CRM: valgono le decisioni 3 e 20.
- Se ARYA Food diventerà un prodotto della macchina: lo decide Ivan.
- Se i pacchetti prepagati scontati del 15% restano in vendita: nel CRM non ci sono, quindi negli annunci no.
