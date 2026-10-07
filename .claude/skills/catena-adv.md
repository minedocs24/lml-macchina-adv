# La catena pubblicitaria LML — mappa e chiusura

**Versione 1.0 — 13 settembre 2026.** Da tenere nella radice di `lml-adv`. È la mappa che tiene insieme le dodici skill: chi legge cosa, chi scrive cosa, e cosa gira da solo.

## Il perimetro

Dal mercato al contatto raccolto. **Si ferma alla call fissata.** Tutto quello che viene dopo — la call, il preventivo, il ricontatto di chi ha detto "non ora", il caso studio — è fuori da questa catena e si costruisce in un secondo momento.

## Le dodici skill, in ordine di uso

| # | Skill | Legge | Scrive | Stato |
|---|---|---|---|---|
| 1 | `lml-radar-inserzioni` | Libreria Inserzioni | `radar/<settore>/<data>.md`, `pagine.md` | creata |
| 2 | `lml-voce-del-settore` | recensioni, forum, fonti nostre | `voce/<settore>/<data>.md` | creata |
| 3 | `lml-scheda-settore` | radar, voce, product-marketing, **risposte di Ivan e Roberto** | `settori/<settore>.md` (BOZZA → CONFERMATA) | creata |
| 4 | `lml-coda-angoli` | scheda CONFERMATA, esiti dei blocchi | `angoli/<settore>.md` | creata |
| 5 | `lml-pacchetto-inserzione` | angolo in campo, voce, customer-language | `inserzioni/<settore>/<blocco>.md` | creata |
| 6 | `lml-copione-video-adv` | brief del pacchetto | `inserzioni/<settore>/<blocco>-<C>-copione.md` | duplicata da `lml-copione-video` |
| 7 | `lml-tavole-adv` | brief del pacchetto | immagini in `inserzioni/<settore>/` | duplicata da `lml-tavole-social` |
| 8 | `lml-montaggio-video` | copione | video montato | **esistente, invariata** |
| 9 | `lml-collaudo-creativita` | pacchetto, scheda, angolo | `collaudi/<settore>/<blocco>-<data>.md` | creata — richiama `collaudo-testi-adv` |
| 10 | `lml-montaggio-campagna` | pacchetto collaudato, **sì di Ivan** | entità su Meta **in pausa**, `montaggi/<settore>/<blocco>-<data>.md` | creata — si appoggia a `meta-scrittura-sicura` |
| 11 | `lml-archivio-contatti` | primo messaggio WhatsApp, chat, call | l'archivio (OneDrive, accesso limitato) | creata |
| 12 | `lml-lettura-numeri-adv` | Meta (sola lettura), archivio | `numeri/semaforo/`, `numeri/settimana/`, `numeri/blocchi/` | creata |

**Il cerchio si chiude alla 12:** la lettura di fine blocco torna nella coda (4), che riordina, e il pacchetto (5) riparte.

## Le tre skill che esistevano e non sono state toccate

- `lml-montaggio-video` — si usa com'è.
- `collaudo-testi-adv` e `meta-scrittura-sicura` — installate dal lato Cowork, **non leggibili dalla chat**. Le skill 9 e 10 le richiamano invece di rifarle. **Alla prima sessione da Cowork:** leggerle, e togliere dalle 9 e 10 i doppioni.

## La cartella `lml-adv`, dopo la catena

```
lml-adv/
  CLAUDE.md · regole-adv.md · scaletta-ambiente-adv.md · catena-adv.md (questo file)
  .agents/   product-marketing.md · customer-language.md · glossario.md
  radar/     <settore>/pagine.md · <data>.md
  voce/      <settore>/<data>.md
  settori/   <settore>.md
  angoli/    <settore>.md
  inserzioni/<settore>/<blocco>.md · -copione.md · immagini
  collaudi/  <settore>/<blocco>-<data>.md
  montaggi/  <settore>/<blocco>-<data>.md
  numeri/    semaforo/ · settimana/ · blocchi/
  [archivio contatti: cartella separata ad accesso limitato]
```

## Le attività programmate

Tutte in sola lettura su Meta. Scrivono solo file nuovi. Girano da Cowork, che lavora sulla cartella.

| Attività | Quando | Skill | Parla solo se… |
|---|---|---|---|
| Semaforo | ogni mattina lavorativa | 12 | c'è un allarme |
| Report | lunedì | 12 | sempre |
| Fine blocco | quando il blocco matura (7 giorni + 50 conversazioni, o 21 giorni) | 12 → 4 | sempre |
| Osservatorio concorrenti | ogni mese sui settori aperti, ogni tre sugli altri | 1 | sempre; **subito** se un concorrente usa il nostro messaggio |
| Voce | ogni tre mesi sui settori aperti | 2 | sempre |
| Manutenzione archivio | settimanale leggera, mensile completa | 11 | c'è qualcosa da sistemare |
| Chiusura del mese | primo giorno lavorativo | 12 (§32) | sempre |

**L'attività già attiva** ("Osservatorio concorrenti e bandi", lunedì alle 8) va allineata alla skill 1: stessa cosa, ma con il metodo dei tre livelli e il file datato.

## I cancelli — dove la catena si ferma da sola

1. **Scheda settore BOZZA** → la coda non parte.
2. **Collaudo rosso** → niente produzione, niente montaggio.
3. **Collaudo giallo** → decide Ivan.
4. **Nessun sì esplicito di Ivan** → niente scrittura su Meta.
5. **Connettore su un account inatteso** → il montaggio si ferma.
6. **Nessuno che risponde ai contatti** → niente attivazione.
7. **Terza campagna attiva** → no.
8. **Meno di 7 giorni pieni e 50 conversazioni** → nessun giudizio sull'angolo.

## Cosa si è verificato in chiusura, con fonti

Cercando negli studi accademici e nelle norme se mancava qualcosa, sono emerse **quattro integrazioni**, già applicate alle skill:

| Cosa | Dove | Fonte |
|---|---|---|
| **La prima risposta di ARYA deve dichiarare che risponde una macchina**, al primo contatto | pacchetto (5), collaudo (9) | Regolamento UE 2024/1689, art. 50, in vigore dal 2 agosto 2026; legge italiana 132/2025. Sanzioni fino a 15 milioni o al 3% del fatturato |
| **La parola "intelligenza artificiale" nell'inserzione abbassa fiducia e intenzione d'acquisto**, di più per acquisti percepiti come rischiosi | pacchetto (5), tipi di angolo (4) | Cicek, Gursoy, Lu, *Journal of Hospitality Marketing & Management* 34(1), 2024, sei esperimenti, oltre mille persone. Conferma scientifica di `customer-language.md` |
| **I 5 minuti di risposta hanno una base solida**: 100 volte più probabile raggiungere la persona, 21 volte più probabile qualificarla, rispetto ai 30 minuti | archivio (11), lettura (12) | Oldroyd, MIT Sloan con InsideSales, 2007; Oldroyd, McElheran, Elkington, *Harvard Business Review*, 2011 |
| **Una prova a voce su cinque titolari** prima di spendere, facoltativa, per passare da giallo a verde | collaudo (9) | Pratica qualitativa consolidata; non prova nulla in senso statistico, scopre l'equivoco grosso |

**La distinzione che tiene insieme le prime due:** dichiarare la macchina **nella chat** è un obbligo; scrivere "AI" **nell'inserzione** è una scelta, e le prove dicono di non farla. Non sono in contraddizione: nella chat il cliente ha già scelto di parlare con noi, nell'inserzione non ci conosce ancora.

## Cosa NON manca, e perché

Verificato contro la letteratura e contro le regole. Cose che potevano sembrare buchi e non lo sono:

- **Pagina di destinazione:** non serve, la destinazione è WhatsApp (§26). Quando servirà, si aprirà un pixel nuovo in due minuti.
- **Pubblici caldi e ricontatto:** non prima di 60 giorni (§0.1). Sarà una skill futura, quando esisterà qualcuno da ricontattare.
- **Rotazione delle creatività:** è dentro la 4 (varianti) e la 12 (frequenza sopra 3, tabella "dove si rompe"). Non serve una skill a parte.
- **Aumenti di budget:** regola già scritta (§17: 20-30% ogni 3-4 giorni, mai raddoppi). La 12 propone, Ivan decide, la 10 esegue.
- **Consenso e privacy:** informativa nel primo messaggio (§12), consenso come campo (11), scadenza dei dati scritta nell'archivio (11), frasi della voce sempre anonime (2).
- **Il conflitto fra la skill del linguaggio LML e customer-language:** segnalato all'inizio, e ora con una prova in più (Cicek 2024) a favore della lingua del cliente nelle inserzioni. Va scritta una riga in `lml-tech-content-system` — **con il sì di Ivan**, perché è una skill esistente.

## Quello che viene dopo, fuori da questa catena

Da costruire quando ci sarà materia:

- **Coltivazione di chi ha detto "non ora"** — la skill `email-sequence` del pacchetto marketing è una base; va adattata a WhatsApp e ai messaggi pre-approvati (§12).
- **Pubblici caldi** — dopo 60 giorni di dati.
- **Caso studio** — appena Mr. Toner ha un mese di numeri e il consenso scritto (§21).
- **Guida e ascolto della call** — le domande della §30 e la lettura delle registrazioni.
- **Preventivo ARYA** — `lml-preventivi` vale solo per i progetti.

## Cosa serve per dire "aperto", non solo "chiuso"

La catena è completa sulla carta. Per partire davvero, in ordine:

1. La scaletta dell'ambiente (fasi 1-4), per avere un account su cui montare.
2. Il radar e la voce sul settore rivenditori.
3. Le risposte di Roberto e di Ivan per la scheda settore — **compresa la prova che il pacchetto della provenienza arriva e viene salvato** (skill 11).
4. L'approvazione dell'app da parte di Meta, e le 20 conversazioni di prova.
5. Il conto del bersaglio: quanto vale un cliente, quante call servono, quanto possiamo pagare una conversazione (skill 12).

Il primo blocco misura, non giudica. Il secondo comincia a insegnare.
