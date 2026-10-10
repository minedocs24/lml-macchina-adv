# Modelli del reparto Numeri — semaforo e lettura della settimana

Solo conteggi e ID. Mai nomi, telefoni, email o aziende di persone esterne.
Il CRM si legge con «LML CRM · Statistiche» (`numeri_pubblicita`), guida in `conoscenza/crm-statistiche.md`.

---

## 1. Il file del giorno — `numeri/AAAA-MM-GG.md` (dal 10/10/2026, decisione 29; prima `-semaforo.md`)

Con spesa in corso ogni giorno; senza spesa **solo** se c'è almeno un allarme.

```
# Numeri del giorno — AAAA-MM-GG (dati di ieri, AAAA-MM-GG)

Letto: Meta alle [ora] · Google: report nella posta di Ivan delle [ora] / non arrivato · CRM alle [ora] · pagina alle [ora]
File: CLAUDE.md [data] · decisioni.md [data] · regole-adv.md 3.0 [data] · crm-statistiche.md [data] · file del giorno di [ieri], [l'altro ieri]
Notifica a Ivan: sì ([testo]) / no

## Allarmi con notifica (N1-N6), dal più urgente
**[N2 — PAGINA NON RAGGIUNGIBILE]** [codice, ora delle due prove] · soglia: 2xx e "Arya" nella pagina · proposta: [una riga] · decide: Ivan, cancello spesa
*(se nessuno: "Nessuno")*

## Altri allarmi (senza notifica)
**[ALLARME]** [cosa] · [numero] · soglia [soglia, fonte] · proposta: [una riga] · decide: Ivan, cancello [spesa/altro]

## Il giorno, per campagna e inserzione (fronte prodotti Arya)
| Canale | Campagna (ID) | Inserzione (ID · id scheda) | Spesa ieri | Impression | Clic sul link | Frequenza 7 g | Clic 7 g / 7 g prima | Contatti | Validi | Non verificati | € per contatto valido, 7 g |
|---|---|---|---|---|---|---|---|---|---|---|---|

Tetti: contatto valido 50 € · demo fatta 150 € · cliente 600 € (decisione 16). Doppio del tetto (N5): 100 € a contatto valido.
Giorni di fila sopra 100 € per campagna: [ID: n giorni] (da questo file e dai due prima).

## Controllato e a posto
[una riga sola]

## Cosa non so
- …
```

---

## 2. Lettura della settimana — `numeri/AAAA-MM-GG-settimana.md`

```
# Numeri — settimana dal AAAA-MM-GG al AAAA-MM-GG

Letto: Meta [data e ora] · Google [data e ora / non collegato] · CRM «LML CRM · Statistiche» [data e ora]
Età della settimana: letta il lunedì dopo [sì / no → perché]
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
| Contatti non verificati (anti-bot), a parte | | | — | mai sommati ai contatti |
| Arrivi (CRM) contro contatti di Meta e Google | | | devono tornare | se non tornano, di quanto |
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

**Per canale e per campagna** (da `numeri_pubblicita`, `raggruppa` = canale e campagna; cumulative dopo "contatti")

| Canale o campagna (ID) | Contatti | Arrivi | Contattati | Validi | Demo fissate | Demo fatte | Prove | Clienti | Canoni nati (€) | Prima risposta (min) |
|---|---|---|---|---|---|---|---|---|---|---|

**Promozioni** (blocco promozioni; occupano un posto solo le prove in corso e i clienti)

| Codice | Posti | Prove avviate | In corso | Clienti | Perse | Posti rimasti | Allarme (meno di 3) |
|---|---|---|---|---|---|---|---|

**Le 3 settimane prima, rilette oggi** (per vederle maturare; le righe di `storico.csv` non si toccano)

| Settimana | Letta il lunedì dopo: contatti · validi · demo fatte · clienti | Oggi: contatti · validi · demo fatte · clienti |
|---|---|---|

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
