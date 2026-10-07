# Arya oggi — la scheda

**Unica fonte per descrivere Arya** (vedi CLAUDE.md). Prima stesura: 7/10/2026.
Ricavata da `.agents/product-marketing.md` v1.3 (14/09/2026, letto su OneDrive), con l'aiuto di
`conoscenza/glossario.md` e `archivio-lml-adv/regole-adv.md` v2.5 (17/09/2026).
`product-marketing.md` non è stato copiato nel repository: contiene nomi di persone esterne (vedi README).

**Stati:** **vendibile** = si può promettere negli annunci · **in prova** = esiste ma senza prove sufficienti, non si promette ·
**in arrivo** = non c'è ancora · **da verificare con Ivan** = non è certo, non si promette finché Ivan non conferma.
Negli annunci entrano solo le righe **vendibili**. Al 7/10/2026 **nessuna riga è "vendibile" senza riserve**: tutte
aspettano la conferma di Ivan (prima domanda aperta del README).

## 1. Cosa fa, per canale

### Telefono — ARYA Voice ("l'assistente telefonico")
| Funzione | Cosa fa | Stato | Prova |
|---|---|---|---|
| Risponde al telefono | Capisce la richiesta in italiano parlato e risponde | da verificare con Ivan (probabile vendibile) | Nessun cliente voce indicato in produzione nei file; demo "con la voce vera" disponibile |
| Ordini e appuntamenti | Prende ordini d'asporto e appuntamenti | da verificare con Ivan | Integrazione con un gestionale per ristoranti (canale partner); studi odontoiatrici: "demo in corso" |
| Riconosce chi richiama | Riconosce chi ha già chiamato | da verificare con Ivan | nessuna prova nei file |
| Passa a una persona | Passa la chiamata a una persona solo quando serve | da verificare con Ivan | nessuna prova nei file |
| Risposta in meno di un secondo | "al massimo 700 millisecondi" | in prova — **non si promette** | Non misurato in produzione: il file chiede di strumentarlo come metrica fissa; "il giorno che sale a due secondi, il claim si toglie" |

### Chat e WhatsApp — Arya Customer Care (nome "ARYA Care" non definitivo)
| Funzione | Cosa fa | Stato | Prova |
|---|---|---|---|
| Risponde su WhatsApp, chat del sito, Telegram | Stesso "cervello" del modulo voce; qualsiasi e-commerce | vendibile per il caso in produzione; da verificare con Ivan per la formulazione | Primo cliente in produzione: rivenditore di consumabili in Puglia (~10 persone), contratto 24 mesi. **Numeri del cliente: non ancora raccolti** |
| Assistenza tecnica sul numero del negozio | Risponde alle domande di assistenza anche a negozio chiuso | vendibile (stesso caso) — da verificare con Ivan | come sopra |
| Primo contatto ai nuovi contatti e appuntamento | Un secondo numero contatta per primo chi arriva dalle campagne e fissa un appuntamento telefonico | vendibile (stesso caso) — da verificare con Ivan | come sopra |
| Ricontatto e promozioni | Ricontatta i clienti dopo N giorni e invia promozioni (su WhatsApp serve un template approvato) | da verificare con Ivan | come sopra |
| Agisce nei programmi del cliente | Con i collegamenti (connettori) mette l'ordine, fissa l'appuntamento, controlla la spedizione: "rispondiamo e facciamo" | da verificare con Ivan | È il differenziatore n. 1 nei file; serve un caso reale da citare. Collegamenti inclusi: 0 Base, 2 Pro, 5+ Scale |
| Voce e immagini in chat | Disponibili da fascia Pro in su | da verificare con Ivan | nessuna prova nei file |
| Passaggio a operatore | Passa la conversazione a una persona con tutto il contesto | da verificare con Ivan | nessuna prova nei file |
| Stesso numero su WhatsApp Business e Arya (coesistenza) | Tiene il numero e lo storico chat (180 giorni) | **in arrivo** — non si promette | Richiede l'accreditamento Tech Provider Meta (chiesto a settembre 2026, esito da verificare) |
| Collegamento del numero da soli dal pannello (Embedded Signup) | Il cliente collega il suo numero WhatsApp senza passare da LML | in arrivo — da verificare con Ivan | — |

Nota: WhatsApp per i clienti parte solo dopo la verifica dell'azienda su Meta (al 14/09/2026: non ancora ottenuta).

### Email — a-Mail ("la casella che si svuota da sola")
| Funzione | Cosa fa | Stato | Prova |
|---|---|---|---|
| Legge, smista, risponde e inoltra le email | Con agenti AI; si paga per email elaborata, non per casella (fasce Start / Crescita / Impresa) | da verificare con Ivan | `product-marketing.md` non dà funzioni, stato, clienti o numeri. Nessuna prova nei file |

### Prezzi e offerta (da leggere insieme a `regole/decisioni.md`)
- Customer care: fasce Base / Pro / Scale a 98 / 189 / 290 €/mese, più una tantum di attivazione e quota per conversazione risolta.
- **Offerta di lancio in vigore: decisione 3** (prova di 15 giorni e attivazione inclusa per i primi clienti). Prevale su
  "nessuna prova gratuita" e sull'una tantum "volutamente alta" scritti a settembre in `product-marketing.md` e `glossario.md`.
- Contratti a 24 mesi (settembre 2026): **da verificare con Ivan** se valgono anche con l'offerta di lancio.

## 2. Cosa Arya NON fa (o non si può dire)
- Non dice "intelligenza artificiale" negli annunci: è una scelta (le prove dicono che abbassa la fiducia). Nella chat invece
  **deve** dire al primo contatto che risponde una macchina (Regolamento UE 2024/1689, art. 50).
- Non ha capacità che non ha: mai attribuirle funzioni non in questa scheda (EU AI Act).
- Non promette la risposta in 700 ms finché non è misurata in produzione.
- Non promette la coesistenza del numero WhatsApp finché Meta non accredita LML come Tech Provider.
- Non lavora senza un flusso di richieste in entrata: senza clienti che scrivono o chiamano "non ha niente da fare".
- Non vende pacchetti di conversazioni (le vecchie fasce a conversazioni incluse sono superate).
- Non usa come propri i numeri di mercato (70-80% risolte senza persona, gradimento 4,1/5…): sono dei fornitori.
  Le stime sul costo del problema sono di mercato, non dei clienti LML.
- Non ha ancora testimonianze registrate né numeri di un cliente da mostrare.
- Non fa riconciliazione bancaria (modulo in sviluppo con un partner, **non in vendita**).
- "Chiamate perse" non è più un messaggio solo nostro (lo usa un concorrente): serve il pezzo in più, "e fa".
- Nomi dei clienti mai negli annunci (decisione 2).

## 3. Da verificare con Ivan (riassunto)
1. Quali righe passano a "vendibile" oggi, e con quale prova.
2. ARYA Voice: c'è almeno un cliente voce in produzione? Le funzioni ordini/appuntamenti/riconoscimento sono attive?
3. a-Mail: funzioni attive, clienti, numeri.
4. Esito di Tech Provider e verifica dell'azienda su Meta.
5. Il nome definitivo del modulo customer care.
6. Contratti a 24 mesi e una tantum: come convivono con l'offerta di lancio.

## Registro delle modifiche
| Data | Cosa | Fonte | Sì di Ivan |
|---|---|---|---|
| 7/10/2026 | Prima stesura | product-marketing.md v1.3, glossario.md, regole-adv.md v2.5 | in attesa (richiesta di unione) |
