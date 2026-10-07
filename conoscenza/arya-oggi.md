# Arya oggi — la scheda

**Unica fonte per descrivere Arya** (vedi CLAUDE.md). Prima stesura: 7/10/2026. Ultimo aggiornamento: 7/10/2026.
Fonti: `.agents/product-marketing.md` v1.3 (14/09/2026, solo su OneDrive), `conoscenza/glossario.md`, `regole/regole-adv.md` 3.0,
i listini ufficiali in OneDrive `Company/Commerciale/Prodotti/Suite ARYA/` (ARYA Voice settembre 2026, Customer Care AI e a-Mail luglio 2026)
e la verifica delle funzioni `novita-arya/VERIFICA-FUNZIONI.md` (Roberto "confermato" su 19 righe, approvata da Ivan il 7/10/2026).
Prezzi e condizioni: `conoscenza/offerta.md`.

## La regola (decisione 8)
- Lo stato di ogni funzione lo decidono **Roberto e Fabio** (LML); **Ivan approva**.
- **Vendibile** solo se funziona **oggi** per un cliente vero o in una demo che si ripete uguale, **e Roberto lo conferma per iscritto**.
- Negli annunci entrano **solo** le righe "vendibile". Le novità diventano promesse solo dopo il sì di Ivan.
- Le conferme si raccolgono in OneDrive `Company/Marketing/macchina-adv/novita-arya/VERIFICA-FUNZIONI.md`.

**Stati:** **vendibile** · **in arrivo** (non c'è ancora o non è chiaro se funziona oggi) · **non si promette** (limite noto).
**Al 7/10/2026: 16 funzioni vendibili su 19.** Restano fuori la 6, la 17 e la 18 finché Ivan non chiarisce se funzionano già oggi.

**Prove** (nomi dei clienti mai negli annunci, decisione 2): cliente WhatsApp in produzione (Mr. Toner); cliente telefono
dal 30 ottobre 2026 (Timeo & Dimarco); tenant dimostrativo Ecoross (voce, chat, appuntamenti su Google Calendar).

## 1. Cosa fa, per canale
Il numero "#" è la riga di VERIFICA-FUNZIONI.md. La colonna "Fascia" dice da quale fascia del listino la funzione è compresa.

### Telefono — ARYA Voice ("l'assistente telefonico")
| # | Funzione | Fascia | Stato | Prova |
|---|---|---|---|---|
| 1 | Risponde al telefono 24 ore su 24, in italiano parlato naturale | tutte | **vendibile** (7/10/2026) | Ecoross; cliente telefono dal 30/10 |
| 2 | Fissa appuntamenti al telefono e li scrive in Google Calendar | tutte | **vendibile** (7/10/2026) | Ecoross; cliente telefono dal 30/10 |
| 3 | Prende ordini d'asporto e prenotazioni | tutte | **vendibile** (7/10/2026) | conferma di Roberto |
| 4 | Riconosce chi ha già chiamato e ricorda le volte precedenti | da Pro | **vendibile** (7/10/2026) | conferma di Roberto |
| 5 | Passa la chiamata a una persona quando serve, con il riassunto | tutte | **vendibile** (7/10/2026) | conferma di Roberto |
| 6 | Risponde in meno di un secondo (al massimo 700 millisecondi) | — | **non si promette** | da misurare in produzione; resta fuori finché Ivan non chiarisce |

Dal listino, compresi in tutte le fasce: registrazione, trascrizione e ricerca nelle telefonate; il numero del cliente resta suo
(si imposta una deviazione). Da Pro: riepilogo al chiamante via SMS o WhatsApp, proposte in chiamata (alternative, orari liberi).
Solo Scale: voce costruita su misura, report direzionale mensile. **Fuori listino:** chiamate in uscita (richiami automatici,
promemoria, campagne) e numeri verdi: non si promettono.

### Chat e WhatsApp — Arya Customer Care (nome "ARYA Care" non definitivo)
| # | Funzione | Fascia | Stato | Prova |
|---|---|---|---|---|
| 7 | Risponde su WhatsApp, anche a negozio chiuso | tutte | **vendibile** (7/10/2026) | Mr. Toner |
| 8 | Risponde in chat sul sito | tutte | **vendibile** (7/10/2026) | Ecoross |
| 9 | Risponde su Telegram | tutte | **vendibile** (7/10/2026) | conferma di Roberto |
| 10 | Assistenza tecnica sul numero del negozio | tutte | **vendibile** (7/10/2026) | Mr. Toner |
| 11 | Scrive per primo ai nuovi contatti delle campagne e fissa un appuntamento telefonico | tutte | **vendibile** (7/10/2026) | Mr. Toner |
| 12 | Ricontatta i clienti dopo N giorni e invia promozioni (su WhatsApp con un modello approvato da Meta) | tutte | **vendibile** (7/10/2026) | Mr. Toner |
| 13 | Fissa appuntamenti in chat su Google Calendar | tutte | **vendibile** (7/10/2026) | Ecoross |
| 14 | Agisce nei programmi del cliente (ordine nel gestionale, controllo spedizione) | collegamenti da Pro (2 su Pro, 5 su Scale); collegamento su misura a parte | **vendibile** (7/10/2026) | conferma di Roberto |
| 15 | Capisce voce e immagini in chat | da Pro | **vendibile** (7/10/2026) | conferma di Roberto |
| 16 | Passa la conversazione a una persona con tutto il contesto | tutte (non fatturata da Pro) | **vendibile** (7/10/2026) | conferma di Roberto |
| 17 | Stesso numero su WhatsApp Business e Arya (coesistenza) | — | **in arrivo** | serve l'accreditamento Tech Provider Meta (vedi sotto); resta fuori finché Ivan non chiarisce |
| 18 | Il cliente collega da solo il suo numero WhatsApp (Embedded Signup) | — | **in arrivo** | resta fuori finché Ivan non chiarisce |

Dal listino, in tutte le fasce: operatori illimitati nel pannello, tutti i canali di messaggistica e web, raccolta contatti,
follow-up, gradimento e analisi dei temi. Da Pro: memoria storica del cliente, proposte di vendita aggiuntiva.

**Tech Provider Meta — da chiarire.** A settembre era "da verificare" (glossario e product-marketing); secondo Ivan nella progettazione
risulta approvato il 2 settembre 2026. Nelle copie di `archivio-lml-adv/progettazione/` questa data non compare. Finché non è chiarito,
la riga 17 resta "in arrivo". Nota: WhatsApp per i nuovi clienti richiede anche la verifica dell'azienda su Meta, indicata come
ottenuta nel collaudo del 17/09/2026.

### Email — a-Mail ("la casella che si svuota da sola")
| # | Funzione | Fascia | Stato | Prova |
|---|---|---|---|---|
| 19 | Legge, smista, risponde e inoltra le email (Gmail e Outlook) | tutte | **vendibile** (7/10/2026) | conferma di Roberto |

Dal listino: categorie e reparti illimitati e rilevamento di tono e urgenza da Crescita; report direzionale e API da Impresa.
**Non si promettono:** l'analisi degli allegati (PDF, Word) e le notifiche fuori dal pannello (email, Slack, telefono).

## 2. Cosa Arya NON fa (o non si può dire)
- Non dice "intelligenza artificiale" negli annunci: è una scelta (le prove dicono che abbassa la fiducia). Nella chat e al telefono
  invece **deve** dire subito che risponde un assistente automatico (Regolamento UE 2024/1689, art. 50).
- Non ha capacità che non ha: mai attribuirle funzioni che non sono in questa scheda (EU AI Act).
- Non promette la risposta in meno di un secondo (riga 6), la coesistenza del numero (17), il collegamento da soli (18).
- Non fa chiamate in uscita automatiche (richiami, promemoria, campagne) e numeri verdi: fuori listino.
- a-Mail non analizza gli allegati e non manda notifiche fuori dal pannello.
- Non promette sulla fascia Base ciò che è da Pro in su (voce e immagini in chat, riconoscimento del chiamante, collegamenti).
- Non lavora senza un flusso di richieste in entrata: senza clienti che scrivono o chiamano "non ha niente da fare".
- Non usa come propri i numeri di mercato (70-80% risolte senza persona, gradimento 4,1/5…): sono dei fornitori.
- Non ha ancora testimonianze registrate né numeri di un cliente da mostrare.
- Non fa riconciliazione bancaria (modulo in sviluppo con un partner, **non in vendita**).
- "Chiamate perse" non è più un messaggio solo nostro (lo usa un concorrente): serve il pezzo in più, "e fa".
- Nomi dei clienti mai negli annunci (decisione 2); clienti mai in video.

## 3. Ancora da chiarire
1. Righe 6, 17, 18 e Tech Provider Meta **restano fuori dagli annunci** (decisione 11). Quando Roberto conferma che
   funzionano oggi, lascia una nota in OneDrive `macchina-adv/novita-arya/` e l'Osservatorio propone l'aggiornamento.
2. Il nome definitivo del modulo customer care.

## Registro delle modifiche
| Data | Cosa | Fonte | Sì di Ivan |
|---|---|---|---|
| 7/10/2026 | Prima stesura | product-marketing.md v1.3, glossario.md, regole-adv.md v2.5 | — |
| 7/10/2026 | Regola della vendibilità, prove disponibili, listino e offerta di lancio | risposte di Ivan del 7/10/2026 | sì (risposte 7/10/2026) |
| 7/10/2026 | 8 funzioni vendibili (lettura prudente della verifica) | VERIFICA-FUNZIONI.md | — superata dalla riga sotto |
| 7/10/2026 | 16 funzioni vendibili su 19 (tutte tranne 6, 17, 18); fasce dai listini; Tech Provider da chiarire | VERIFICA-FUNZIONI.md, istruzioni di Ivan del 7/10/2026, listini PDF | sì, Ivan Arpino 07.10.2026 |
| 7/10/2026 | Righe 6, 17, 18 e Tech Provider restano fuori finché Roberto non lascia una nota in novita-arya | decisione 11 | sì (risposte al Prompt 2) |
