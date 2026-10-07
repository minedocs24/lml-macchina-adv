---
name: regia
description: Reparto Regia creativa della macchina pubblicitaria di Arya. Ogni lunedì sceglie gli argomenti dei reels e dei post da sponsorizzare nella settimana, scrive una scheda di una pagina per ognuno (secondo regia/MODELLO-SCHEDA.md) e tiene regia/archivio-pezzi.md. Usala quando si dice "gli argomenti della settimana", "cosa giriamo", "la scheda del reel", "prepara le schede per la persona social", "aggiorna l'archivio dei pezzi", o quando chi gira chiede "mi scrivi il copione completo?". Non gira, non monta, non collauda, non tocca Meta e non spende: i pezzi li girano e li montano la persona social e il cast.
---

# Reparto Regia creativa — gli argomenti della settimana, una scheda di una pagina per pezzo

## Quando si usa

- **Lunedì** (ritmo della settimana in CLAUDE.md): dopo Osservatorio e Piano, Regia scrive gli argomenti della settimana
  e una scheda per ognuno. Ivan può **bocciarne uno entro martedì alle 12**; se non dice niente, si gira.
- **Martedì-giovedì:** la persona social e il cast girano e montano. Regia scrive il **copione completo solo se lo chiede
  chi gira** (`references/copione-su-richiesta.md`).
- **Quando arrivano i numeri** (file nuovi in `numeri/`): Regia aggiorna `regia/archivio-pezzi.md`.
- Richieste tipiche: "cosa giriamo questa settimana?", "fammi la scheda del reel sul telefono che squilla",
  "serve un post statico", "il copione per Brian", "segna nell'archivio come è andato il reel di Mauro".

## Cosa legge all'inizio

Sempre, prima di scrivere una riga:
1. `CLAUDE.md`, `regole/decisioni.md`, `conoscenza/apprendimenti.md`.
2. L'ultimo file datato in `regia/` (di solito la lista argomenti della settimana prima) e `regia/archivio-pezzi.md`.
3. `conoscenza/arya-oggi.md` — **unica fonte** su Arya. Si usano solo le righe "vendibile", con la fascia giusta.
   Prezzi e condizioni solo da `conoscenza/offerta.md`.
4. `regole/regole-adv.md` (3.0): §1 (cancelli), §2bis (segni distintivi), §3.1 (le due porte), §5.1, §17.1, §18, §21, §23, §26.
5. Il piano della settimana: l'ultimo `piano/AAAA-MM-GG-*.md` (cosa provare, a chi, con quanto budget).
6. `piano/carta-dei-messaggi.md` — i messaggi ammessi e già provati.
7. La voce dei clienti: `conoscenza/customer-language.md` e l'ultimo file di voce in `osservatorio/`.
8. L'ultimo radar dei concorrenti in `osservatorio/` (per gli spunti di struttura).
9. L'ultimo report in `numeri/` (cosa ha reso, cosa no) e `regia/MODELLO-SCHEDA.md`.

In testa a ogni prodotto si scrivono **nome, versione e data** di ogni file letto. Se un file manca (es. non c'è ancora la
carta dei messaggi o il piano della settimana), si scrive che manca e si lavora con quello che c'è, senza inventare.

## Cosa produce

Tre prodotti. Un file datato per prodotto, **mai sovrascritto**: se cambia, nuovo file con nuova data.

**1. La lista del lunedì — `regia/AAAA-MM-GG-argomenti.md`**
1. File letti (nome, versione, data).
2. La settimana in breve: cosa dice il piano (prova, budget) in tre righe.
3. Gli argomenti: tabella con #, titolo, per chi, chi va in video, formato, promessa ammessa (riga di arya-oggi),
   primo gancio, nome del file della scheda.
4. Un argomento **di riserva** (stesse colonne): prende il posto di quello bocciato.
5. Controllo diversità: le regole qui sotto, una riga per regola, con "sì" o "no".
6. Il cancello: "Ivan può bocciarne uno entro martedì [data] alle 12, in `direttore/da-rivedere.md`; altrimenti si gira".
7. **Cosa non so.**

**2. Una scheda per pezzo — `regia/AAAA-MM-GG-<titolo-breve>.md`**
Segue `regia/MODELLO-SCHEDA.md`. Sta in **una pagina** (circa 40 righe). Le voci, in quest'ordine:

| Voce | Cosa ci va |
|---|---|
| Titolo | corto; **mai "intelligenza artificiale"** |
| Per chi | chi deve fermarsi a guardare: chi gestisce telefono, chat o email di un'attività (decisione 4) |
| Argomento | il momento concreto (§2bis, momenti d'ingresso), in una frase |
| Promessa ammessa | una sola, **solo funzioni "vendibili"** di arya-oggi.md, con il numero della riga, la data della conferma e la fascia se non è "tutte" |
| Formato e durata | reel 9:16 (ritaglio 4:5), post 4:5 o 1:1; video **15-30 secondi** |
| Chi va in video | uno del cast: Ivan, Brian, Riccardo, Mauro, la persona social, un tecnico, la voce di Arya. **Mai clienti** |
| Tre ganci | tre aperture diverse, ognuna dentro i **primi 2 secondi**, scritte a schermo; ognuna cita la frase dei clienti da cui nasce |
| Cosa far vedere | la scena, non la spiegazione; comprensibile **senza audio** (sottotitoli sempre) |
| Chiusura | la **chiusura grafica e la frase uguali per tutti** i pezzi; l'invito porta alla pagina Arya (§3.1) |
| Da evitare | parole e immagini vietate per questo pezzo |
| Spunto | la **struttura** di un pezzo di un concorrente (dal radar), mai testo né immagini |
| Cosa vogliamo capire | la domanda che i numeri devono chiudere, scritta come indizio da verificare |

In fondo alla scheda, due righe fisse: "Copione completo: solo se lo chiede chi gira" e **Cosa non so**.

**3. L'archivio — `regia/archivio-pezzi.md`** (registro che cresce, non un report: si aggiunge, non si cancella)
Una riga per reel o post: argomento, chi parla, formato, gancio (prime parole), date (dal-al), numeri, esito
("vince", "pari", "perde", "ritirato (motivo)"). I numeri si copiano dai file di `numeri/`, citando il file; mai stimati.

## Come lavora

1. **Legge** tutto l'elenco sopra. Se `arya-oggi.md` non ha funzioni "vendibili", si ferma: niente schede, una riga in
   `direttore/da-rivedere.md` (decisione 8).
2. **Conta i pezzi.** Il piano dice quante idee: di regola 3-5 idee nuove a settimana, ognuna in 2 versioni (§18).
   All'inizio quasi tutto nuovo; quando ci sono vincenti in archivio, 70% varianti dei vincenti e 30% idee nuove.
3. **Sceglie gli argomenti** dalla carta dei messaggi e dal piano: un momento concreto, una promessa vendibile.
   Un argomento per un singolo mestiere è una prova di una settimana (decisione 4). Evita "chiamate perse" da solo:
   serve il pezzo in più, "e fa" (arya-oggi §2; apprendimento 3).
4. **Chi parla e formato:** li prende dal piano della settimana se li indica, altrimenti li propone. Poi fa il
   **controllo diversità** su questa settimana e sui pezzi ancora in campo (letti in archivio):
   - mai due pezzi con **stessa persona, stesso argomento e stesso formato** (§18); quindi le 2 versioni di un'idea
     cambiano almeno chi parla o il formato, non solo il gancio (la carta dei messaggi ammette "due ganci": vale §18);
   - **almeno 3 volti o voci diversi** nella settimana;
   - **clienti mai in video**, né la loro voce. La voce di Arya si registra **solo da una demo** che si ripete uguale
     (arya-oggi), mai da una conversazione di un cliente vero.
5. **Scrive i tre ganci** partendo dalle frasi dei clienti (customer-language.md o voce dell'Osservatorio), citando la
   fonte. Ogni gancio passa due test:
   - **attributi personali di Meta** (§23): togli il nome del prodotto e rileggi; se la frase dice qualcosa sul lettore
     ("stai perdendo clienti?", "sei in difficoltà?"), si riscrive come situazione o in terza persona;
   - **la recensione**: lo scriverebbe un cliente in una recensione? Se no, si riscrive.
6. **Scrive "cosa far vedere"** perché si capisca a volume zero: gancio scritto a schermo nel primo fotogramma,
   sottotitoli incisi, niente logo all'inizio (il marchio sta solo nella chiusura), niente di importante nel 10% in
   alto e in basso del 9:16.
7. **Mette la chiusura uguale per tutti.** Se chiusura grafica e frase non sono ancora state decise (§2bis: si decidono
   una volta e non si cambiano per un anno), **nella prima settimana la Regia ne propone 3** (decisione 13), ognuna con
   la frase e la descrizione della chiusura grafica, in `regia/AAAA-MM-GG-chiusure.md` con una riga in
   `direttore/da-rivedere.md` (cancello "pacchetto"): **sceglie Ivan**. Finché non ha scelto, la scheda scrive
   "chiusura: da decidere". L'invito dice cosa succede davvero: pagina Arya (chiama il numero, prova la chat,
   fatti richiamare). Se la pagina non è pronta, lo scrive (§0.1).
8. **Cerca lo spunto** nel radar dell'Osservatorio: si prende la struttura (es. "domanda a schermo, poi risposta dal
   vivo"), mai le parole, le immagini o la musica di un concorrente.
9. **Scrive "cosa vogliamo capire"**: una domanda sola, che i numeri della settimana possono chiudere come indizio.
10. **Salva** la lista e le schede, aggiunge in archivio una riga per pezzo con date "da girare", e scrive la riga del
    cancello in `direttore/da-rivedere.md`.
11. **Martedì dopo le 12** rilegge `direttore/da-rivedere.md`. Se Ivan ha bocciato un argomento, al suo posto va la
    riserva (Ivan l'ha già vista nella stessa lista); si segna in archivio "bocciato da Ivan il [data]". Nessun'altra
    modifica alla lista: se serve, file nuovo con nuova data.
12. **Su richiesta di chi gira**, scrive il copione completo (`references/copione-su-richiesta.md`) in un file datato
    `regia/AAAA-MM-GG-<titolo-breve>-copione.md`. Per un post statico vale `references/pezzo-statico.md`.
13. **Quando arrivano i numeri**, aggiorna date, numeri ed esito in archivio, citando il file di `numeri/`.

## Cosa non fa

- **Non gira e non monta.** Lo fanno la persona social e il cast. Non scrive il copione se nessuno lo chiede.
- **Non promette niente che non sia "vendibile"** in arya-oggi.md: niente "da confermare", "in arrivo", "non si
  promette", niente funzioni prese dalla memoria o da altre fonti. Al 7/10/2026 restano fuori le righe 6 (meno di un
  secondo), 17 (stesso numero WhatsApp) e 18 (collegamento da soli), le chiamate in uscita automatiche e i numeri dei
  fornitori presentati come nostri; ciò che è "da Pro" non si presenta come compreso in tutte le fasce.
- **Non scrive prezzi o condizioni** fuori da `conoscenza/offerta.md` (decisioni 3 e 10); l'offerta di lancio solo con
  le parole lì indicate ("per i primi dieci clienti").
- **Non mette nomi di clienti** negli annunci (decisione 2), né clienti in video, né conversazioni vere di clienti.
- **Non scrive "intelligenza artificiale"** nei titoli né nei testi degli annunci (arya-oggi.md §2; regole-adv §5.1 e §26).
- **Non copia** testi, immagini, musiche o volti dei concorrenti.
- **Non tocca Meta** (nemmeno in lettura: i numeri li legge Numeri) e **non tocca il CRM**.
- **Non spende:** nessuno strumento a pagamento (generatori di immagini o video) senza il sì di Ivan (decisioni 5 e 6).
- **Non approva** al posto di Ivan e **non collauda**: il controllo lo fa Collaudo il giovedì.
- **Non manda** email o messaggi a nessuno: la persona social trova le schede in archivio e su OneDrive.
- **Dati personali:** nessun nome, telefono o email di persone esterne. Se un file letto ne contiene, si salta e si segnala.
- **Niente invenzioni:** se manca un dato (la chiusura, la carta, il piano, i numeri), si scrive cosa manca.

## Come chiude

a. **Apprendimenti:** in `conoscenza/apprendimenti.md`, una riga per lezione: data, indizio o confermato (confermato
   solo se regge in due periodi diversi), cosa si è visto con i numeri, su quanta spesa e in quanto tempo, cosa cambia.
   Lezioni tipiche di Regia: quale gancio, quale volto, quale formato ha reso. Niente si cancella: una lezione smentita
   diventa "superata" con motivo e data.
b. **Salvataggio:** un commit per lavoro, messaggio in italiano chiaro, es.
   "regia: argomenti 12-16 ottobre, 4 idee, 4 volti, riserva sul B&B".
c. **Copia su OneDrive:** lista e schede in `Company/Marketing/macchina-adv/regia/` (qui le legge la persona social).
d. **Da rivedere:** in `direttore/da-rivedere.md` la riga del cancello del lunedì (scadenza martedì alle 12) e ogni
   decisione che serve a Ivan (es. la chiusura comune, una promessa che manca).

## Da dove viene

Le tre skill di settembre sono in archivio (`.claude/skills/archivio/`, secondo CLAUDE.md). Si è preso il metodo, non il
flusso: la scheda di una pagina sostituisce il pacchetto completo.

| Skill di settembre | Cosa è stato preso | Cosa è stato lasciato e perché |
|---|---|---|
| `lml-pacchetto-inserzione` (SKILL, `modello-pacchetto.md`, `vincoli-formati.md`) | Test degli attributi personali con esempi; ganci costruiti da frasi dei clienti con la fonte citata; gancio che regge senza audio; zona di sicurezza; "cosa prova questa creatività" (diventa "cosa vogliamo capire"); promessa citata con la riga che la autorizza | Settore CONFERMATO e coda angoli (decisione 4: niente settori); blocchi di 3-4 settimane (§18: idee settimanali); destinazione WhatsApp, pulsante "Invia messaggio", messaggio di apertura (§3.1: porta principale pagina Arya; testi e pulsanti sono di Campo); nomi delle campagne (Campo); "colonna sì della scheda settore" (ora arya-oggi.md "vendibile"); "la faccia di Ivan" (ora cast a rotazione) |
| `lml-copione-video-adv` (SKILL, `modello-copione.md`, `copione-originale-v1.md`) | Gancio nei primi 2-3 secondi scritto a schermo; sottotitoli incisi; marchio solo in fondo; i quattro blocchi, il conto parole/secondi, i silenzi recitati, le regole di sottrazione e la doppia versione del gancio: tutto in `references/copione-su-richiesta.md` | Copione sempre obbligatorio (ora solo se lo chiede chi gira); 15-25 secondi (ora 15-30, regola del brief e §18 "sotto i 30"); "nessuna ripresa prima del collaudo e del sì di Ivan" (ora si gira dopo il cancello di martedì, Collaudo il giovedì); registrazione di Arya "da conversazione vera" (ora solo demo, per dati personali e clienti mai in video); la ricerca d'attualità e i sette blocchi dell'originale (sono del profilo personale) |
| `lml-tavole-adv` (SKILL, `composizione.md`, `direzioni.md`) | Un messaggio per immagine; gerarchia titolo → immagine → invito → marchio; formati 9:16, 4:5, 1:1 con le zone coperte; niente volti, loghi, schermi leggibili, cliché; firma LML Technologies: in `references/pezzo-statico.md` | Prompt dettagliati e coordinate per il generatore (Regia non genera senza il sì di Ivan: costa); palette delle due direzioni (rimandata alla chiusura comune, da decidere una volta); invito "si apre WhatsApp" (ora pagina Arya); "molte varianti per blocco" (ora 2 versioni per idea, §18) |
