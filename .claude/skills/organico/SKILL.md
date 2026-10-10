---
name: organico
description: Pubblicazione organica della macchina pubblicitaria di Arya (reparto Messa in campo). Il venerdì trasforma i pezzi con collaudo verde in bozze IN REVISIONE su Metricool per i profili di LML, con il testo collaudato e il link con promo= e utm, e scrive il registro in campo/AAAA-MM-GG-organico.md. Mai pubblicazione diretta, mai approvazione automatica: approva la persona social o Ivan. Usala quando si dice "metti i pezzi verdi su Metricool", "prepara le bozze organiche", "manda in revisione i reel della settimana", "cosa aspetta l'approvazione su Metricool?". Non pubblica, non cambia né cancella post approvati, non tocca Meta né il CRM, non spende.
---

# Pubblicazione organica — bozze in revisione su Metricool, mai post pubblicati da soli

**Serve il connettore Metricool** (lo usa il Direttore, decisione 28). Senza, si scrive in "Cosa non so" e si ferma.

## Quando si usa
- **Venerdì** (ritmo della settimana in `CLAUDE.md`), dopo il Collaudo del giovedì: un pezzo verde diventa una bozza in
  revisione; la persona social o Ivan la approva in Metricool e solo allora esce.
- Quando un pezzo diventa verde dopo un ricollaudo, il primo giro utile del Direttore.
- Frasi tipiche: "metti i verdi su Metricool", "prepara le bozze", "cosa aspetta l'approvazione?".

## Cosa legge all'inizio
1. `CLAUDE.md` (sezione "Impostazioni": pagina degli annunci, **marchio Metricool dei profili LML**, **revisori**),
   `conoscenza/apprendimenti.md`, `regole/decisioni.md` (26-28).
2. L'ultimo file `campo/AAAA-MM-GG-organico.md` (cosa è già in revisione o approvato: non si rifà).
3. L'ultimo verbale di `collaudo/` e, per ogni pezzo, il file dell'esito in OneDrive
   `macchina-adv/consegne/<id-scheda>/collaudo-AAAA-MM-GG.md` (l'ultimo).
4. La cartella delle consegne del pezzo: il pezzo, `testo-post.txt`, `link-video.txt` (versione collaudata).
5. La scheda `regia/<id-scheda>.md` (formato, promozione citata) e `direttore/da-rivedere.md` (il sì di Ivan su un giallo).

Nel registro: versione e data di ogni file letto.

## Le regole che non si toccano
- **Solo bozze in revisione.** Si usa **solo** lo strumento che crea un post nuovo e lo manda in revisione
  (`createScheduledPostForReview`), più le letture (`getBrandSettings`, `getScheduledPosts`, `getBestTimeToPostByNetwork`).
- **Mai** `createScheduledPost` (pubblica da solo all'ora data), **mai** `updateScheduledPost` né
  `sendScheduledPostForReview` su un post esistente (cambiano un post che qualcuno ha già visto o approvato), **mai**
  cancellare. Un errore si segnala: lo sistema la persona social in Metricool.
- **Approvazione:** `approvalSystem` = `"any"` (basta uno fra la persona social e Ivan). **Mai `"optional"`**: approva
  da solo se nessuno rifiuta, quindi sarebbe una pubblicazione senza sì.
- **Revisori:** solo gli indirizzi scritti in `CLAUDE.md` ("Revisori delle bozze Metricool"), collaboratori del marchio.
  Un indirizzo esterno riceverebbe un'email: se la riga manca o un indirizzo non è un collaboratore, ci si ferma.
  Gli indirizzi non si copiano nel registro (si scrive "persona social" e "Ivan").
- **Marchio:** solo quello scritto in `CLAUDE.md` ("Marchio Metricool dei profili LML"), riletto con `getBrandSettings`.
  Se la riga dice "manca", o il marchio letto non corrisponde, ci si ferma: **nessuna bozza sul profilo personale di Ivan**
  (è un altro fronte, §6).
- **Solo pezzi verdi.** Un giallo solo con il sì scritto di Ivan in `direttore/da-rivedere.md` (copiato testuale).
  Un rosso mai.
- **Testi e file uguali al collaudo.** Nessun ritocco: se un testo non convince, torna al Collaudo.
- **Niente spesa:** niente "boost" né promozione del post (`boost` vuoto). La spesa passa solo da Campo e da Ivan.

## Come lavora
1. **Cancelli.** Per ogni pezzo: esito verde (o giallo con il sì di Ivan); consegna completa; nessuna bozza già creata per
   quell'id (registro e `getScheduledPosts` sulle prossime 2 settimane). Se il marchio o i revisori mancano in `CLAUDE.md`,
   nessuna bozza: riga in `direttore/da-rivedere.md`, cancello "pacchetto".
2. **Il video.** Metricool vuole un indirizzo pubblico del file: si usa `link-video.txt` della consegna. Se manca, o
   Metricool lo rifiuta, nessun tentativo strano: il pezzo resta "da caricare a mano" e si scrive cosa serve.
3. **La data.** La propone la persona social nella consegna se vuole; altrimenti il primo orario buono da
   `getBestTimeToPostByNetwork`, almeno **48 ore dopo** la creazione (tempo per approvare) e mai nel passato.
   Se l'approvazione arriva dopo quell'ora, la data la sposta chi approva.
4. **Il post.** `info` con: `providers` del marchio LML (Instagram e Facebook, se collegati), `text` = `testo-post.txt`
   esatto, `media` = il link del video o dell'immagine, `instagramData.type` = `REEL` per i video e `POST` per le immagini,
   `facebookData.type` = `REEL` o `POST`, `autoPublish` = vero (esce da solo **solo dopo** l'approvazione),
   `draft` = falso, niente `boost`. Se il testo contiene un link: pagina degli annunci di `CLAUDE.md` +
   `?promo=<codice>&utm_source=<instagram|facebook>&utm_medium=organico&utm_campaign=organico&utm_content=<id-scheda>`
   (codice della scheda o la promozione "predefinita"; decisione 23). L'indirizzo della pagina si **legge** da
   `CLAUDE.md` ogni volta, non si ricopia (decisione 24).
5. **Una bozza alla volta**, poi rilettura con `getScheduledPosts`: nel registro si scrive ciò che torna (stato, data,
   `plannerUrl`), non ciò che si è mandato.
6. **Il registro.** `campo/AAAA-MM-GG-organico.md`, mai sovrascritto: per ogni pezzo id della scheda, esito del collaudo,
   rete, data proposta, stato in Metricool ("in revisione"), `plannerUrl`, cosa resta da fare. In fondo **Cosa non so**.
7. **Ivan e la persona social.** Una riga in `direttore/da-rivedere.md`: "N bozze in revisione su Metricool, le approva
   la persona social o Ivan", cancello "pacchetto". Nessun altro messaggio: l'email di revisione la manda Metricool da sé
   ai revisori interni (decisione 28).

## Il lunedì: cosa serve al Piano
I numeri organici li legge **il Piano** (skill `piano`), non questa skill. Metriche di Metricool lette il 10/10/2026:
- Instagram Reels: `IGRE28` percentuale di visualizzazioni oltre 3 secondi (**quanti si fermano**), `IGRE24` tempo medio
  di visione e `IGRE27` percentuale media vista (**quanto guardano**), `IGRE23` visualizzazioni, `IGRE11` copertura,
  `IGRE06` link del reel, `IGRE03` testo (per ritrovare il pezzo).
- Facebook Reels: `FBRE13` tempo medio, `FBRE10` visualizzazioni, `FBRE11` copertura (non c'è la percentuale oltre 3 secondi).
Se Metricool cambia le metriche, si rileggono con `getAnalyticsAvailableMetrics` e si scrive la data.

## Cosa non fa
- Non pubblica, non approva, non cambia né cancella post. Non usa il profilo personale di Ivan.
- Non promuove a pagamento (boost) e non tocca Meta Ads né il CRM.
- Non mette nomi, telefoni o email di persone esterne, né gli indirizzi dei revisori, nel registro.
- Non manda email o messaggi (le email di revisione sono di Metricool, solo ai revisori interni).
- Non inventa: se un file, un link o un marchio manca, lo scrive in "Cosa non so".

## Come chiude
a) **Apprendimenti**: una riga se si è imparato qualcosa (es. un formato che Metricool rifiuta), indizio o confermato.
b) **Salva su `main`**: un commit, es. "organico: 4 bozze in revisione su Metricool, settimana 16-20 novembre".
c) **Copia leggibile** del registro su OneDrive `Company/Marketing/macchina-adv/campo/`.
d) **Da rivedere**: la riga per l'approvazione e ogni blocco (marchio, revisori, link del video).
