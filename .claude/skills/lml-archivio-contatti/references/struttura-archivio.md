# La struttura dell'archivio

Una tabella sola. Un contatto per riga. Su OneDrive, in una cartella ad accesso limitato.

Se si usa Zoho o un altro gestionale, i nomi dei campi cambiano ma **l'elenco no**: sono i campi minimi senza i quali un contatto non si può contare.

## Le colonne

### Arrivano da sole, dal primo messaggio

| Colonna | Tipo | Note |
|---|---|---|
| `id` | testo | progressivo |
| `data_ora` | data e ora | del primo messaggio |
| `telefono` | testo | dato personale |
| `codice_clic` | testo | serve **solo** al ritorno a Meta |
| `id_inserzione` | testo | |
| `blocco` | testo | es. `B1-lunedi-mattina` |
| `angolo` | testo | |
| `titolo_visto` | testo | il titolo dell'inserzione |
| `provenienza` | elenco | `inserzione` / `organico` |

### Si raccolgono parlando

| Colonna | Tipo | Note |
|---|---|---|
| `nome` | testo | |
| `azienda` | testo | |
| `settore` | elenco | gli otto target + `altro` |
| `volume_giorno` | numero | chiamate o messaggi al giorno |
| `ruolo` | elenco | `titolare` / `direzione` / `dipendente` / `non so` |
| `cosa_vorrebbe` | testo | |
| `consenso_ricontatto` | sì/no | §12 |

### Si aggiungono dopo

| Colonna | Tipo | Note |
|---|---|---|
| `stato` | elenco | i nove stati |
| `data_stato` | data | del cambio più recente |
| `motivo` | elenco | obbligatorio con `scartato` e `perso` |
| `data_call` | data e ora | |
| `esito_call` | testo | |
| `come_ci_hai_conosciuto` | testo libero | raccolto **in call** (§13) |
| `prossimo_ricontatto` | data | obbligatorio con `non ora` |
| `minuti_prima_risposta` | numero | |
| `note` | testo | |

## Gli stati

`nuovo` · `in lavorazione` · `scartato` · `valido` · `call fissata` · `call fatta` · `non ora` · `attivazione` · `perso`

## I motivi

Lista chiusa. Se serve un motivo nuovo, si aggiunge alla lista, non si scrive a mano nelle note.

**Scarto:** `volume troppo basso` · `settore fuori` · `non è il titolare` · `cercava altro` · `è un fornitore` · `studente o privato` · `nessuna risposta` · `numero non valido`

**Perso dopo la call:** `prezzo` · `tempi` · `ha scelto un concorrente` · `rimandato senza data` · `non risponde più` · `non serviva davvero`

## Chi mette cosa

| Passaggio | Chi |
|---|---|
| nuovo | automatico |
| in lavorazione, scartato, valido, call fissata | chi risponde in chat |
| call fatta, non ora, perso | chi fa la call |
| attivazione | Ivan |

## In testa al file

Due righe fisse, che si leggono prima di tutto:

```
Archivio contatti pubblicitari LML — accesso limitato a: [nomi]
Dati conservati fino a: [regola decisa da Ivan con chi segue la privacy, il <data>]
```

## Il foglio di riepilogo

Un secondo foglio, che si calcola da solo. Una riga per blocco.

| Blocco | Chat | Validi | Call fissate | Call fatte | Attivazioni | Organici | Senza provenienza |
|---|---|---|---|---|---|---|---|

Da qui la lettura dei numeri ricava il costo per contatto valido e per call fissata. **Il costo non sta qui:** la spesa la legge da Meta, e il conto lo fa quella skill.

## Cosa NON va nell'archivio

- Il contenuto delle conversazioni. Restano dove stanno; qui va il riassunto.
- Frasi dei clienti con nome e azienda attaccati: quelle vanno nella scheda voce, **anonime**.
- Contatti che non vengono dalla pubblicità né da un canale che stiamo misurando, salvo marcarli chiaramente.
- Il codice del clic usato per qualcosa che non sia il ritorno a Meta.
