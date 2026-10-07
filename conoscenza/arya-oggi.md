# Arya oggi — la scheda

**Unica fonte per descrivere Arya** (vedi CLAUDE.md). Prima stesura: 7/10/2026. Aggiornata con le risposte di Ivan del 7/10/2026.
Ricavata da `.agents/product-marketing.md` v1.3 (14/09/2026, letto su OneDrive, resta solo lì), da
`conoscenza/glossario.md` e da `archivio-lml-adv/regole-adv.md` v2.5 (17/09/2026).

## La regola (decisione 8)
- Lo stato di ogni funzione lo decidono **Roberto e Fabio** (LML); **Ivan approva**.
- **Vendibile** solo se funziona **oggi** per un cliente vero o in una demo che si ripete uguale, **e Roberto lo conferma per iscritto**.
- Finché non c'è la conferma: **nessuna funzione è vendibile e niente va negli annunci.**
- Le conferme si raccolgono in OneDrive `Company/Marketing/macchina-adv/novita-arya/VERIFICA-FUNZIONI.md`
  (colonna "conferma Roberto"). Quando una riga è confermata, qui si aggiorna lo stato, con data e fonte.

**Stati:** **vendibile** (confermata da Roberto, approvata da Ivan) · **da confermare** (c'è una prova possibile, manca la conferma) ·
**in arrivo** (non c'è ancora) · **non si promette** (c'è un limite noto).
**Al 7/10/2026 sono vendibili 8 funzioni** (conferma di Roberto e approvazione di Ivan del 7/10/2026, in
`VERIFICA-FUNZIONI.md`; registro in `osservatorio/2026-10-07-verifica-funzioni.md`). Le altre 8 "confermate" ma senza
una prova scritta restano **da confermare: manca la prova** finché non si indica il cliente o la demo che la mostra.

**Prove disponibili da far verificare** (nomi dei clienti mai negli annunci, decisione 2):
- **Mr. Toner** — cliente vero, WhatsApp.
- **Timeo & Dimarco** — cliente vero, telefono, **dal 30 ottobre 2026**.
- **Tenant dimostrativo Ecoross** — demo ripetibile: voce, chat, appuntamenti su Google Calendar.

## 1. Cosa fa, per canale

### Telefono — ARYA Voice ("l'assistente telefonico")
| Funzione | Cosa fa | Stato | Prova possibile |
|---|---|---|---|
| Risponde al telefono | Capisce la richiesta in italiano parlato e risponde | **vendibile** (7/10/2026) | Ecoross (demo voce); Timeo & Dimarco dal 30/10 |
| Fissa appuntamenti | Prende l'appuntamento e lo scrive in agenda (Google Calendar) | **vendibile** (7/10/2026) | Ecoross (appuntamenti su Google Calendar); Timeo & Dimarco dal 30/10 |
| Prende ordini d'asporto | Prende l'ordine al telefono | da confermare: manca la prova | nessuna prova indicata (integrazione con un gestionale per ristoranti citata a settembre) |
| Riconosce chi richiama | Riconosce chi ha già chiamato | da confermare: manca la prova | nessuna prova indicata |
| Passa a una persona | Passa la chiamata a una persona solo quando serve | da confermare: manca la prova | nessuna prova indicata |
| Risposta in meno di un secondo | "al massimo 700 millisecondi" | non si promette | Va misurata in produzione come metrica fissa; "il giorno che sale a due secondi, il claim si toglie" |

### Chat e WhatsApp — Arya Customer Care (nome "ARYA Care" non definitivo)
| Funzione | Cosa fa | Stato | Prova possibile |
|---|---|---|---|
| Risponde su WhatsApp | Risponde ai clienti, anche a negozio chiuso | **vendibile** (7/10/2026) | Mr. Toner |
| Risponde in chat sul sito | Stesso "cervello" del modulo voce | **vendibile** (7/10/2026) | Ecoross (demo chat) |
| Risponde su Telegram | — | da confermare: manca la prova | nessuna prova indicata |
| Assistenza tecnica sul numero del negozio | Risponde alle domande di assistenza | **vendibile** (7/10/2026) | Mr. Toner |
| Primo contatto ai nuovi contatti e appuntamento | Un secondo numero scrive per primo a chi arriva dalle campagne e fissa un appuntamento telefonico | **vendibile** (7/10/2026) | Mr. Toner |
| Ricontatto e promozioni | Ricontatta i clienti dopo N giorni e invia promozioni (su WhatsApp serve un template approvato) | **vendibile** (7/10/2026) | Mr. Toner |
| Fissa appuntamenti in chat | Appuntamento scritto in Google Calendar | **vendibile** (7/10/2026) | Ecoross |
| Agisce nei programmi del cliente | Con i collegamenti mette l'ordine, fissa l'appuntamento, controlla la spedizione ("rispondiamo e facciamo") | da confermare: manca la prova | Ecoross per l'agenda; serve un caso con gestionale |
| Voce e immagini in chat | Da fascia Pro in su | da confermare: manca la prova | nessuna prova indicata |
| Passaggio a operatore | Passa la conversazione a una persona con tutto il contesto | da confermare: manca la prova | nessuna prova indicata |
| Stesso numero su WhatsApp Business e Arya (coesistenza) | Tiene numero e storico chat (180 giorni) | in arrivo | Richiede l'accreditamento Tech Provider Meta (esito da verificare) |
| Collegamento del numero da soli (Embedded Signup) | Il cliente collega il suo numero dal pannello | in arrivo | — |

Nota: WhatsApp per i nuovi clienti parte solo dopo la verifica dell'azienda su Meta (al 14/09/2026: non ancora ottenuta).

### Email — a-Mail ("la casella che si svuota da sola")
| Funzione | Cosa fa | Stato | Prova possibile |
|---|---|---|---|
| Legge, smista, risponde e inoltra le email | Con agenti AI; si paga per email elaborata, non per casella (fasce Start / Crescita / Impresa) | da confermare: manca la prova | nessuna prova indicata |

### Prezzi e offerta (decisione 3)
- Customer care: fasce Base / Pro / Scale a 98 / 189 / 290 €/mese, più quota per conversazione risolta.
- **Listino:** contratto 24 mesi con recesso libero a 60 giorni di preavviso; attivazione a pagamento, fino a 3 rate.
- **Offerta di lancio, solo per i primi 10 clienti Arya:** prova gratuita di 15 giorni prima della firma e attivazione inclusa;
  contratto sempre 24 mesi con recesso a 60 giorni. Si rivede al controllo di fine dicembre 2026.
  Prevale su "nessuna prova gratuita", scritto a settembre in `product-marketing.md`.

## 2. Cosa Arya NON fa (o non si può dire)
- Non dice "intelligenza artificiale" negli annunci: è una scelta (le prove dicono che abbassa la fiducia). Nella chat invece
  **deve** dire al primo contatto che risponde una macchina (Regolamento UE 2024/1689, art. 50).
- Non ha capacità che non ha: mai attribuirle funzioni che non sono in questa scheda (EU AI Act).
- Non promette la risposta in 700 ms finché non è misurata in produzione.
- Non promette la coesistenza del numero WhatsApp finché Meta non accredita LML come Tech Provider.
- Non lavora senza un flusso di richieste in entrata: senza clienti che scrivono o chiamano "non ha niente da fare".
- Non vende pacchetti di conversazioni (le vecchie fasce a conversazioni incluse sono superate).
- Non usa come propri i numeri di mercato (70-80% risolte senza persona, gradimento 4,1/5…): sono dei fornitori.
- Non ha ancora testimonianze registrate né numeri di un cliente da mostrare.
- Non fa riconciliazione bancaria (modulo in sviluppo con un partner, **non in vendita**).
- "Chiamate perse" non è più un messaggio solo nostro (lo usa un concorrente): serve il pezzo in più, "e fa".
- Nomi dei clienti mai negli annunci (decisione 2).

## 3. Ancora da chiarire
1. Per le 8 funzioni "da confermare: manca la prova": quale cliente o quale demo ripetibile le mostra?
2. a-Mail: c'è una prova (cliente o demo)?
3. Esito di Tech Provider e verifica dell'azienda su Meta.
4. Il nome definitivo del modulo customer care.

## Registro delle modifiche
| Data | Cosa | Fonte | Sì di Ivan |
|---|---|---|---|
| 7/10/2026 | Prima stesura | product-marketing.md v1.3, glossario.md, regole-adv.md v2.5 | — |
| 7/10/2026 | Regola della vendibilità, prove disponibili, listino e offerta di lancio | risposte di Ivan del 7/10/2026 | sì (risposte 7/10/2026) |
| 7/10/2026 | 8 funzioni passano a vendibile (righe 1, 2, 7, 8, 10, 11, 12, 13 di VERIFICA-FUNZIONI.md) | conferma di Roberto, VERIFICA-FUNZIONI.md | sì, Ivan Arpino 07.10.2026 |
