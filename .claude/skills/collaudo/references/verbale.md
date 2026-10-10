# Modello — Verbale di collaudo

File: `collaudo/AAAA-MM-GG-settimana.md` (tutti i pezzi) oppure `collaudo/AAAA-MM-GG-<pezzo>.md` (uno solo o ricollaudo).
Ogni ricollaudo è un file nuovo. Mai nomi, numeri o email di persone esterne in questo file.

---

# Collaudo — settimana [dal … al …] · [data]

## Esito della settimana
**In una riga:** [es. "7 verdi, 2 gialli da decidere, 1 rosso: promessa non vendibile nel video di Mauro"]

| Pezzo (scheda) | Chi parla · argomento · formato | Esito | Gravi | Medi | Lievi |
|---|---|---|---|---|---|
| regia/[data]-[titolo].md · versione A | | VERDE / GIALLO / ROSSO | | | |

**Collaudo precedente:** [file, oppure "primo"] · **Momento:** primo collaudo / ricollaudo dopo correzioni

## Fonti lette
CLAUDE.md del [ ] · regole/decisioni.md del [ ] · regole-adv.md v[ ] del [ ] · arya-oggi.md del [ ] (ultima riga del
registro: [ ]) · elenco_promozioni letto il [ ] alle [ ] (listino [codice], promozioni [codici]) / **non letto** · offerta.md del [ ] ·
pagina degli annunci da CLAUDE.md: [indirizzo] · customer-language.md v[ ] · glossario.md v[ ] · campo/[ultimo verbale] ·
regia/archivio-pezzi.md del [ ]

---

## [Pezzo] — ESITO: [VERDE / GIALLO / ROSSO]

**Consegna** (`macchina-adv/consegne/<id-scheda>/`, versione letta: [v1 / v2…]):
| File | C'è? | Esito | Nota |
|---|---|---|---|
| pezzo (video / immagine) | | | |
| testo-post.txt | | | |
| trascrizione.txt | | | senza: GIALLO con la richiesta |
| primo-fotogramma.jpg | | | |
| sottotitoli.srt (se esportati) | | | senza: lieve, "Cosa non so" |
| Arya parla? prima frase con "assistente virtuale/automatico" | | | se manca: ROSSO |

Esito accanto al pezzo scritto in `consegne/<id-scheda>/collaudo-AAAA-MM-GG.md`: [sì / no → perché]

| # | Controllo | Esito | Nota |
|---|---|---|---|
| 1 | Promesse (solo righe vendibili) | | |
| 2 | Offerta (prezzi e promozioni in vigore in elenco_promozioni) | | |
| 3 | Nomi e persone (clienti mai, dati esterni mai) | | |
| 4 | Meta e legali (attributi personali, dichiarazione dell'assistente automatico, consenso, coerenza con la porta) | | |
| 5 | Lingua (test della recensione, parole vietate) | | |
| 6 | Diversità e firma (chiusura e frase uguali) | | |
| 7 | Misure (125 / 40 / 27, durata, gancio, sottotitoli, zone) | | |
| 8 | Link e codice promo (pagina degli annunci + `?promo=<codice>` in vigore) | | |
| 9 | Corrispondenze e parametri | | |

**Promesse trovate:**
| Frase | Dove | Riga di arya-oggi.md che la autorizza | Esito |
|---|---|---|---|

**Test degli attributi personali:**
| Frase | Senza il prodotto dice… | Passa? |
|---|---|---|

**Misure:**
| Cosa | Valore | Limite | Esito |
|---|---|---|---|
| Messaggio nel testo entro | [ ] car. | 125 | |
| Gancio scritto | [ ] car. | 40 | |
| Titolo | [ ] car. | 27 | |
| Durata video | [ ] s | sotto 30 | |
| Gancio entro | [ ] s | 2 | |

**Rilievi:**
```
[GRAVE] — <punto esatto>
Cosa non va: <una riga, con la regola>
Prima: "…"  →  Dopo: "…"

[MEDIO] — <punto esatto>
Cosa non va: …
Come lo riscriverei: "…"
```
**Opinioni** (nessuna regola le sostiene): …

*(ripetere il blocco per ogni pezzo)*

---

## Diversità della settimana
| Chi parla | Argomento | Formato | Pezzi | Già in campo con gli stessi tre? |
|---|---|---|---|---|

Volti o voci diversi nella settimana: [n] (minimo 3) · Chiusura grafica e frase: uguali in tutti sì/no/da decidere

## Diagnosi (solo se richiesta)
| Pezzo in campo | Numeri letti (fonte, periodo, spesa) | Cosa succede | Dove è il problema | Indizio o confermato |
|---|---|---|---|---|

## Cancelli ancora aperti (bloccano l'attivazione, non il collaudo)
- [ ] Ricontatto di ARYA provato con almeno 20 contatti finti — pagina Arya
- [ ] Ricontatto di ARYA provato con almeno 20 contatti finti — modulo Meta
- [ ] Pagina Arya, numero da chiamare, chat di prova, "fatti richiamare" pronti
- [ ] Consenso e informativa su pagina e modulo; "Come ci hai conosciuto?" nel modulo
- [ ] Chi risponde ai contatti, e in quali fasce

## Da segnalare a Ivan
- [gialli da decidere, promesse che mancano (domande per Roberto), cancelli aperti] → righe aggiunte in direttore/da-rivedere.md: [sì/no]

## Cosa non so
- [anteprime non viste, file che non si aprono, offerta.md mancante, numeri non disponibili…]
