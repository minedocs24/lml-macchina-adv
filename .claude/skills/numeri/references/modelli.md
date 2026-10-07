# Modelli del reparto Numeri — semaforo e lettura della settimana

Solo conteggi e ID. Mai nomi, telefoni, email o aziende di persone esterne.

---

## 1. Semaforo — `numeri/AAAA-MM-GG-semaforo.md`

Si scrive **solo** se c'è almeno un allarme.

```
# Semaforo — AAAA-MM-GG

Letto: Meta alle [ora] · Google [alle ora / non collegato] · CRM alle [ora]
File: CLAUDE.md [data] · decisioni.md [data] · regole-adv.md 3.0 [data] · collegamento-crm.md [data]

## [n] allarmi, dal più urgente

**[ALLARME]** [cosa] · [numero] · soglia [soglia, fonte] · proposta: [una riga] · decide: Ivan, cancello [spesa/altro]

## Controllato e a posto
[una riga sola]

## Cosa non so
- …
```

---

## 2. Lettura della settimana — `numeri/AAAA-MM-GG-settimana.md`

```
# Numeri — settimana dal AAAA-MM-GG al AAAA-MM-GG

Letto: Meta [data e ora] · Google [data e ora / non collegato] · CRM [data e ora]
File: [elenco con versione e data]
CRM leggibile: sì / **no → la lettura si ferma alla spesa e lo dice qui**

## 1. La riga secca
[Una frase: bene o male, e perché. Numero: costo per cliente (o per demo e contatto valido finché non ci sono clienti).]

## 2. I numeri — fronte prodotti Arya
*(consulenza e personal brand: righe separate sotto, mai sommate)*

| | Questa settimana | Settimana prima | Riferimento | Nota |
|---|---|---|---|---|
| Spesa Meta | | | piano della settimana; 50 €/giorno (dec. 6) | |
| Spesa Google | | | 400 €/mese da novembre (dec. 5) | |
| Spesa del mese finora | | | budget del mese (dec. 5) | |
| Spesa dall'ultimo controllo | | | 500 € (dec. 6) | contatore del Piano + spesa della settimana |
| Contatti — pagina Arya: chiamata / chat / fatti richiamare | | | | |
| Contatti — modulo Meta | | | | |
| Organici · senza provenienza | | | senza provenienza: sotto il 10% | |
| Contatti validi (quota) | | | almeno 40% (§17) | su [n] contatti |
| Costo per contatto valido | | | tetto 50 € (§27) | |
| Demo fissate · fatte | | | | il tetto vale per le demo fatte |
| Costo per demo fatta | | | tetto 150 € (dec. 16) | |
| Clienti nuovi | | | contatto → cliente 2-4% (§2) | |
| Costo per cliente (settimana · ultime 4 settimane) | | | tetto 600 € (dec. 1) | |
| Costo per cliente sulle ultime 4 settimane (finestra mobile; zero clienti = spesa intera) | | | stop sopra 600 € (dec. 17); nelle prime 4 settimane dal lancio si guardano contatti validi e demo fatte | il Piano usa questo numero |
| Canoni mensili in essere | | | obiettivo 15.000-20.000 € a settembre 2027 | |
| Tempo medio di prima risposta | | | 5 minuti (§11); soglia 30 (§17) | |
| Frequenza massima | | | sotto 3 (§17) | |

*Sotto le 10 unità: numeri interi, non percentuali.*

**Per idea e per pezzo**

| Idea | Pezzo | ID inserzione | Spesa | Impression | Contatti | Validi | Demo | Costo per contatto | Lettura |
|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | Indizio: … |

**Righe per l'archivio pezzi** (le riporta la Regia in `regia/archivio-pezzi.md`)

| Argomento | Chi parla | Formato | Gancio (prime parole) | Date (dal–al) | Numeri | Esito |
|---|---|---|---|---|---|---|
| | | | | | spesa · impression · contatti · costo per contatto | indizio: vince / pari / perde |

**Fronte consulenza:** [una riga, o "nessuna attività"] · **Fronte personal brand:** [una riga, o "nessuna attività"]

## 3. Cosa è cambiato
| Cosa | Di quanto | Spiegazione più probabile (ipotesi) | Indizio o confermato | Su quanti contatti |
|---|---|---|---|---|

## 4. Le proposte
**[P1] [cosa]** — Cosa cambia: … · Quanto costa: … · Cosa succede se non lo faccio: … · Decide: Ivan, cancello …
*(Le proposte di budget — stop, aumento, spostamenti — le scrive il Piano. Qui solo se le condizioni ci sono, e le altre proposte.)*

## 5. Cosa non so
- …
```

Solo il primo lunedì del mese, prima di "Cosa non so": **Controlli del mese** (clienti persi §28, "come ci hai conosciuto"
per tema §13, contatti Meta contro CRM, budget del mese nuovo). Nell'ultima lettura di dicembre e di marzo:
**Per il controllo di fine dicembre / fine marzo** (numeri dalla partenza).

---

## 3. Diagnosi — dove si rompe

| Cosa si vede | Dove è il problema | Cosa si propone |
|---|---|---|
| Pochi si fermano sul pezzo | prima immagine o primo fotogramma (§18) | nuova apertura, stessa idea |
| Si fermano ma abbandonano subito | le prime parole (§18) | nuovo gancio |
| Guardano ma non cliccano | la promessa è debole (§18) | idea diversa |
| Cliccano ma non lasciano i dati | la pagina, non il pezzo (§18) | non rifare il video: guardare la pagina |
| Tanti contatti, meno del 40% validi | messaggio o pubblico (§17); guardare i motivi di scarto | stringere testo o pubblico |
| Tanti validi, poche demo | il problema è dopo: ricontatto o agenda | non è il pezzo |
| Buono, poi peggiora con frequenza sopra 3 | pezzo consumato | varianti della stessa idea |
| Costo per contatto scende, costo per contatto valido sale | Meta impara a portare le persone sbagliate | proporre il ritorno dei contatti buoni (con il sì di Ivan) |
