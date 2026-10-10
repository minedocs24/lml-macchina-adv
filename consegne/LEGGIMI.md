# Consegne — come si carica un pezzo finito

Per la persona social e per chi gira. Questo foglio sta anche su OneDrive, in `Company/Marketing/macchina-adv/consegne/`.
Versione 1.0 — 10 ottobre 2026 (decisione 26).

## In breve
1. Il lunedì la Regia scrive le schede. Le trovi su OneDrive in `macchina-adv/regia/`.
2. Ogni scheda ha il suo **id**: è il nome del file senza `.md`. Esempio: la scheda `2026-10-13-telefono-in-sala.md`
   ha id `2026-10-13-telefono-in-sala`. L'id è scritto anche in testa alla scheda.
3. Per ogni scheda c'è già una cartella vuota: `macchina-adv/consegne/<id>/`. Se non c'è, creala tu con lo stesso nome.
4. Quando il pezzo è montato, metti **quattro file** in quella cartella (sotto).
5. Il giovedì il Collaudo lo controlla e lascia nella stessa cartella il suo esito: verde, giallo o rosso.

**Un pezzo per cartella.** Se della stessa idea fai due versioni con schede diverse, ognuna va nella sua cartella.

## I quattro file

| File | Cosa ci metti | Esempio di nome |
|---|---|---|
| **Il pezzo** | il video finito (verticale 9:16, sotto i 30 secondi, sottotitoli incisi) oppure l'immagine finita | `video.mp4` · `immagine.jpg` |
| **Il testo del post** | il testo che andrà sotto il post, esattamente come vuoi pubblicarlo | `testo-post.txt` |
| **La trascrizione** | tutte le parole dette nel video, con il secondo in cui iniziano e chi parla (vedi sotto) | `trascrizione.txt` |
| **Il primo fotogramma** | un'immagine del primissimo fotogramma del video, quello che si vede prima di premere play | `primo-fotogramma.jpg` |

**In più, se il programma di montaggio lo fa:** i sottotitoli esportati come file `.srt` (`sottotitoli.srt`). Aiuta il
Collaudo a controllare che le scritte siano giuste lettera per lettera.

**Se il video deve finire su Metricool**, aggiungi `link-video.txt` con il link di condivisione di OneDrive del video
("chiunque abbia il link può visualizzare"). Senza il link la bozza su Metricool non si può preparare da sola.

Per un'**immagine** (post statico) la trascrizione non serve: scrivi in `trascrizione.txt` solo "statica, nessuna parola
detta" e metti come primo fotogramma l'immagine stessa.

## Come si scrive la trascrizione
Una riga per frase. Prima il secondo, poi chi parla, poi le parole esatte, anche quelle sbagliate o ripetute.
In prima riga la durata totale.

```
durata: 0:24
0:00 IVAN: Sono in sala con un cliente e il telefono squilla.
0:03 ARYA: Buongiorno, sono Arya, l'assistente virtuale di ...
0:09 IVAN: ...
```

Chi parla: `IVAN`, `BRIAN`, `RICCARDO`, `MAURO`, `SOCIAL` (tu), `TECNICO`, `ARYA` (la voce o la chat di Arya).
Se nel video si vede una chat scritta di Arya, copia anche quei messaggi, con `ARYA (chat):`.

## Cosa controlla il Collaudo (così lo sai prima)
- Le promesse: si dice solo quello che Arya fa davvero oggi (lo dice la scheda, alla voce "Promessa ammessa").
- Prezzi e promozioni: solo quelli in vigore. Se nella scheda non ci sono, non dirli.
- **Nessun nome di cliente**, né detto né scritto né in un logo o in una schermata. **Mai clienti in video.**
- **Quando parla Arya, la sua prima frase dice che è un assistente virtuale.** Se manca, il pezzo è rosso.
- Il gancio entro i primi 2 secondi, scritto a schermo; il marchio solo alla fine; sottotitoli sempre.
- Niente di importante nel 14% in alto e nel 35% in basso del video verticale: lì Instagram mette le sue scritte.
- Niente frasi che dicono qualcosa su chi guarda ("hai problemi col telefono?"): si racconta una situazione.

## Gli esiti
- **Verde:** va bene così. Il venerdì diventa una bozza su Metricool e la approvi tu o Ivan prima che esca.
- **Giallo:** c'è qualcosa da sistemare o da decidere (per esempio manca la trascrizione). Nel file dell'esito c'è
  cosa serve. Decide Ivan.
- **Rosso:** così non può uscire. Nel file dell'esito c'è la correzione già scritta. Correggi e ricarica.

## Se correggi un pezzo
**Non cancellare e non sovrascrivere** i file vecchi. Aggiungi i nuovi con `-v2` nel nome (`video-v2.mp4`,
`trascrizione-v2.txt`, ...). Il Collaudo controlla l'ultima versione e scrive un esito nuovo.

## Cosa non mettere mai nella cartella
Numeri di telefono, email o nomi di clienti o di altre persone esterne, conversazioni vere di clienti, file che non
riguardano il pezzo.

## Se hai un dubbio
Scrivilo in un file `domande.txt` nella stessa cartella: lo legge il Collaudo e, se serve, finisce fra le cose che
deve decidere Ivan. La macchina non manda email né messaggi.
