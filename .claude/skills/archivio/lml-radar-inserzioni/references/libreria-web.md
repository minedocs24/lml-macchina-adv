# La Libreria Inserzioni — cosa dà lo strumento, cosa dà il sito

**Verificato il 13 settembre 2026** con due ricerche reali sull'Italia. Da riverificare se lo strumento cambia: segnare qui la data.

## 1. Lo strumento del connettore: `ads_library_search`

### Cosa restituisce, per ogni inserzione

| Campo | C'è? |
|---|---|
| Numero della Libreria | ✅ |
| Nome e numero della pagina | ✅ |
| Titolo del pulsante (`ad_creative_link_title`) | ✅ — spesso vuoto o "Leggi tutto" |
| Data di creazione e data di partenza | ✅ (in secondi dal 1970: vanno convertite) |
| Collegamento alla Libreria (`ad_snapshot_url`) | ✅ |
| Valuta | ✅ |
| **Testo dell'inserzione** | ❌ |
| **Video o immagine** | ❌ |
| **Se è ancora attiva / data di fine** | ❌ — usare il filtro `ad_active_status: "ACTIVE"` |
| **Persone raggiunte, età, genere, zone** | ❌ |
| `estimated_total_count` | ✅ — quante inserzioni corrispondono, in tutto |

### Comportamento misurato

- Restituisce **al massimo 50 inserzioni**, le **più recenti** per data di creazione. Non c'è modo di chiedere la pagina successiva né di ordinare dalle più vecchie.
- La ricerca per parole **senza virgolette è larghissima**: `chiamate perse` in Italia → 11.558 risultati, con pagine di intrattenimento in cima.
- Con le virgolette e il filtro attive: `"centralino AI"` → 123 risultati, concorrenti veri (fra cui uno non ancora nella lista: Romulus AI).
- Le stesse inserzioni compaiono spesso **in più copie identiche** (stessa pagina, stesso titolo, date a pochi secondi): sono la stessa creatività messa in più gruppi. Contarle è un segnale di scala.
- Funziona solo se chi lo usa ha almeno un account pubblicitario attivo.
- Copre le inserzioni **consegnate in UE/Regno Unito negli ultimi 12 mesi circa**. Un concorrente che fa pubblicità solo fuori dall'Europa non compare.

### Parametri

```
search_terms:      "frase esatta"      ← fra virgolette
countries:         ["IT"]
ad_active_status:  "ACTIVE"            ← sempre, nella scoperta
limit:             50
page_ids:          ["<numero>"]        ← per profilare una pagina nota
```

Cercando per `page_ids` si ottengono le inserzioni di quella pagina, sempre le 50 più recenti. Per una pagina con meno di 50 attive è l'elenco completo; per una con più di 50, le vecchie non si vedono da qui.

### Cosa NON fare

- Non estrarre in massa: lo strumento è pensato per la ricerca creativa, non per scaricare la Libreria.
- Non giudicare un'inserzione dai soli campi dello strumento: manca il testo.
- Non contare `estimated_total_count` come "numero di concorrenti": conta inserzioni, e le copie duplicate gonfiano il numero.

## 2. Il sito della Libreria: `facebook.com/ads/library`

Va aperto nel browser. Si usa per profilare le pagine trovate nel passo 1.

### Collegamenti pronti

Tutte le inserzioni attive di una pagina, in Italia:
```
https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IT&is_targeted_country=false&media_type=all&search_type=page&view_all_page_id=<NUMERO_PAGINA>
```

Solo i video di quella pagina: cambia `media_type=video`. Solo immagini: `media_type=image`. Valori possibili: `all`, `video`, `image`, `meme`, `image_and_meme`, `none`.

Ricerca per frase esatta:
```
https://www.facebook.com/ads/library/?active_status=active&ad_type=all&country=IT&is_targeted_country=false&media_type=all&q=%22frase%20esatta%22&search_type=keyword_exact_phrase
```

Una singola inserzione, dal suo numero:
```
https://www.facebook.com/ads/library/?id=<NUMERO_LIBRERIA>
```

Altri parametri utili: `publisher_platforms[0]=facebook` (o `instagram`), `content_languages[0]=it`, `start_date[min]=AAAA-MM-GG`.

### Come ordinare dalle più vecchie

Dal menu di ordinamento della pagina dei risultati, scegliere la data di inizio, crescente. L'ordinamento per persone raggiunte (`sort_data[mode]=total_impressions`) è disponibile per le inserzioni europee e serve a vedere quali stanno spendendo di più adesso — è un secondo criterio, non il primo.

### Cosa leggere su ogni inserzione

- **"Attiva dal"** — la data che conta. I giorni in aria si calcolano da qui.
- **Formato** — si vede.
- **Testo, titolo, pulsante, destinazione** — si vedono. Il pulsante dice dove porta: sito, modulo, WhatsApp, Messenger.
- **Piattaforme** — le icone sotto il nome della pagina.
- **"Vedi i dettagli dell'inserzione"** → il pannello europeo, obbligatorio per legge sulle inserzioni consegnate in UE: persone raggiunte nell'UE, distribuzione per età e genere, **zone incluse ed escluse**, chi paga e chi beneficia. È il targeting del concorrente scritto nero su bianco. Fuori dall'Europa non esiste.
- **Copie duplicate** — la Libreria le raggruppa ("N inserzioni usano questo contenuto"). Il numero è il segnale di scala.

### Cosa NON si vede mai

Spesa, clic, costi, risultati. Per le inserzioni commerciali non esistono. **L'unico indizio di funzionamento è il tempo in aria.**

### Le inserzioni spente

Sul sito, con `active_status=inactive`, si vedono le inserzioni europee spente da meno di 12 mesi circa. È l'unico modo di rivedere qualcosa che un concorrente ha abbandonato, e solo per un anno. Dopo, sparisce. Per questo il radar scrive file datati: l'archivio ce lo facciamo noi.

## 3. Conversione delle date dello strumento

Le date dello strumento arrivano come numero di secondi dal 1° gennaio 1970. Esempio: `1789131995` → 11 settembre 2026. Per convertire in modo affidabile usare uno strumento di calcolo, non fare a mente.

## 4. Fonti consultate per costruire questo metodo

Lette il 13 settembre 2026. Sono blog di venditori di strumenti di analisi: le cifre vanno prese come ordini di grandezza, non come dati verificati.

- get-ryze.ai — flusso in cinque passi (lista di sorveglianza, filtri, sopravvissute 60+, ripetizione fra tre concorrenti, archivio per argomenti); la stima dell'11,3% di sopravvivenza oltre 60 giorni.
- adlibrary.com — la longevità come unico indizio; l'avviso che il metodo non vede chi prova molto e in fretta; "il formato non è una strategia".
- selzee.com — controllo mensile, non trimestrale; includere la categoria adiacente e l'alternativa economica; salvare l'argomento (promessa, obiezione, prova, pubblico), non la creatività.
- adstellar.ai — sotto i 14 giorni è rumore, salvo volume su più concorrenti.
- admanage.ai, adsuploader.com, swipekit.app — campi dell'interfaccia ufficiale e copertura UE/Regno Unito.
