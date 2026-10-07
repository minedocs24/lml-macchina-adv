---
name: lml-scheda-settore
description: Costruisce la scheda settore di LML Technologies per un target ARYA (o per la consulenza) unendo il radar inserzioni, la voce del settore e quello che LML sa di sé — cosa fa davvero ARYA in quel settore, quali prove esistono, se c'è un partner, chi è il cliente giusto, quali momenti d'ingresso presidiare — e dice se il settore è pronto per le inserzioni o cosa manca. Usa SEMPRE questa skill quando l'utente chiede "prepariamo il settore X", "la scheda del settore", "siamo pronti per i rivenditori?", "cosa sappiamo di questo settore", "che promesse possiamo fare a…", "apriamo un settore nuovo", oppure quando radar e voce di un settore sono entrambi fatti e va deciso se procedere — anche se non nomina la skill e dice solo "mettiamo insieme quello che abbiamo sui dentisti". È il terzo anello della catena pubblicitaria LML: dopo radar e voce, prima della coda degli angoli. Si ferma dove serve una risposta di Ivan o di Roberto.
---

# Scheda settore — quello che sappiamo, quello che possiamo promettere

**Versione 1.0 — 13 settembre 2026.** Solo lettura e scrittura di file nella cartella di lavoro. Non tocca Meta. Non completa mai una scheda da sola: dove serve una risposta di una persona, si ferma e la chiede.

## A cosa serve, in una riga

Il radar dice cosa fanno gli altri. La voce dice cosa dicono i clienti. **Questa scheda dice cosa possiamo dire noi**, e se possiamo dirlo adesso. È il punto in cui il mercato incontra le prove che abbiamo davvero — e dove la §0.1 di regole-adv smette di essere un principio e diventa un elenco di caselle piene o vuote.

Il principio che la regge viene dalla letteratura sul software verticale: **si vince un settore alla volta, in profondità.** La credibilità in un settore si guadagna con un cliente di quel settore raccontabile, con la lingua di quel settore, e con i canali che quel settore già usa — associazioni, fornitori che ci sono già dentro. Un secondo settore si apre solo quando il primo produce risultati ripetibili.

## Prima di cominciare — leggi sempre

1. `regole-adv.md`: §0.1 (si parte da zero), §2bis (momenti d'ingresso), §4.2 (target prodotti), §5.1 (il messaggio), §10.1 (contatto valido), §21 (casi studio), §22.1 (partner prima della pubblicità), §23 (cosa non si dice), §26 (cosa non facciamo).
2. `.agents/product-marketing.md`: tutto. In particolare "Differentiation", "Proof Points", "Objections", i casi reali.
3. `.agents/glossario.md`: cosa fanno i connettori, le fasce, cosa si dice al cliente.
4. `radar/<settore>/` — l'ultimo radar. **Se non c'è, fermati:** la scheda non si fa senza radar.
5. `voce/<settore>/` — l'ultima scheda voce. **Se non c'è, fermati.**
6. La scheda settore precedente, se esiste: `settori/<settore>.md`.

Dichiara versione e data di ogni file letto.

## Cosa entra e cosa esce

**Entra:** il settore; radar e voce di quel settore; le risposte alle domande in `references/domande.md` (se già date in una sessione precedente, stanno nella scheda precedente).

**Esce:** `settori/<settore>.md` — **un file solo per settore**, che si aggiorna, con lo storico delle modifiche in fondo. A differenza di radar e voce, che sono fotografie datate, la scheda settore è lo stato attuale: c'è una risposta sola alla domanda "possiamo promettere X?".

La scheda ha **due stati**, scritti in cima:
- **BOZZA** — ci sono domande aperte. Non si passa alla coda degli angoli.
- **CONFERMATA il <data>** — tutte le domande hanno risposta. Le skill successive la possono usare.

---

## Passo 1 — Il cliente giusto in questo settore

Dalla §4.2 e §10.1, specializzate sul settore. Compila:

- **Dimensione:** da quanti a quanti addetti. Il target prodotti dice 5-50; alcuni settori stanno sotto (molti B&B hanno meno di 5 addetti): dirlo, e dire cosa si fa.
- **Chi decide e chi risponde oggi al telefono/chat:** spesso la stessa persona. Chi subisce (il front office) e cosa teme.
- **Il segnale d'acquisto:** non l'interesse per l'AI, ma il volume. **La domanda che qualifica** resta una: *"quante chiamate o messaggi ricevi in un giorno?"* Scrivere qual è la soglia sotto cui, in questo settore, ARYA non serve.
- **La stagionalità del settore**, se c'è (ricettività: estate; studi medici: settembre e gennaio; e-commerce: novembre-dicembre). Serve alla §15 per decidere quando partire.
- **A chi non vendere** in questo settore.

## Passo 2 — I momenti d'ingresso, classificati

Il metodo è quello dell'Ehrenberg-Bass (Romaniuk, "How Brands Grow Part 2"): si elencano le situazioni in cui il titolare pensa al problema, e poi si ordinano. Per elencarle si usano le sette domande, dette le "7 W":

| Domanda | Esempio nel settore rivenditori |
|---|---|
| **Perché** pensa al problema | ha perso un ordine perché non ha risposto |
| **Quando** | il lunedì mattina, con dieci chiamate perse dal sabato |
| **Dove** | in magazzino, con le mani occupate |
| **Mentre** fa cos'altro | serve un cliente al banco e il telefono squilla |
| **Con o per chi** | il socio che gli dice "non rispondiamo mai" |
| **Con che altro** | il gestionale che non parla col telefono |
| **Come si sente** | in colpa verso il cliente che ha richiamato tre volte |

Le situazioni **non si inventano al tavolo**: si prendono dalla scheda voce (casella "Momento" e "Dolore") e dal radar (i momenti che i concorrenti nominano). Ogni momento cita la frase che lo sostiene.

Poi si ordinano su **due criteri**, ed è questo che fa la differenza:

1. **Quanto è frequente** — quante frasi della voce lo nominano.
2. **Chi lo presidia già** — quanti concorrenti del radar ci hanno costruito sopra un'inserzione sopravvissuta.

| | Nessuno lo presidia | Lo presidiano in 1-2 | Lo presidiano in 3+ |
|---|---|---|---|
| **Frequente** | **Il posto migliore.** Spazio libero su un momento vero | Buono, si entra col "e fa" | Lingua già imparata: si usa, ma non basta a distinguerci |
| **Raro** | Nicchia: forse in un secondo momento | Lasciare | Lasciare |

Prima di ordinare, una scrematura sola: **togliere i momenti in cui ARYA non è credibile**. Se il momento è "il cliente vuole parlare con il titolare in persona", non è un momento nostro. Romaniuk la chiama la prima C, credibilità: si toglie prima ancora di contare.

## Passo 3 — Cosa fa ARYA in questo settore, oggi

**È il passo che nessuna ricerca può fare da sola: la risposta è di Roberto.** Le domande stanno in `references/domande.md`. In sintesi:

- Quali azioni ARYA fa **davvero, oggi, in produzione** per un'attività di questo settore: risponde, prende l'appuntamento, controlla lo stato dell'ordine, guarda la disponibilità, riconosce il cliente, passa a una persona?
- Con quali programmi del settore esiste **già** un collegamento, e con quali va costruito.
- Cosa **non fa ancora** e non va promesso.

Da qui esce la tabella più importante della scheda:

| Promessa | Si può fare oggi? | Con quale prova | Dove sta il limite |
|---|---|---|---|
| "risponde anche quando il negozio è chiuso" | sì | Mr. Toner in produzione | — |
| "ti mette l'ordine nel gestionale" | dipende dal gestionale | Mr. Toner (Zoho) | solo con collegamento esistente o costruito |
| "fissa l'appuntamento in agenda" | [risposta di Roberto] | | |

**Regola (§23, EU AI Act): quello che non sta nella colonna "sì" non entra in nessuna inserzione.** Nemmeno come "presto".

## Passo 4 — Le prove che abbiamo

Per ogni prova, quattro campi:

| Prova | Tipo | Stato del consenso | Numeri disponibili |
|---|---|---|---|
| Mr. Toner | cliente in produzione, stesso settore | da chiedere / chiesto il … / ottenuto il … / negato | i cinque numeri della product-marketing: [quali ci sono] |
| MineDocs | nostro negozio, non un cliente | — | [se ARYA ci gira sopra] |
| demo con voce vera | registrazione | — | tempo di risposta misurato: [sì/no] |

Regole:
- **Il nome del cliente solo con consenso scritto** (§21). Senza, il caso si racconta in forma anonima e va scritto così già qui: "un rivenditore di consumabili in Puglia, dieci persone".
- **Un caso di un settore diverso non è una prova per questo settore.** Si può citare come "abbiamo già fatto", non come "abbiamo già fatto per uno come te". La scheda lo marca.
- **Un numero si usa solo se è misurato e se continua a essere misurato** (il tempo di risposta di ARYA, product-marketing "Proof Points").
- **Se non c'è nessuna prova del settore**, la scheda lo dice in cima, in grassetto, e l'unica strada per le inserzioni è **mostrare il prodotto che funziona**, senza racconti di clienti.

## Passo 5 — Il partner, prima della pubblicità

§22.1 e §26 sono chiare: non si apre un settore su Meta senza aver controllato se esiste un fornitore che ha già dentro quei clienti. La scheda risponde a tre domande, e la risposta è di Ivan:

1. C'è un partner con parco clienti installato in questo settore? (gestionale di settore, fornitore di registratori di cassa, distributore, associazione)
2. È stato chiesto ai partner dell'accordo quadro se servono questo settore?
3. Se il partner c'è: Meta serve solo come supporto. Se non c'è: Meta a pieno regime. Quale dei due?

Finché la domanda 2 non ha risposta, la scheda resta BOZZA.

## Passo 6 — I concorrenti e le alternative

Dal radar, riassunte in una tabella corta: chi sono, cosa promettono (la promessa più ripetuta fra le sopravvissute), cosa regalano (prova gratuita, demo), e **dove cascano** rispetto a noi (product-marketing "Dove cascano": vendono il centralino non il risultato, scaricano la configurazione sul cliente, non agiscono nel gestionale).

Poi le **alternative che sembrano ragionevoli** in questo settore — la persona part-time, la segreteria esterna, il risponditore a tasti, la risposta automatica di WhatsApp — con la frase che le smonta, presa dalla voce se c'è.

## Passo 7 — Le obiezioni di questo settore

Dalla casella "Dubbio" della voce, non dalla lista generica. Per ognuna: la frase esatta del cliente, la risposta di LML (product-marketing "Objections"), e se la risposta **regge in questo settore** o va cambiata.

Un'obiezione della voce che non ha risposta in nessun materiale LML va in "Da segnalare".

## Passo 8 — Il formato, per questo settore

Tre righe di numeri, non un'opinione:
- dal radar: fra le inserzioni sopravvissute del settore, quante video, quante immagini, quante con una faccia;
- da noi: quali risorse esistono già (registrazione della voce di ARYA, video di Ivan, tavole);
- la scelta di partenza, con il motivo, e **la nota che la decide la spesa, non la scheda** (regole-adv §18: la creatività pesa metà del risultato, e si giudica sui numeri).

## Passo 9 — I cancelli

La scheda chiude con l'elenco delle condizioni per aprire il settore su Meta, ognuna con sì/no:

| Condizione | Stato |
|---|---|
| Radar fatto da meno di 30 giorni | |
| Voce fatta | |
| Cosa fa ARYA nel settore: confermato da Roberto | |
| Almeno una prova del settore, o decisione esplicita di partire senza | |
| Partner verificato (§22.1) | |
| Il settore è nella §10.1 di regole-adv come contatto valido (altrimenti serve una modifica approvata) | |
| Chi risponde ai contatti e in quanto tempo (§11) | |
| Un secondo settore è già aperto? (§0.1: massimo due campagne attive) | |

Se tutte le caselle sono "sì": **CONFERMATA**. Altrimenti resta **BOZZA**, con l'elenco di cosa manca e di chi deve rispondere.

---

## Regole vincolanti

1. **Non si completa mai una scheda inventando le risposte di Roberto o di Ivan.** Le caselle che dipendono da loro restano con `[DA CHIEDERE A …]` finché non rispondono. È la regola delle sezioni `[DA DEFINIRE]` di regole-adv, applicata qui.
2. **Non si promette quello che ARYA non fa oggi.** La colonna "sì" del Passo 3 è l'unico serbatoio di promesse per tutte le skill successive.
3. **Un caso di un altro settore non è una prova.** Si marca.
4. **Nome del cliente solo con consenso scritto.** Senza, forma anonima già scritta.
5. **Nessun angolo scelto.** La scheda classifica i momenti e dice quali sono liberi; la scelta è della coda degli angoli.
6. **Nessun testo di inserzione.** Nemmeno un esempio.
7. **Un file per settore, aggiornato, con lo storico in fondo.** Non si sovrascrive senza lasciare traccia di cosa è cambiato e quando.
8. **Se radar o voce mancano, non si procede.** Una scheda fatta senza è un'opinione.

## Cadenza

Si costruisce **una volta** per aprire il settore. Si riapre **ogni volta che cambia una risposta**: un consenso arriva, ARYA impara a fare una cosa nuova, un partner si trova, un radar nuovo sposta un momento d'ingresso da "nessuno lo presidia" a "tre lo presidiano". L'attività di chiusura del mese controlla se i cancelli sono ancora tutti "sì".

## Dove si scrive

```
settori/
  rivenditori.md
  e-commerce.md
  ...
```

Da Cowork si scrive direttamente. Dalla chat del progetto si consegna il file. Vale la regola della cartella: file di appoggio, rilettura, copia sul file buono.

## Cosa fa dopo, e chi

Con la scheda **CONFERMATA**, la **coda degli angoli** prende i momenti nel quadrante "frequente e libero", li incrocia con la colonna "sì" delle promesse e con le prove, e produce gli angoli in ordine. Il **pacchetto inserzione** prende dalla scheda la forma anonima del caso, la soglia di qualificazione e il formato di partenza. Il **collaudo** usa la colonna "sì" per bocciare ogni promessa che non ci sta.

Va segnalato subito in chat, non solo nella scheda: un momento d'ingresso frequente che nessuno presidia; una promessa dei concorrenti che noi non possiamo fare; un'obiezione senza risposta nei materiali LML; un settore che non passa i cancelli per una sola casella.
