# lml-macchina-adv

La macchina pubblicitaria di LML Technologies per **Arya** (telefono, chat e WhatsApp, email).
Questo archivio è l'unico posto in cui la macchina tiene regole, conoscenza, skill, stato e storico.

## Da dove partire
| Se vuoi… | Guarda |
|---|---|
| le regole che valgono sempre e il ritmo della settimana | `CLAUDE.md` |
| le decisioni in vigore (budget, tetti, offerta, prezzi) | `regole/decisioni.md` |
| le regole pubblicitarie complete (3.1) | `regole/regole-adv.md` |
| cosa Arya fa oggi e cosa si può promettere | `conoscenza/arya-oggi.md` |
| prezzi, condizioni e offerta di lancio | `conoscenza/offerta.md` (specchio di `elenco_promozioni` del CRM) |
| cosa abbiamo imparato finora | `conoscenza/apprendimenti.md` |
| le idee da provare | `piano/carta-dei-messaggi.md` |
| il modello della scheda di un reel o post | `regia/MODELLO-SCHEDA.md` |
| come si leggono i contatti dal CRM | `conoscenza/crm-statistiche.md` (connettore «LML CRM · Statistiche»; `numeri/collegamento-crm.md` è superato) |
| indirizzo della pagina degli annunci | `CLAUDE.md`, sezione "Impostazioni" |
| cosa deve decidere Ivan | `direttore/da-rivedere.md` |
| i numeri settimana per settimana | `numeri/storico.csv` |
| ogni reel o post pubblicato e com'è andato | `regia/archivio-pezzi.md` |

## Le cartelle
- `regole/` — decisioni in vigore e superate, regole pubblicitarie 3.1.
- `conoscenza/` — scheda di Arya, offerta, apprendimenti, linguaggio dei clienti (`customer-language.md`), glossario.
- `osservatorio/`, `piano/`, `regia/`, `collaudo/`, `campo/`, `numeri/` — un reparto ciascuno, file datati.
- `direttore/` — riepiloghi e coda delle cose da rivedere.
- `consegne/` — solo il `LEGGIMI.md` per la persona social: i pezzi finiti stanno su OneDrive in `macchina-adv/consegne/<id-scheda>/`.
- `prompt/` — i testi delle automazioni in cloud: `direttore.md` (feriali alle 8), `osservatorio.md` (lunedì alle 7) e
  `numeri.md` (ogni giorno alle 7:30, dal lancio).
- `.claude/skills/` — una skill per reparto (`osservatorio`, `piano`, `regia`, `collaudo`, `campo`, `numeri`, `direttore`),
  `organico` (testo dei post organici, per Campo) e `meta-scrittura-sicura`, che usa Campo. Le 13 skill di settembre e la mappa `catena-adv.md` sono in `.claude/skills/archivio/`.
- `archivio-lml-adv/` — il lavoro di settembre 2026 da `Company/Marketing/lml-adv/`, copiato così com'era. Si legge, non si modifica.

## Copia leggibile
In OneDrive, `Company/Marketing/macchina-adv/`: i report da leggere e ogni lunedì gli apprendimenti.
- `consegne/<id-scheda>/` — i pezzi finiti caricati da chi gira e, accanto, l'esito del Collaudo.
- `novita-arya/` — le novità di Arya (`MODELLO-NOTA.md`) e le conferme delle funzioni (`VERIFICA-FUNZIONI.md`).
- `fondamenta/` — copia di `CLAUDE.md`, `regole/decisioni.md` e `conoscenza/arya-oggi.md`, per rileggerli dalla chat.
- `cervello/` — copia di `regole-adv.md` 3.0, `carta-dei-messaggi.md`, `MODELLO-SCHEDA.md`, `offerta.md`, `collegamento-crm.md`.

## Cosa NON è stato copiato da `lml-adv` (7/10/2026), e perché
| File | Motivo |
|---|---|
| `STATO-progetto-adv.md` | contiene nomi e cognomi di persone esterne (accessi Meta) |
| `scaletta-configurazione-adv.md` | contiene nomi e cognomi di persone esterne e un'email personale |
| `.agents/product-marketing.md` (anche in `conoscenza/`) | contiene nomi di persone esterne (sezione testimonianze). La scheda di Arya è stata comunque ricavata dal file letto su OneDrive |
| `Archivio-contatti-LML.xlsx` e copie | dati personali dei contatti: non si copia mai |
| tutti i `.bak`, `numeri/`, `Claude outputs/`, `storico-minedocs/` | esclusi per istruzione |
| `CLAUDE.md`, `fase-*.md`, `RIEPILOGO-*.md`, `prompt-edge-*.md`, `.mcp.json`, `.claude/`, `montaggi/` (vuota) di `lml-adv` | non richiesti in questa fase |

Decisione di Ivan (7/10/2026): STATO-progetto-adv.md, scaletta-configurazione-adv.md e product-marketing.md **restano solo su OneDrive**.
Regola: i nomi dei colleghi LML, nel loro ruolo, possono stare nell'archivio; quelli di persone esterne mai.
