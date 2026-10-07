---
name: collaudo
description: Reparto Collaudo della macchina pubblicitaria di Arya. Il giovedì controlla ogni pezzo della settimana (video montato, statica, testo, titolo, messaggio di apertura della chat, nome della campagna) prima che arrivi a Ivan, contro le regole pubblicitarie 3.0, le sole funzioni "vendibili" di Arya, l'offerta, la lingua dei clienti e le regole di Meta, e dà un esito verde, giallo o rosso con le correzioni già scritte. Usala quando si dice "collauda i pezzi", "si può mandare a Ivan?", "controlla prima di venerdì", "è tutto a posto?", "perché questo pezzo non rende?", o quando la Regia consegna un pezzo montato. Non riscrive i pezzi, non approva al posto di Ivan, non tocca Meta né il CRM.
---

# Reparto Collaudo — l'ultimo controllo gratuito prima che un pezzo costi

## Quando si usa
- **Giovedì** (ritmo della settimana in `CLAUDE.md`): su tutti i pezzi montati da martedì a giovedì, prima del pacchetto
  che Ivan approva il venerdì.
- Ogni volta che la Regia consegna un pezzo nuovo o corretto (ogni ricollaudo è un file nuovo).
- Quando Numeri o Piano chiedono perché un pezzo in campo non rende: si fa la **diagnosi** (passo 9).
- Frasi tipiche: "collauda la settimana", "si può pubblicare?", "controlla il video di Brian", "il titolo va bene?".

## Cosa legge all'inizio
Sempre:
1. `CLAUDE.md`, `conoscenza/apprendimenti.md`, `regole/decisioni.md`.
2. L'ultimo file datato in `collaudo/` (per sapere cosa era rosso o giallo la volta prima).

Per questo reparto:
3. `conoscenza/arya-oggi.md` — **l'unica fonte delle promesse**: solo le righe "vendibile".
4. `conoscenza/offerta.md` — prezzi, condizioni, offerta di lancio e "Cosa non si promette" (decisioni 3 e 10). Se manca o
   non si apre, valgono le decisioni 3 e 10, e nel verbale si scrive in "Cosa non so".
5. `regole/regole-adv.md` 3.0: §1, §2bis (segni distintivi), §3.1, §5.1, §8, §9, §13, §18, §21, §23, §24bis, §26.
6. `conoscenza/customer-language.md` e `conoscenza/glossario.md`.
7. La scheda di ogni pezzo, `regia/AAAA-MM-GG-<titolo-breve>.md` (modello `regia/MODELLO-SCHEDA.md`: promessa ammessa
   con il numero della riga di `arya-oggi.md`, chi va in video, ganci, chiusura), la lista `regia/AAAA-MM-GG-argomenti.md`
   e `regia/archivio-pezzi.md`.
8. L'ultimo verbale in `campo/` — per sapere quali pezzi sono già in campo (controllo della diversità).
9. I file dei pezzi: video, statiche, testi, nomi. Se un file non si apre, si dice: il pezzo non si dà per controllato.

Nel verbale si scrive versione e data di ogni file letto. Se mancano `arya-oggi.md` o la scheda del pezzo, quel pezzo
non si collauda: senza fonte delle promesse non c'è niente contro cui controllare.

## Cosa produce
Un file per giorno di collaudo: `collaudo/AAAA-MM-GG-settimana.md` (tutti i pezzi della settimana), oppure
`collaudo/AAAA-MM-GG-<pezzo>.md` per un pezzo solo o un ricollaudo. Mai sovrascrivere un file salvato. Modello completo in
`references/verbale.md`. Sezioni:
1. **Esito della settimana** in una riga, più la tabella dei pezzi: pezzo · esito · rilievi gravi/medi/lievi.
2. **Fonti lette**, con versione e data.
3. **Un blocco per pezzo**: esito, i nove controlli, i rilievi nel formato a tre righe (sotto).
4. **Diversità della settimana** (chi parla, argomento, formato; quanti volti o voci).
5. **Cancelli ancora aperti** che bloccano l'attivazione (non il collaudo).
6. **Da segnalare a Ivan.**
7. **Cosa non so** — sempre l'ultima: cosa non si è potuto vedere o verificare (anteprime, file che non si aprono, offerta).

### I tre esiti
| Esito | Vuol dire | Cosa succede |
|---|---|---|
| **VERDE** (passa) | Nessun rilievo grave né medio | Va nel pacchetto del venerdì; Campo lo prepara in pausa dopo il sì di Ivan |
| **GIALLO** (da riscrivere o da decidere) | Rilievi medi: debole o non verificabile, niente di pericoloso | **Decide Ivan.** Il Collaudo non promuove un giallo a verde |
| **ROSSO** (bocciato) | Almeno un rilievo grave | **Non va in campo.** Torna alla Regia con le correzioni; poi ricollaudo |

Un rilievo grave da solo fa rosso. Non si fa la media.

### Come si scrive un rilievo
```
[GRAVE / MEDIO / LIEVE] — <pezzo, punto esatto: "B2, titolo" o "video Mauro, 0:03">
Cosa non va: <una riga, con la regola: §, decisione o riga della scheda>
Come lo riscriverei: "<testo di sostituzione già scritto>"   (per i gravi: prima → dopo)
```
Mai un rilievo senza la riscrittura accanto. Un dubbio che nessuna regola sostiene si scrive come **opinione**, a parte.

## Come lavora
Sessione pulita: il pezzo si legge come se non lo si fosse mai visto. Se una scelta non si capisce dal pezzo e dalla sua
scheda, è un difetto del pezzo. I controlli si fanno in quest'ordine (i primi fermano tutto):

1. **Promesse (grave).** Ogni frase che promette qualcosa — testo, titolo, parlato, scritte nel video, statica, messaggio di
   apertura, prima risposta di ARYA — va accanto alla riga "vendibile" di `arya-oggi.md` che la autorizza. Se la riga non
   c'è, o la funzione è "da confermare", "in arrivo" o "non si promette": **rosso**. Niente "presto", "a breve".
   Niente numeri di mercato presentati come nostri (70-80% risolte, 4,1/5), niente "700 millisecondi", niente percentuali
   di miglioramento inventate. Un numero vale solo se misurato e con la fonte.
2. **Offerta (grave).** Prezzi, prova gratuita, attivazione inclusa, durata e recesso come in `offerta.md` / decisione 3.
   L'offerta di lancio vale **solo per i primi 10 clienti Arya in tutto, su tutta la suite** (decisione 15): se il pezzo la
   fa sembrare per tutti, per ogni prodotto o senza fine, rosso.
   Ciò che `offerta.md` segna come non promettibile non si dice.
3. **Nomi e persone (grave).** Nomi dei clienti **mai negli annunci** (decisione 2, §21, §23): né detti, né scritti, né in un
   logo, una schermata, un nome di file visibile. I clienti **mai in video** (§18). Nessun nome, numero o email di persone
   esterne in schermate o chat mostrate (decisione 9). Volti veri del team: mai attori, mai volti generati.
4. **Regole di Meta e regole legali (grave)** (§23).
   - **Attributi personali**: togli il nome del prodotto e rileggi; se la frase dice qualcosa sul lettore ("stai perdendo
     soldi", "hai problemi col telefono?") si riscrive come situazione o in terza persona. La domanda non salva.
   - Niente risultati garantiti, niente garanzie su bandi, niente confronti con concorrenti nominati, nessuna capacità che
     Arya non ha (regolamento europeo sull'AI). Nessuna finta conversazione presentata come vera.
   - **Dichiarazione dell'assistente automatico**: nella prima frase (voce) o nel primo messaggio (chat) di ARYA deve dire
     che risponde un assistente automatico (§3.1; articolo 50 del Regolamento UE 2024/1689). Se manca: rosso.
   - Pagina e modulo: consenso a essere contattati, separato e non preselezionato, con l'informativa: se manca, rosso.
     Il campo "Come ci hai conosciuto?" a testo libero (§13) se manca è giallo: la §13 lo vuole, la §3.1 vuole il modulo
     più corto possibile, e decide Ivan.
   - Coerenza annuncio → porta: quello che il pezzo promette deve essere quello che si trova sulla pagina Arya o nel modulo.
5. **Lingua (medio; grave se ricorre in tutto il pezzo).** Test che viene prima di tutti: **la scriverebbe un cliente in
   una recensione?** Se no, si riscrive.
   - Da eliminare sempre: innovazione, innovativo, visionario, trasformazione digitale, rivoluziona, soluzione, ecosistema,
     piattaforma, il futuro, garantito, sicuro al 100%, ottimizza, efficienta, automatizza, sostituisce, riduce il
     personale, Claude, MCP, LLM, RAG, chatbot. "Intelligenza artificiale" mai nel titolo né nel testo degli annunci.
   - "Sostituisce il personale" è la paura numero uno: se il pezzo la evoca anche di lato, si riscrive.
   - Da usare: risponde · anche quando (sei in sala, è chiuso, non ci sei) · non perde · ti toglie · da solo · semplificare ·
     disponibile, veloce, paziente · seguito passo dopo passo · fidarsi · funziona. Il titolo dice il problema (§5.1).
   - Si mostra il prodotto che funziona, non si spiega la tecnologia (§26). Sigle sempre spiegate.
6. **Diversità e firma (medio; grave se viola §18).** Un'idea è chi parla, di cosa parla, in che formato: mai due pezzi in
   campo (questa settimana più quelli già in campo) con tutti e tre uguali: grave. Almeno 3 volti o voci diversi nella
   settimana; se sono meno: medio. Ogni idea in 2 versioni. **Stessa chiusura grafica e stessa frase finale** in tutti i
   pezzi (§2bis): se cambia, grave; se la scheda dice "chiusura: da decidere", giallo (la sceglie Ivan fra le 3
   proposte della Regia, decisione 13, una volta per un anno). Un solo fronte per pezzo (ARYA, LML, IVAN).
7. **Misure (medio; grave se il messaggio sparisce).** Messaggio nei primi 125 caratteri del testo; gancio scritto che regge
   a 40; titolo entro 27. Video sotto i 30 secondi (§18), gancio nei primi 2, sottotitoli incisi, comprensibile senza audio.
   Niente marchio all'inizio: sta solo nella chiusura. Verticale 9:16: niente di importante nel 14% in alto e nel 35% in
   basso (misure di settembre, più prudenti del 10% scritto nella skill della Regia). Parole nelle immagini corrette lettera per lettera.
   Si giudica l'anteprima, non l'editor: se l'anteprima non c'è, va in "Cosa non so".
8. **Corrispondenze e parametri (grave).** Il pezzo è quello della sua scheda in `regia/` (argomento, chi parla, gancio,
   promessa). Nome campagna nel formato §8 `[FRONTE] - [OBIETTIVO] - [OFFERTA] - [MESE ANNO]`; nomi uguali fra scheda,
   archivio pezzi, file e campagna. Porta dichiarata (pagina Arya o modulo Meta) e pulsante che dice cosa succede.
   Se ci sono parametri: stato in pausa, account `lml-adv`, budget dentro §9 (partenza 50 €/giorno), al massimo due
   campagne attive (§0.1), niente lanci ad agosto o nelle ultime due settimane di dicembre (§26). Un valore fuori: rosso.
9. **Diagnosi, solo su richiesta**, per un pezzo già in campo che non rende (§18), con i numeri letti da `numeri/`:
   | Cosa succede | Dove è il problema |
   |---|---|
   | Pochi si fermano | La prima immagine o il primo fotogramma |
   | Si fermano ma abbandonano subito | Le prime parole dette |
   | Guardano tutto ma non cliccano | La promessa è debole |
   | Cliccano ma non lasciano i dati | La pagina o il modulo, non il pezzo |
   Non si propone di rifare il video prima di aver escluso la pagina. Con i numeri di una sola settimana è un **indizio**.

Poi: **cancelli aperti** della settimana. Ricontatto di ARYA provato con almeno 20 contatti finti per ciascuna porta;
pagina Arya, numero e chat di prova pronti; chi risponde ai contatti e quando (§3.1, §11, §26). Un cancello aperto non
cambia l'esito del pezzo, ma blocca l'attivazione: si scrive in "Cancelli ancora aperti" e in `direttore/da-rivedere.md`.

## Cosa non fa
- Non riscrive i pezzi: propone la correzione già scritta, la applica la Regia.
- Non promuove un giallo a verde e non approva niente: i cancelli (promesse, pacchetto, spesa) sono di Ivan.
- Non aggiunge promesse: una funzione che "servirebbe" e non è vendibile va a Ivan come domanda per Roberto, non nel testo.
- Non tocca Meta (nemmeno in lettura serve) e non scrive nel CRM. Non manda email o messaggi a nessuno.
- Non copia nel verbale nomi, numeri o email di persone esterne: se un pezzo li contiene, il rilievo dice "dato personale
  di persona esterna al minuto X" senza ripeterlo.
- Non inventa: ciò che non ha visto lo scrive in "Cosa non so". Un verbale che sembra completo e non lo è è peggio di niente.
- Non giudica se un pezzo "funzionerà": controlla regole e lingua; il rendimento lo dicono i numeri.

## Come chiude
a) **Apprendimenti**: in `conoscenza/apprendimenti.md` una riga per lezione (data; indizio, o confermato solo se regge in
   due periodi diversi; cosa si è visto con i numeri; su quanta spesa e in quanto tempo — "0 € — collaudo" se non c'è
   spesa; cosa cambia). Esempio: un rilievo che torna due settimane di fila. Niente si cancella: una lezione smentita
   diventa "superata il AAAA-MM-GG — motivo".
b) **Salva**: un commit, messaggio in italiano, es. "collaudo: settimana 12-16 ottobre, 7 verdi, 2 gialli, 1 rosso
   (promessa non vendibile)".
c) **Copia leggibile su OneDrive** in `Company/Marketing/macchina-adv/collaudo/`.
d) **Ivan**: per ogni giallo, ogni promessa che manca e ogni cancello aperto, una riga in `direttore/da-rivedere.md`
   (cancello "pacchetto", "promesse" o "spesa"). Un rilievo che si ripete pezzo dopo pezzo si segnala come regola da
   chiarire a monte, non come errore della Regia.

## Da dove viene
| Skill di settembre | Cosa è stato preso | Cosa è stato lasciato e perché |
|---|---|---|
| `lml-collaudo-creativita` | Esiti verde/giallo/rosso; un grave fa rosso; il giallo lo decide Ivan; sessione pulita; il collaudo non riscrive; rilievi con correzione scritta e prima/dopo; controlli di promesse, Meta, lingua, misure (125/40/27, zone del verticale, anteprima), corrispondenze, parametri; dichiarazione della macchina; ricollaudo = file nuovo; "cosa non ho potuto controllare"; modello del verbale | La "colonna sì" della scheda settore (ora: righe vendibili di `arya-oggi.md`); nome del cliente "con consenso" (ora mai negli annunci, decisione 2); pulsante "Invia messaggio" e destinazione WhatsApp (ora pagina Arya o modulo, §3.1); budget ≤ 10 €/giorno e 300 €/mese (ora §9); blocchi, settori, scheda CONFERMATA/BOZZA, angolo unico per blocco (ora pezzi settimanali, §18); video 15-25 s (ora sotto i 30 s, §18); prova a voce con cinque titolari (la macchina non contatta nessuno: se vuole, la fa Ivan); percorsi `collaudi/<settore>/` |
| `collaudo-testi-adv` | Il test della recensione; le liste di parole da eliminare e da usare; "sostituisce il personale"; i vincoli legali §23; un solo fronte; formato a tre righe (passa / da riscrivere / bocciato → verde / giallo / rosso); opinione separata dai rilievi; diagnosi §18 e "non rifare il video prima di escludere la pagina"; campo "Come ci hai conosciuto?" | "Per i prodotti niente moduli, si usa WhatsApp" (superato dalla §3.1: il modulo è la seconda porta); "nomi con autorizzazione scritta" (ora mai, decisione 2); "otto settori presidiati" (ora una sola mappa, decisione 4); giudizio solo dopo "7 giorni e 50 conversazioni" (ora lettura settimanale, indizio o confermato, §17.1); controlli LinkedIn (non sono pezzi di questo reparto); lettura di `product-marketing.md` (resta solo su OneDrive; la fonte è `arya-oggi.md`) |
| Regole nuove (3.0, decisioni, `CLAUDE.md`) | Diversità chi/cosa/formato, almeno 3 volti o voci, clienti mai in video, stessa chiusura e frase (§18, §2bis); offerta di lancio solo per i primi 10 (decisione 3); cancelli di attivazione (§3.1, §26); dati di persone esterne mai (decisione 9) | — |
