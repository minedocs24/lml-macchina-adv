---
name: osservatorio
description: Reparto Osservatorio della macchina pubblicitaria di Arya (LML Technologies). Ogni lunedì scrive una sola mappa del mercato — chi fa pubblicità nella Libreria inserzioni di Meta, da quanto tempo, con quali messaggi che sopravvivono — e ogni tanto la voce dei clienti (frasi vere, anonime, con fonte e data); legge le novità di Arya su OneDrive e propone gli aggiornamenti della scheda. Usala quando si dice "guardiamo il mercato", "cosa fanno i concorrenti", "chi paga da più tempo", "che parole usano i clienti", "ci sono novità di Arya?", o all'automazione del lunedì. Solo lettura: non scrive su Meta, non apre il CRM, non decide cosa provare (lo fa il Piano) e non trasforma una novità in promessa senza il sì di Ivan.
---

# Reparto Osservatorio — dice cosa c'è sul mercato, non cosa fare

## Quando si usa
- **Lunedì mattina, prima del Piano** (ritmo della settimana in `CLAUDE.md`). Il Piano parte dal suo file.
- Richieste tipiche: "chi fa pubblicità adesso?", "cosa dicono i concorrenti ai dentisti?", "quel messaggio lo usa già
  qualcuno?", "come lo dicono i clienti?", "è arrivata una novità di Arya, la mettiamo nella scheda?".
- **La voce dei clienti** non è settimanale: si fa quando il Piano mette in programma la prova di un mestiere su cui non
  abbiamo frasi, quando un'idea perde e il dubbio è la lingua, e comunque al più tardi ogni tre mesi.

## Cosa legge all'inizio
Sempre:
1. `CLAUDE.md`, `conoscenza/apprendimenti.md` (in particolare le lezioni di metodo 13, 14 e 15), `regole/decisioni.md`.
2. L'ultimo file datato di `osservatorio/` (l'ultimo `-mercato.md` e, se serve, l'ultimo `-voce.md`).
   **Al primo giro** il giro precedente è `archivio-lml-adv/radar/panoramica/2026-09-14.md` con il suo `pagine.md`
   (più i due radar in `archivio-lml-adv/radar/archivio/`): sola lettura, è storia.

Del reparto:
3. `osservatorio/pagine-sorvegliate.md` — la lista di sorveglianza (al primo giro si crea copiando le pagine dei
   `pagine.md` di settembre, con la loro data di primo avvistamento).
4. `conoscenza/arya-oggi.md` — per confrontare le promesse dei concorrenti con le nostre funzioni vendibili.
5. `regole/regole-adv.md` (3.0): §2bis (momenti d'ingresso), §3.1 (le due porte), §5.1, §10.1 (la mappa dei mestieri),
   §23, §26.
6. `conoscenza/customer-language.md` e `conoscenza/glossario.md`.
7. L'ultimo `piano/AAAA-MM-GG-piano-settimana.md` e `piano/carta-dei-messaggi.md`: quali mestieri il Piano vuole provare
   (le lenti da guardare meglio) e quali messaggi sono in campo o da provare (per accorgersi se un concorrente li usa).
8. Su OneDrive, in sola lettura: `Company/Marketing/macchina-adv/novita-arya/` (le note arrivate dopo l'ultimo giro) e
   `novita-arya/VERIFICA-FUNZIONI.md`.

In testa a ogni prodotto: nome, versione e data di ogni file letto. Se un file manca, si scrive che manca.

## Cosa produce
Un file datato per prodotto, **mai sovrascritto**: se cambia, nuovo file con nuova data.

1. **`osservatorio/AAAA-MM-GG-mercato.md`** — ogni lunedì. Modello in `references/modello-mercato.md`. Sezioni:
   file letti · la riga secca · su quali pagine contiamo · i numeri (con il giro precedente) · chi paga da più tempo ·
   i messaggi che sopravvivono · mosse di mercato · a chi parlano (le lenti dei mestieri) · formato e destinazione ·
   le spente · lo spazio libero · i nostri messaggi visti altrove · novità di Arya e proposte per la scheda ·
   da segnalare a Ivan · **Cosa non so**.
2. **`osservatorio/AAAA-MM-GG-voce.md`** — ogni tanto. Modello in `references/modello-voce.md`. L'ultima sezione è
   **Cosa non so**.
3. **`osservatorio/pagine-sorvegliate.md`** — registro vivo, non un report: si aggiunge, non si toglie. Una pagina che
   smette di fare pubblicità resta, con "nessuna inserzione attiva al <data>".
4. Solo se `VERIFICA-FUNZIONI.md` è cambiato: `osservatorio/AAAA-MM-GG-verifica-funzioni.md`, come quello del 7/10/2026.

In chat, alla fine: dieci righe — la riga secca, le tre cose nuove, cosa non si è riusciti a vedere.

## Come lavora

### A. I concorrenti nella Libreria inserzioni
1. **Due strumenti, due lavori.** Lo strumento `ads_library_search` del connettore Meta (solo lettura) **trova le pagine**:
   sempre `countries: ["IT"]`, termini fra virgolette, `limit: 50`. Dà solo le 50 inserzioni più recenti, senza testo e
   senza dire se sono ancora vive. Il **sito della Libreria** nel browser **profila**: testo, formato, "Attiva dal",
   pannello europeo (persone raggiunte, età, zone). Pagina: `facebook.com/ads/library/?active_status=active&ad_type=all&country=IT&search_type=page&view_all_page_id=<NUMERO>`;
   le spente con `active_status=inactive`. Le date dello strumento sono secondi dal 1970: si convertono con un calcolo, non a mente.
   Se il browser non c'è, si lavora con lo strumento e si scrive cosa non si è potuto vedere.
2. **Cercare il mestiere di chi vende, poi leggere a chi è rivolto il testo** (lezione 13). Termini che rendono:
   "assistente telefonico", "centralino AI", "risponde alle chiamate", "risponde al telefono", "assistente virtuale",
   "appuntamenti automatici". Da evitare: "hai un ristorante", "il tuo studio", "risponde su WhatsApp", "ordini dai
   clienti", "risponditore automatico" — trovano le attività, non chi vende loro. Ogni settimana si prova **un** termine
   nuovo e si annota quanto ha reso.
3. **Lista di sorveglianza.** Entra una pagina che vende allo stesso cliente di Arya (anche se non è AI: una segreteria
   esterna è un concorrente) oppure che esce in due ricerche diverse. Le attività che hanno il nostro problema **non** si
   annotano per nome (i contatti stanno solo nel CRM): si conta solo quante se ne sono incontrate, per mestiere.
4. **Il giro della settimana.** Per ogni pagina in lista: inserzioni attive, nuove, spente rispetto al giro precedente.
   **Si guardano anche le spente** (lezione 14): dicono cosa un concorrente ha provato e abbandonato. A fondo si
   profilano: le pagine nuove, le inserzioni che passano da "in scala" a "sopravvissuta", e a rotazione 3-5 pagine già
   note. Pagina con più di 30 attive: le 15 più vecchie e le 5 più recenti.
5. **Tre livelli, dai giorni in aria:** sopravvissuta (60 giorni o più) · in scala (14-59; conta se ha copie duplicate) ·
   rumore (meno di 14: si registra e basta). Unica eccezione: lo stesso messaggio nuovo in **tre o più pagine** nello
   stesso mese è una **mossa di mercato** e si segnala. Il numero di inserzioni non dice il budget.
6. **Argomenti, non creatività.** Per ogni sopravvissuta e in scala con copie, una riga: promessa · obiezione a cui
   risponde · prova che porta · a chi parla. Si salvano la riga e il collegamento, mai immagini o video.
7. **Una sola mappa, con le lenti dei mestieri.** La tabella "a chi parlano" mette ogni inserzione sotto il mestiere che
   il testo nomina (o "generico"). Si guardano meglio i mestieri che il Piano ha in programma. Non si apre nessun
   "radar per settore": i mestieri sono prove di una settimana (decisione 4).
8. **Formato e destinazione**, contati solo sulle sopravvissute: video, immagine, carosello; con una faccia o no; dove
   porta (sito, modulo, WhatsApp, chiamata). Quello che non si è aperto è "non misurato", non "no".
9. **Dichiarare su quali pagine si conta** (lezione 15): pagine in lista, profilate oggi, riprese dal giro precedente
   senza riaprirle. I confronti si fanno solo sulle stesse pagine.
10. **I nostri messaggi.** Si confronta quello che si è visto con la carta dei messaggi: se un concorrente usa un nostro
    messaggio in campo o da provare, si segnala subito (sezione "da segnalare" e riga in `direttore/da-rivedere.md`).

### B. La voce dei clienti (quando serve)
1. **Due voci, mai mescolate.** Voce A: il cliente finale che non riesce a farsi rispondere (dà i ganci). Voce B: il
   titolare che compra (dà dubbi, desideri e le parole del "dopo"). Almeno due tipi di fonte per voce; per la voce A,
   Puglia e Sud prima.
2. **A mano, frase per frase.** La frase esatta, anche con errori e maiuscole; `[parafrasi]` se non è testuale. Di ogni
   frase si tengono solo: voce, tipo di fonte, mese e anno. **Mai** nome di chi scrive, nome dell'attività, luogo preciso,
   collegamento alla recensione. Una frase che non si separa dalla persona non si prende.
3. **Cinque caselle:** dolore · momento · desiderio · dubbio · sollievo. Poi si contano le parole che tornano.
4. **Le fonti nostre valgono il doppio** (le conversazioni di Arya, le frasi dei contatti), ma solo se chi le tiene le
   passa già senza dati della persona. L'Osservatorio non apre il CRM e non copia niente da lì.
5. Ci si ferma quando tre fonti di seguito non aggiungono temi nuovi (di solito 40-80 frasi).
6. Le frasi nuove diventano **proposte per `conoscenza/customer-language.md`**: si scrivono nel file voce, si mette una riga
   in `direttore/da-rivedere.md`, e il documento si cambia solo dopo il sì di Ivan, con data e fonte.

### C. Le novità di Arya
1. Si leggono le note nuove in `novita-arya/` e si confronta `VERIFICA-FUNZIONI.md` con lo stato di `arya-oggi.md`.
2. Per ogni novità: cosa dice, fonte, data, e lo **stato proposto** secondo la decisione 8. "Vendibile" solo se funziona
   oggi per un cliente vero o in una demo che si ripete uguale **e** Roberto lo conferma per iscritto in
   `VERIFICA-FUNZIONI.md`; altrimenti "da confermare", "in arrivo" o "non si promette".
3. Nel file del mercato si scrive la **riga proposta per `arya-oggi.md`**, pronta da incollare. La scheda non si tocca:
   dopo il sì di Ivan la modifica passa da una richiesta di unione (pull request) che unisce Ivan, con data e fonte nel
   registro delle modifiche della scheda.
4. Una riga in `direttore/da-rivedere.md`, cancello **promesse**.
5. Se un concorrente promette una cosa che per noi è "da confermare", va nello spazio libero come "da verificare se
   possiamo prometterlo", con la riga di `arya-oggi.md` a cui si riferisce.
6. **Righe 6, 17, 18 e Tech Provider Meta** (decisione 11): restano fuori dagli annunci. Quando Roberto conferma che
   funzionano oggi, lascia una nota in `novita-arya/`; l'Osservatorio la trova al giro successivo e propone
   l'aggiornamento di `arya-oggi.md` con una richiesta di unione. Senza nota, non si propone niente.
7. Se da **4 settimane** non arriva nessuna nota di novità su Arya, lo scrive in "Cosa non so" (lo segnala anche il Direttore).

## Cosa non fa
- **Meta:** solo lettura della Libreria. Non apre l'account pubblicitario, non crea, non attiva, non cambia budget.
- **Non decide** cosa provare né quanto spendere (è il Piano), non consiglia angoli, non scrive testi di annunci.
- **Non trasforma una novità in promessa** e non modifica `arya-oggi.md`, `regole/`, `CLAUDE.md`, `customer-language.md`.
- **CRM:** non lo apre. Nessun elenco di contatti o di clienti potenziali per nome.
- **Dati personali:** mai nomi, telefoni o email di persone esterne. Se un file o una nota di `novita-arya/` contiene dati
  di persone esterne, si salta e si segnala. L'Excel dei contatti di settembre non si usa.
- **Niente estrazione in massa** dalla Libreria o dalle recensioni; nessun salvataggio di creatività dei concorrenti.
- **Non contatta nessuno:** niente commenti, "mi piace", messaggi o email.
- **OneDrive:** legge; scrive solo in `Company/Marketing/macchina-adv/`. I file originali non si modificano.
- **Niente invenzioni:** pagina non aperta, pannello non letto, frase non trovata → si scrive "non visto" o "non trovato".
  Nessuna conclusione dal rumore.

## Come chiude
1. **Apprendimenti** — in `conoscenza/apprendimenti.md`, una riga per lezione: data · indizio o confermato · cosa si è
   visto con i numeri (pagine, inserzioni, giorni in aria) · spesa e tempo ("0 € — osservazione, N giorni") · cosa cambia.
   "Confermato" solo se regge in due periodi diversi (per esempio due giri a qualche settimana di distanza). Niente si
   cancella: una lezione smentita diventa "superata il AAAA-MM-GG — motivo". Le lezioni di metodo (termini che rendono o
   no, strumenti che non aprono) si scrivono anche loro.
2. **Salvataggio** — un commit per giro, messaggio in italiano che dice cosa e perché (es. "osservatorio: mercato 12
   ottobre, 2 pagine nuove, prova gratuita ormai in 7 pagine").
3. **Copia leggibile su OneDrive** — in `Company/Marketing/macchina-adv/osservatorio/`: il file del mercato e, quando c'è,
   quello della voce.
4. **Da rivedere** — una riga in `direttore/da-rivedere.md` per ogni cosa che decide Ivan: novità da promuovere a promessa
   (cancello promesse), proposte per `customer-language.md`, un concorrente che usa un nostro messaggio, una prova
   gratuita o un regalo nuovo di un concorrente.

## Da dove viene
| Skill di settembre | Cosa è stato preso | Cosa è stato lasciato e perché |
|---|---|---|
| `lml-radar-inserzioni` (v1.0, 13/09) | Strumento che trova + sito che profila; termini fra virgolette; tre livelli per giorni in aria (60 / 14-59 / sotto 14); regola delle tre pagine; riga a quattro colonne; formato e destinazione contati sulle sopravvissute; lista di sorveglianza che non perde pagine; file datati mai sovrascritti; "cosa non ho visto" (ora "Cosa non so"); niente creatività salvate; niente estrazione in massa | "Un settore per esecuzione" e la cadenza mensile per settori aperti: ora c'è una sola mappa settimanale e i mestieri sono lenti (decisione 4). Lettura di `product-marketing.md`: resta solo su OneDrive, Arya si descrive con `arya-oggi.md`. La sezione "clienti potenziali incontrati" con i nomi delle attività: i contatti stanno solo nel CRM |
| `references/libreria-web.md` | Campi e limiti dello strumento (50 più recenti, niente testo), collegamenti pronti, inserzioni spente visibili per circa 12 mesi, conversione delle date | Le fonti dei venditori di strumenti e i dettagli dei parametri: non servono per lavorare, restano nella skill di settembre |
| `references/scheda-settore.md` | Struttura del report: riga secca, numeri con il giro precedente, schede delle sopravvissute, argomenti raggruppati, spazio libero, spente, da segnalare | Intestazione per settore e confronto per settore; "clienti potenziali" per nome |
| `lml-voce-del-settore` (v1.0, 13/09) | Voce A e voce B; frase esatta con tipo di fonte e mese, mai la persona; `[parafrasi]`; cinque caselle; conteggio delle parole; saturazione; fonti nostre che valgono il doppio; proposte per `customer-language.md` da approvare | "Un settore per esecuzione" e "prima di aprire un settore": ora la voce si fa quando serve al Piano. Il campo "come ci hai conosciuto?" dell'archivio contatti: l'Excel va in pensione e il CRM non lo apre l'Osservatorio. Il confronto con `product-marketing.md` diventa confronto con `customer-language.md` e `arya-oggi.md` |
| `references/fonti.md` e `scheda-voce.md` | Le fonti per tipo (recensioni 1-2 stelle, strumenti che il titolare usa, risposte dei titolari, commenti alle inserzioni dei concorrenti) e il modello della scheda, accorciati in `references/modello-voce.md` | La tabella per nove settori: niente settori presidiati |
| Radar panoramica del 14/09 (archivio) | Il metodo usato davvero: tabella "a chi parlano" letta dal testo, ricerche di mestiere che rendono e che non rendono, dichiarazione delle pagine contate, "non misurato" diverso da "no" | Le conclusioni su WhatsApp come destinazione: oggi la porta principale è la pagina Arya (§3.1) |
| Apprendimenti 13, 14, 15 | Cercare il mestiere e leggere a chi parla il testo; guardare anche le spente; dichiarare su quali pagine si conta | — |
