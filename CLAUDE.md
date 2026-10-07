# CLAUDE.md — regole permanenti della macchina pubblicitaria di Arya

Valgono per ogni sessione e ogni automazione. Si cambiano solo con il sì di Ivan.

## Chi siamo
LML Technologies S.r.l. (Bitritto, Bari). Vendiamo **Arya**, assistente AI per il servizio clienti:
- **ARYA Voice** — telefono;
- **Arya Customer Care** — chat e WhatsApp;
- **a-Mail** — email.
Clienti: chiunque gestisca un servizio clienti o un'assistenza di primo livello.

## Obiettivo
Entro settembre 2027: **120-150 clienti paganti** e **15.000-20.000 € al mese di canoni**.

## Le decisioni in vigore (date e fonti in `regole/decisioni.md`; la 8, funzioni vendibili, e la 9, dati personali, sono più sotto)
1. Tetto di spesa per un cliente nuovo: **600 €** (7/10/2026).
2. Nomi dei clienti: **mai negli annunci**; sì sul sito e nei casi studio, con la clausola di referenza del contratto.
3. Listino: contratto di 24 mesi con recesso libero a 60 giorni, attivazione a pagamento (fino a 3 rate). Offerta di lancio
   per i **primi 10 clienti Arya**: prova gratuita di 15 giorni prima della firma e attivazione inclusa; contratto sempre
   24 mesi con recesso a 60 giorni. Si rivede al controllo di fine dicembre.
4. Nessuna nicchia decisa a tavolino, il prodotto è per tutti: i messaggi per singolo mestiere sono **prove di una settimana**; il budget va dove dicono i numeri.
5. Budget: ottobre 300-400 €/mese; novembre-dicembre 1.500 €/mese su Meta + 400 € su Google; gennaio-marzo 3.000 €/mese; aprile-settembre 5.000-10.000 €/mese **solo dopo** i controlli di fine dicembre e fine marzo.
6. Regole di spesa: partenza 50 €/giorno; controllo a 500 € spesi; stop se un cliente costa più di 600 € per 4 settimane di fila; +20% ogni 2 settimane solo sotto i 600 €; **mai** soldi di stipendi, tasse o IVA.
7. Tre cancelli umani: **promesse ammesse, pacchetto della settimana, spesa**. Claude propone, Ivan approva.

## Come si descrive Arya
- Arya si descrive **solo** con `conoscenza/arya-oggi.md`. Niente funzioni prese da altre fonti o dalla memoria.
- Negli annunci entrano **solo le funzioni "vendibili"** della scheda. "Da confermare", "in arrivo" e "non si promette" restano fuori.
- **"Vendibile"** solo se funziona oggi per un cliente vero o in una demo che si ripete uguale, **e Roberto lo conferma per
  iscritto** (lo stato lo decidono Roberto e Fabio, Ivan approva). Senza conferma nessuna funzione è vendibile e niente va
  negli annunci. Le conferme si raccolgono in OneDrive `macchina-adv/novita-arya/VERIFICA-FUNZIONI.md`.
- Le novità (arrivano in OneDrive `Company/Marketing/macchina-adv/novita-arya/`) diventano promesse **solo dopo il sì di Ivan**; allora si aggiorna la scheda, con data e fonte.

## I reparti
Ognuno ha la sua cartella e scrive file datati.
| Reparto | Cartella | Cosa fa |
|---|---|---|
| Osservatorio | `osservatorio/` | guarda il mercato: concorrenti (Libreria inserzioni), voce dei clienti, novità di Arya |
| Piano | `piano/` | decide cosa provare la settimana dopo e con quanto budget, dentro le decisioni 4-6 |
| Regia creativa | `regia/` | scrive copioni, testi e tavole; tiene `regia/archivio-pezzi.md` |
| Collaudo | `collaudo/` | controlla ogni pezzo contro regole, scheda di Arya e linguaggio dei clienti, prima di Ivan |
| Messa in campo | `campo/` | prepara le campagne su Meta **in pausa**, solo dopo il sì di Ivan |
| Numeri e conversione | `numeri/` | legge i risultati (sola lettura), aggiorna `numeri/storico.csv`, segue contatti → demo → clienti |
| Direttore | `direttore/` | tiene insieme i reparti, scrive il riepilogo, mette in `direttore/da-rivedere.md` ciò che deve decidere Ivan |

Le skill dei reparti sono in `.claude/skills/` (mappa in `.claude/skills/catena-adv.md`). Ne mancano tre della catena
(`lml-direttore-adv`, `collaudo-testi-adv`, `meta-scrittura-sicura`): non sono su OneDrive. Finché mancano, valgono le regole di questo file.
I testi delle automazioni stanno in `prompt/`. Il lavoro di settembre 2026 è in `archivio-lml-adv/`
(solo da leggere: è storia, non regola; dove contraddice questo file, vale questo file).

## Regole di sicurezza
- **Meta:** nelle automazioni solo lettura. Creazioni solo **in pausa** e solo dopo il sì di Ivan. **Mai attivare, mai cambiare budget.**
- **Dati personali:** i nomi dei colleghi LML, nel loro ruolo, possono stare nell'archivio. Nomi, telefoni o email di
  persone esterne (clienti, contatti, fornitori) **mai**. L'archivio contatti (`Archivio-contatti-LML.xlsx`) non si copia.
  Se un file contiene dati di persone esterne, si salta e si segnala. STATO-progetto-adv.md, scaletta-configurazione-adv.md
  e product-marketing.md di settembre restano solo su OneDrive.
- **OneDrive:** i file originali non si modificano. Si scrive solo in `Company/Marketing/macchina-adv/`.
- **Comunicazioni:** non si mandano email o messaggi a nessuno.
- **Niente invenzioni:** se qualcosa non si legge o non si copia, si scrive cosa manca.
- **Soldi:** nessuna spesa fuori dalle decisioni 5 e 6.

## La regola della memoria
La macchina **non ricorda niente** fra un giro e l'altro. Quindi ogni sessione e ogni automazione:
1. **All'inizio legge**: `conoscenza/apprendimenti.md`, `regole/decisioni.md` e **l'ultimo file del proprio reparto**
   (più `conoscenza/arya-oggi.md` se scrive o controlla testi).
2. **Alla fine scrive** cosa ha imparato in `conoscenza/apprendimenti.md` (una riga per lezione: data,
   indizio o confermato, cosa abbiamo visto con i numeri, su quanta spesa e in quanto tempo, cosa cambia)
   e lo salva nell'archivio.
3. **Niente si cancella.** Una lezione smentita diventa "superata" con motivo e data; una decisione
   cambiata resta in `regole/decisioni.md` segnata "superata".
4. "Confermato" vuol dire numeri sufficienti (vedi regole di spesa); sotto, è un "indizio".

## Come si salva il lavoro
1. **Un file datato per ogni prodotto**: `<cartella-reparto>/AAAA-MM-GG-argomento.md`. Non si sovrascrive un file
   già salvato: se cambia, nuovo file con nuova data.
2. **Un salvataggio con messaggio chiaro**: un commit per lavoro, messaggio in italiano che dice cosa e perché
   (es. "numeri: settimana 12-18 ottobre, costo per cliente 540 €").
3. **Una copia leggibile su OneDrive**: in `Company/Marketing/macchina-adv/` (report dei reparti; ogni lunedì
   la copia di `conoscenza/apprendimenti.md`).
4. Le modifiche a `CLAUDE.md`, `regole/` e `conoscenza/arya-oggi.md` passano da una richiesta di unione
   (pull request) che unisce Ivan.

## Lingua e tono
Italiano semplice, frasi corte, parole dei clienti (vedi `conoscenza/customer-language.md` e `conoscenza/glossario.md`).
