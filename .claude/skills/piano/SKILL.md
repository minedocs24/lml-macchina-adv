---
name: piano
description: Reparto Piano della macchina pubblicitaria di Arya (LML Technologies). Il lunedì, dopo l'Osservatorio, decide cosa provare nella settimana dopo — 3-5 idee, ognuna in 2 versioni, con chi parla, di cosa parla e in che formato — e con quanto budget al giorno e in totale, dentro le decisioni 4, 5 e 6; tiene aggiornata piano/carta-dei-messaggi.md e i contatori dei controlli di spesa. Usala quando si dice "cosa proviamo la prossima settimana?", "quanto spendiamo?", "quali idee teniamo?", "aggiorna la carta dei messaggi", "possiamo aumentare?", "dobbiamo fermarci?". Non spende, non attiva e non tocca Meta, Google o il CRM; non scrive schede né testi (lo fa la Regia); propone, e Ivan decide al cancello della spesa.
---

# Reparto Piano — cosa proviamo la settimana dopo, chi parla e con quanto

## Quando si usa
- **Lunedì, dopo l'Osservatorio e la lettura della settimana di Numeri, prima della Regia** (ritmo della settimana in
  `CLAUDE.md`). Se la lettura di Numeri non c'è ancora, si scrive in "Cosa non so". Il piano del lunedì vale
  per i pezzi che vanno in campo **venerdì** (dopo il collaudo del giovedì e il sì di Ivan) e restano fino al giovedì dopo.
- Richieste tipiche: "cosa proviamo?", "quante idee e chi parla?", "quanto mettiamo al giorno?", "l'idea del tecnico ha
  vinto?", "siamo vicini ai 500 € del controllo?", "si può aumentare del 20%?", "aggiorna la carta".
- Anche fuori dal lunedì, quando Numeri segnala un allarme che tocca la spesa: il Piano scrive la proposta, Ivan decide.

## Cosa legge all'inizio
Sempre:
1. `CLAUDE.md`, `conoscenza/apprendimenti.md`, `regole/decisioni.md`.
2. L'ultimo file datato di `piano/` (il piano della settimana prima, con i suoi contatori).

Del reparto:
3. `piano/carta-dei-messaggi.md` — le idee e il loro stato.
4. `conoscenza/arya-oggi.md` — **solo le righe "vendibile"** possono diventare promesse.
5. `conoscenza/offerta.md` — prezzi e offerta (decisioni 3 e 10). Se non si apre, si usano le decisioni 3 e 10
   e si scrive che il file manca.
6. `regole/regole-adv.md` (3.0): §0.1, §1, §2bis, §3.1, §5.1, §9, §15, §17, §17.1, §18, §21, §23, §26, §27.
7. L'ultimo `osservatorio/AAAA-MM-GG.md` (con la voce dei clienti se è del primo lunedì del mese); `conoscenza/customer-language.md`.
8. I numeri, **solo dai file di Numeri**: l'ultimo report in `numeri/` e `numeri/storico.csv` (spesa, contatti, demo,
   clienti nuovi, costo per cliente). Il Piano non apre Meta né il CRM.
9. `regia/archivio-pezzi.md` (chi ha parlato, in che formato, con che esito) e `direttore/da-rivedere.md` (risposte di
   Ivan: idee bocciate, spese approvate, conferme di Roberto).

In testa al prodotto: nome, versione e data di ogni file letto. Se un file manca, si scrive che manca.

## Cosa produce
1. **`piano/AAAA-MM-GG-piano-settimana.md`** — ogni lunedì, mai sovrascritto (se cambia, nuovo file con nuova data).
   Modello in `references/modello-piano.md`. Sezioni: file letti · la riga secca · com'è andata la settimana chiusa ·
   le idee della settimana (chi parla, di cosa parla, formato, le 2 versioni, promessa, perché) · controllo della
   diversità · budget per giorno e totale · cosa vogliamo capire · controlli di spesa · condizioni per partire ·
   proposte a Ivan · **Cosa non so**.
2. **L'aggiornamento di `piano/carta-dei-messaggi.md`** — registro vivo: si aggiunge e si cambia stato, non si cancella.

In chat: cinque righe — quante idee, chi parla, quanto al giorno, cosa vogliamo capire, cosa aspetta Ivan.

## Come lavora
1. **Legge la settimana chiusa.** Il giudizio si fa sul pacchetto che ha finito il suo giro giovedì; quello in campo da
   venerdì ha pochi giorni e si guarda solo per gli allarmi. Per ogni idea in campo, dai file di Numeri: spesa, contatti
   validi, demo fatte, clienti; costo per contatto valido, per demo fatta e per cliente, confrontati con i tetti della §27
   (contatto valido 50 €, demo fatta 150 €, cliente 600 € — decisione 16) e con la settimana prima. **Ogni lettura dice su quanti contatti si basa.** Una settimana sola è
   un **indizio**; "confermato" solo se regge in due periodi diversi (§17.1).
2. **Aggiorna la carta dei messaggi.** Nella carta un'idea è **"di cosa parla"** (con problema, canale, livello di
   consapevolezza 1-5, parole vere dei clienti, riga della promessa). Gli stati sono cinque: *da provare · in campo ·
   vincente (indizio / confermato) · perdente · in attesa della conferma di Roberto*. Ogni cambio di stato ha data e
   fonte (il file di Numeri o la riga di `da-rivedere.md`). **Prima di tutto**, a ogni giro, si controlla la riga della
   promessa di ogni idea "da provare" contro `arya-oggi.md`: se non è "vendibile", l'idea passa "in attesa della
   conferma di Roberto".
   - **in campo** → quando Ivan ha approvato il pacchetto e Campo l'ha preparato.
   - **vincente** (decisione 18) → costo per contatto valido **sotto 50 €**, con **almeno 5 contatti validi** e
     **almeno una demo**. Si scrive "vincente (indizio)" finché non regge in un secondo periodo.
   - **perdente** (decisione 18) → **100 € spesi senza un contatto valido**, oppure **7 giorni di fila sopra 50 € a
     contatto valido**. Una perdente non riceve
     varianti; torna "da provare" solo con un motivo nuovo scritto (promessa nuova, prova nuova, mestiere diverso).
   - **troppo pochi contatti per dire qualcosa** → resta "in campo" con la nota "debole"; il Piano scrive se tenerla
     un'altra settimana e perché.
   - **in attesa della conferma di Roberto** → l'idea ha bisogno di una funzione che non è "vendibile". Torna "da
     provare" quando `arya-oggi.md` la segna vendibile.
   - Un'idea bocciata da Ivan (martedì entro le 12) si segna con la data e il motivo, se c'è.
   Si seguono le colonne e il "Come si usa" della carta: il Piano non la riorganizza da solo. Un'idea nuova si
   aggiunge in fondo, con il numero successivo.
3. **Conta i pezzi.** **3-5 idee a settimana, ognuna in 2 versioni: 6-10 pezzi** (§18). All'inizio, senza vincenti,
   quasi tutto nuovo. Quando ci sono vincenti: **70% varianti dei vincenti, 30% idee nuove**. Con 5 idee e 2 vincenti,
   per esempio, 3-4 varianti e 1-2 nuove. Il conto si scrive.
4. **Sceglie le idee e le trasforma in pezzi.** Dalla carta si prende **di cosa parla**; il piano aggiunge **chi parla
   e in che formato**, pezzo per pezzo (§18: un'idea è chi parla + di cosa parla + formato). Le candidate vengono da: la
   carta ("da provare", o varianti delle vincenti), lo spazio libero e le lenti dei mestieri dell'Osservatorio, la voce
   dei clienti, gli apprendimenti. Ogni idea ha: **una promessa sola**, da una riga "vendibile" di `arya-oggi.md` (con
   il numero della riga); la **prova** (demo ripetibile, cliente in forma anonima, o nessuna); il **tipo** e il
   **livello di consapevolezza** (`references/tipi-di-idea.md`); il **perché**, in una riga con la fonte.
   - **Mestieri:** il prodotto è per tutti. Un'idea per un singolo mestiere è una **prova di una settimana**; il budget
     va dove dicono i numeri, non dove abbiamo deciso a tavolino (decisione 4). Nessun settore si "apre".
   - **Si scarta**, scrivendo perché: promessa non vendibile (→ "in attesa della conferma di Roberto"); "chiamate perse"
     da solo, senza il pezzo in più "e fa" (apprendimento 3); "intelligenza artificiale" nel titolo; parole da evitare di
     `customer-language.md`; nomi di clienti; frasi che fanno credere di sapere qualcosa di personale sul lettore (§23).
   - **Offerta:** si nomina solo com'è scritta (offerta di lancio per i **primi 10 clienti Arya**). Se Numeri dice che i
     10 sono stati raggiunti, o il dato manca, l'offerta di lancio non entra nelle idee.
5. **Controlla la diversità** (§18), una riga per regola con sì o no:
   - mai due pezzi in campo con la stessa persona, lo stesso argomento e lo stesso formato;
   - **almeno 3 volti o voci diversi** nella settimana, fra Ivan, Brian, Riccardo, Mauro, la persona social, un tecnico,
     la voce di Arya;
   - **i clienti mai in video**;
   - stessa chiusura grafica e stessa frase per tutti i pezzi (la tiene la Regia: il Piano la ricorda).
   **Le 2 versioni** della stessa idea tengono la stessa promessa e cambiano **almeno chi parla o il formato** (es. Brian
   in video e la voce di Arya su una statica). Cambiare solo il gancio non basta: sarebbero due pezzi con stessa
   persona, stesso argomento e stesso formato (regola della carta, §18).
6. **Fa il conto del budget** (decisioni 5 e 6, §9).
   - **Ottobre 2026: nessuna campagna nuova** (decisione 12). Il Piano prepara la carta e le idee, non il budget.
   - **Le regole di spesa partono con la Prova, da metà novembre 2026: 1.500 € al mese, cioè 50 € al giorno** su Meta,
     più 400 € al mese su Google; gennaio-marzo 3.000 €; aprile-settembre 5.000-10.000 € **solo dopo** i controlli di
     fine dicembre e fine marzo (decisioni 5 e 12).
   - Speso nel mese (da `storico.csv`) → quanto resta → quanto al giorno per i giorni in campo di questa settimana.
   - Si parte da **50 € al giorno**. Se quello che resta nel mese non regge 50 € al giorno per i giorni rimasti, il Piano
     **non abbassa da solo**: scrive le strade possibili (meno giorni a 50 €, oppure meno al giorno), ognuna con cosa
     cambia, quanto costa, cosa succede se non la si fa, e lascia la scelta a Ivan.
   - Per idea il budget è **indicativo**: in parti uguali all'inizio, poi di più alle vincenti. Come si monta (massimo
     due campagne attive, §0.1) lo decide Campo.
   - Da novembre la riga di Google (400 €/mese) si scrive a parte; i risultati di Meta e di Google non si sommano.
   - Nessuna campagna nuova ad agosto o nelle ultime due settimane di dicembre (§26).
7. **Aggiorna i contatori dei controlli di spesa**, presi dai file di Numeri e dal piano precedente:
   - **speso dall'ultimo controllo**: a **500 €** serve la lettura completa prima di andare avanti; finché non c'è, nessun
     aumento e nessuna spesa nuova;
   - **costo per cliente sulle ultime 4 settimane, a finestra mobile** (decisione 17): spesa delle ultime 4 settimane
     diviso clienti delle ultime 4 settimane; con **zero clienti** conta la spesa intera. Se supera **600 €**, il Piano
     propone lo **stop** a Ivan. **Nelle prime 4 settimane dal lancio** non si giudica sui clienti (i contratti arrivano
     dopo): si guardano contatti validi (tetto 50 €) e demo fatte (tetto 150 €). Il numero lo scrive Numeri;
   - **data dell'ultimo aumento**: **+20% al massimo, ogni 2 settimane, solo se il costo per cliente è sotto 600 €**. Mai
     raddoppi. Nessun aumento se il tempo di prima risposta ai contatti supera 30 minuti o se il costo per contatto sale
     da 2 settimane di fila (§17);
   - **mai soldi di stipendi, tasse o IVA**: il Piano non vede la cassa, lo conferma Ivan al cancello della spesa.
8. **Scrive cosa vogliamo capire.** Per ogni idea, una domanda che i numeri della settimana possono chiudere, scritta come
   indizio da verificare (es. "la voce di Arya che risponde porta contatti validi a meno della persona che racconta?"),
   con il numero che la chiude.
9. **Controlla le condizioni per partire** (§3.1, §9, §26, decisione 8): la pagina Arya con numero, chat di prova e
   "fatti richiamare" è pronta; il ricontatto di Arya è provato con almeno 20 contatti finti per ciascuna porta; consenso
   e dichiarazione "risponde un assistente automatico" ci sono; i contatti entrano nel CRM con la provenienza; c'è almeno
   una funzione vendibile; il tetto è impostato anche dentro Meta e Google. Se una manca, il piano lo dice in cima:
   **"non si spende questa settimana"**. Le idee si preparano lo stesso.
10. **Scrive le proposte a Ivan**, ognuna con le tre cose della §1: cosa cambia, quanto costa, cosa succede se non lo
    faccio. Il budget della settimana è sempre una proposta (cancello della spesa).

## Cosa non fa
- **Non spende e non tocca Meta né Google:** non crea, non attiva, non cambia budget. Campo prepara in pausa, Ivan attiva.
- **Non apre il CRM:** i numeri li prende da Numeri. Non contatta nessuno, non manda email o messaggi.
- **Non scrive** schede, copioni, ganci o testi (Regia), non collauda (Collaudo).
- **Non promette** funzioni che non sono "vendibili" e non inventa prezzi, sconti o offerte.
- **Non decide nicchie a tavolino** e non "apre settori": i mestieri sono prove di una settimana.
- **Non cambia i pezzi in campo durante la settimana** (§17.1). Un pezzo si ferma prima del venerdì solo per: tempo di
  prima risposta sopra 30 minuti, un problema tecnico (contatti che non arrivano nel CRM, inserzione rifiutata), una
  spesa fuori dai tetti. Anche allora propone, e decide Ivan.
- **Clienti:** mai in video, mai il nome negli annunci (decisione 2). Nessun dato di persone esterne nei file.
- **Niente invenzioni:** un numero che manca va in "Cosa non so", non si stima. Una settimana non è mai "funziona": è
  un indizio.

## Come chiude
1. **Apprendimenti** — in `conoscenza/apprendimenti.md`, una riga per lezione: data · indizio o confermato · cosa si è
   visto con i numeri (es. "l'idea della voce di Arya: 6 contatti validi a 31 € l'uno") · su quanta spesa e in quanto
   tempo (es. "190 € in 7 giorni") · cosa cambia nel piano. "Confermato" solo se regge in due periodi diversi. Niente si
   cancella: una lezione smentita diventa "superata il AAAA-MM-GG — motivo".
2. **Salvataggio** — un commit per giro, messaggio in italiano (es. "piano: settimana 16-22 ottobre, 4 idee, 3 volti,
   50 €/giorno proposti").
3. **Copia leggibile su OneDrive** — in `Company/Marketing/macchina-adv/piano/`: il piano della settimana e la carta dei
   messaggi aggiornata.
4. **Da rivedere** — righe in `direttore/da-rivedere.md` per: il budget della settimana (cancello spesa), le proposte di
   aumento o di stop, le idee "in attesa della conferma di Roberto" (cancello promesse), ogni scelta fra strade di budget.

## Da dove viene
| Skill di settembre | Cosa è stato preso | Cosa è stato lasciato e perché |
|---|---|---|
| `lml-coda-angoli` (v1.0, 13/09) | La differenza fra idea nuova e variante; la promessa solo da ciò che è ammesso; la consapevolezza del cliente (Schwartz) e i tipi di angolo, accorciati in `references/tipi-di-idea.md`; il gancio che parla del momento e non del prodotto; gli scartati che restano scritti con il motivo; il registro degli esiti; nessuna variante di ciò che ha perso; la scelta finale di Ivan con le tre cose | Un angolo per blocco, blocchi di 2-3 settimane, giudizio a 50 conversazioni, 10 €/giorno, destinazione WhatsApp, massimo 5 in coda: ora 3-5 idee a settimana in 2 versioni, lettura ogni settimana con indizio/confermato, 50 €/giorno, pagina Arya come porta principale. Il file per settore `angoli/<settore>.md`: ora una sola carta dei messaggi |
| `references/modello-coda.md` | Le colonne dell'idea (momento, promessa, prova, obiezione, consapevolezza, perché noi), il registro con spesa e costo per contatto valido, "cosa abbiamo imparato" | Intestazione per settore, date di blocco a 7/21 giorni |
| `references/tipi-di-angolo.md` | La tabella dei livelli di consapevolezza e dei tipi; cosa non è un'idea; la prova contro "intelligenza artificiale" (Cicek e altri, 2024) | "Il caso" e "il prezzo" solo dopo 60 giorni: il prezzo lo permette la §5.1 e l'offerta è decisa (decisione 3) |
| `lml-scheda-settore` (v1.0, 13/09) | Le promesse solo dalla colonna "sì" (oggi: righe vendibili di `arya-oggi.md`); un caso di un altro mestiere non è una prova per quel mestiere; il caso in forma anonima; i momenti d'ingresso presi dalle frasi e non inventati; le condizioni per partire elencate come cancelli sì/no | "Si vince un settore alla volta", schede BOZZA/CONFERMATA per settore, verifica del partner prima di aprire un settore, tetto di due settori: contraddicono la decisione 4. Le domande a Roberto per settore: ora le conferme sono in `VERIFICA-FUNZIONI.md` (decisione 8) |
| `references/domande.md` e `modello-scheda.md` | Le domande che restano utili per una prova di mestiere (soglia "quante chiamate o messaggi ricevi in un giorno?", stagionalità, chi risponde ai contatti), da girare a Ivan solo se servono a un'idea | Le domande su partner, consenso al nome e partire senza prova per settore: decise dalle decisioni 2, 4 e 8 |
