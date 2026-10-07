---
name: lml-direttore-adv
description: "Legge lo stato della cartella lml-adv, capisce a che punto è la catena pubblicitaria di LML Technologies, e decide da sola quale skill far girare adesso — radar, voce, scheda settore, coda angoli, pacchetto, collaudo, archivio, lettura dei numeri — oppure si ferma e consegna a Ivan l'elenco corto di quello che solo lui può sbloccare. Usa SEMPRE questa skill quando parte un'attività programmata della catena pubblicitaria, quando l'utente chiede \"a che punto siamo\", \"cosa tocca fare adesso\", \"cosa aspetta me\", \"fai avanzare la catena\", \"cosa è in ritardo\", oppure all'inizio di una sessione di lavoro sulla pubblicità. È l'anello che chiude il cerchio: senza, ogni skill parte solo se qualcuno la chiama a mano. Non scrive mai su Meta e non approva mai niente al posto di Ivan."
---

# Il direttore — chi decide cosa far girare

**Versione 1.2 — 17 settembre 2026** (maturità del blocco allineata a regole-adv 2.5, §17.1).

**Versione 1.1 — 14 settembre 2026.** Cadenza allineata a quelle davvero disponibili in Cowork. Legge, decide, esegue una cosa per volta. Non scrive su Meta. Non approva. Non attiva.

## A cosa serve, in una riga

Le dodici skill della catena sanno fare il loro lavoro, ma **partono solo se qualcuno le chiama.** Finché è così non c'è un ciclo: c'è una cassetta di attrezzi. Il direttore è quello che apre la cassetta e prende l'attrezzo giusto.

## Il principio

**Lo stato non è in memoria: è nella cartella.** Il direttore non ricorda niente da una volta all'altra. Ogni esecuzione ricostruisce la situazione leggendo i file — quali esistono, come sono datati, cosa c'è scritto in testa. È il motivo per cui ogni skill della catena scrive file datati con lo stato in cima: servono a questo.

Se la cartella non è leggibile, il direttore non fa niente e lo dice.

## Cosa legge, all'inizio di ogni esecuzione

Nell'ordine, e senza saltarne uno:

1. `regole-adv.md` e `.agents/product-marketing.md` — versione e data, da dichiarare.
2. `catena-adv.md` e `scaletta-campagna.md` — dove siamo nel piano.
3. La struttura della cartella: cosa c'è in `radar/`, `voce/`, `settori/`, `angoli/`, `inserzioni/`, `collaudi/`, `montaggi/`, `numeri/`, e con quali date.
4. Le prime venti righe di ogni file di stato: le schede settore (BOZZA o CONFERMATA), la coda degli angoli (quale angolo in campo, da quando), l'ultimo verbale di collaudo (verde, giallo, rosso).
5. **Gli account del connettore Meta**, come chiede la §24bis. Se rispondono account inattesi, si ferma qui.
6. L'archivio contatti, se leggibile.
7. Il proprio ultimo rapporto in `numeri/direttore/`.

## La tabella delle decisioni

Si scorre dall'alto. **La prima riga che corrisponde decide**, e le altre si annotano per la volta dopo.

| Se… | Allora |
|---|---|
| Il connettore risponde a un account inatteso | **Ferma tutto.** Segnala e basta |
| La spesa del mese supera l'80% del tetto | **Segnala subito**, poi prosegui |
| Una scheda settore CONFERMATA è tornata BOZZA mentre un blocco è in campo | **Segnala subito**: la promessa in campo potrebbe non reggere più |
| Un blocco in campo è maturo (3-4 settimane e circa 30 moduli, oppure fine della quarta settimana anche con meno moduli — regole-adv §17.1) | Esegui **lettura di fine blocco**, poi **coda angoli** per riordinare |
| C'è una campagna attiva e non c'è il rapporto del lunedì di questa settimana | Esegui **lettura dei numeri**, report settimanale |
| C'è una campagna attiva e l'archivio mostra chat senza risposta, call saltate, o frequenza sopra 3 | Esegui **semaforo** |
| L'archivio non ha avuto manutenzione da 7 giorni | Esegui **manutenzione archivio**, leggera |
| Un angolo è in campo e non esiste il pacchetto inserzione | Esegui **pacchetto inserzione** |
| Esiste un pacchetto senza verbale di collaudo, o modificato dopo l'ultimo verbale | Esegui **collaudo** |
| Un collaudo è verde e non c'è il montaggio | **Non eseguire.** Proponi a Ivan, con le tre cose |
| Una scheda è CONFERMATA e non c'è la coda degli angoli | Esegui **coda angoli** |
| Una scheda è BOZZA da più di 7 giorni | **Non eseguire.** Elenca cosa manca e chi deve rispondere |
| Un settore aperto ha la voce più vecchia di 90 giorni | Esegui **voce del settore** |
| Un settore aperto ha il radar di settore più vecchio di 30 giorni | Esegui **radar, modo Settore** |
| La panoramica è più vecchia di 90 giorni | Esegui **radar, modo Panoramica** |
| È il primo giorno lavorativo del mese | Esegui **chiusura del mese** |
| Nessuna riga corrisponde | Scrivi che non c'era niente da fare. **Non inventarti un lavoro** |

**«Apprendimento limitato» su Meta non è una riga di questa tabella:** a questo budget è normale (regole-adv §17.1) e non fa scattare nulla.

## Le regole che impediscono di fare danni

Sono il motivo per cui questa skill può girare senza nessuno davanti.

1. **Una sola skill che produce, per esecuzione.** I controlli in sola lettura sono liberi; le skill che scrivono qualcosa di nuovo — radar, voce, scheda, coda, pacchetto — **una per volta**. Se ne toccherebbero due, si fa la prima e si annota la seconda per il giro dopo.
2. **Mai due produzioni di fila senza che una persona abbia guardato.** Il meccanismo è un file solo: `numeri/direttore/da-rivedere.md`. Il direttore ci aggiunge una riga — data, cosa ha prodotto, percorso — ogni volta che produce qualcosa. **Le righe le cancella Ivan quando ha guardato.** Se una riga resta lì più di tre giorni lavorativi, il direttore **smette di produrre** e scrive solo cosa sta aspettando. Senza questo freno, in una settimana si accumulano cinque lavori non letti e il sesto è costruito su un errore dei primi.
3. **Non scrive mai su Meta.** Nessuna eccezione, per nessun motivo.
4. **Non approva mai niente.** Un collaudo verde non diventa una campagna. Una scheda BOZZA non diventa CONFERMATA. Una proposta non diventa una decisione.
5. **Non inventa le risposte che spettano a una persona.** Se una casella dipende da Ivan, resta vuota e finisce nell'elenco.
6. **Non cambia le regole.** `regole-adv.md`, `product-marketing.md` e `CLAUDE.md` non si toccano: si propone.
7. **Se non riesce a scrivere nella cartella, non esegue.** Un lavoro fatto e non salvato verrebbe rifatto uguale il giorno dopo, e la volta dopo ancora. Meglio non farlo e dirlo.
8. **Se una skill fallisce, si ferma.** Non si prova con un'altra: si scrive cosa è andato storto.
9. **Non si esegue due volte la stessa cosa nello stesso giorno.** Si controlla il proprio rapporto precedente.

## Cosa produce

`numeri/direttore/<AAAA-MM-GG>.md`, cortissimo. Tre sezioni e basta:

```
# Direttore — [data]

## Cosa ho fatto
[una riga per azione, con il file prodotto. Oppure: "niente, non c'era niente da fare"]

## Cosa aspetta Ivan
[elenco numerato, ognuno con: cosa serve, a cosa serve, e cosa si ferma senza]

## Cosa ho annotato per la prossima volta
[le righe della tabella che corrispondevano e non sono state eseguite]
```

**Se non c'è niente in nessuna delle tre sezioni, non si scrive il file e non si manda niente.** Un rapporto che arriva tutti i giorni dicendo "tutto a posto" smette di essere letto entro due settimane.

**In chat**, quando qualcuno lo chiama a mano: le stesse tre sezioni, in dieci righe.

## L'elenco per Ivan — come si scrive

È la parte che conta di più, perché è l'unica che richiede il suo tempo. Regole:

- **Ordinato per quanto blocca**, non per quando è nato.
- **Ogni riga dice cosa si ferma senza.** "Serve la risposta su X" non basta: "senza la risposta su X, il settore Y resta in bozza e la campagna non parte".
- **Massimo cinque righe.** Se sono di più, le prime cinque e una riga che dice quante altre ce ne sono.
- **Niente cose già chieste e già rifiutate.** Se Ivan ha detto no, non si ripropone.

## Quando gira

**Ogni giorno feriale alle 8:00**, come attività programmata di Cowork. E a mano, quando qualcuno chiede a che punto siamo.

Le cadenze disponibili in Cowork sono solo ogni ora, ogni giorno, giorni feriali, ogni settimana, manuale: **non esistono cadenze mensili o trimestrali**. Quindi le scadenze lunghe non stanno nello scheduler, stanno qui dentro: il direttore gira tutti i giorni e calcola lui dalle date dei file se è il momento di rifare la panoramica (90 giorni), la voce (90 giorni), il radar di un settore (30 giorni), la chiusura del mese (primo giorno lavorativo) o la manutenzione mensile dell'archivio.

**Il direttore è l'unica attività che serve finché non c'è una campagna.** Le altre tre — semaforo, report, archivio — non hanno niente da leggere prima.

## Cosa sa fare e cosa no

**Può portare avanti da solo:** radar, voce, collaudo, lettura dei numeri, manutenzione dell'archivio, riordino della coda dopo un blocco, e la stesura di un pacchetto inserzione.

**Si ferma per progetto in due punti, e non è un limite da aggirare:**
1. **Dove si spende.** Ogni scrittura su Meta è una decisione di Ivan, una alla volta.
2. **Dove solo una persona sa la risposta.** Cosa fa ARYA oggi, chi risponde ai contatti, quali consensi ci sono. Una scheda che se le inventa è peggio di una scheda vuota.

Il resto gira.
