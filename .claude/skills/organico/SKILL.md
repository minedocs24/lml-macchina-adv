---
name: organico
description: Testo dei post organici della macchina pubblicitaria di Arya (reparto Messa in campo). Il martedì, insieme alle schede della Regia, prepara il testo del post di ogni pezzo (una versione per Facebook con il link, una per Instagram) e lo mette nella cartella delle consegne su OneDrive, dove il giovedì lo controlla il Collaudo; se il Collaudo scrive una correzione, prepara la versione nuova. I pezzi verdi li pubblica la persona social su Instagram e Facebook dalla Meta Business Suite, con il testo approvato. Usala quando si dice "prepara i testi dei post", "il testo per Instagram", "correggi il testo dopo il collaudo". Non pubblica niente, non usa strumenti social o a pagamento, non tocca Meta né il CRM.
---

# Testo dei post organici — la macchina scrive, la persona social pubblica

Decisione 33 (10/10/2026): niente Metricool. I pezzi con collaudo **verde** li pubblica **la persona social**
direttamente su Instagram e Facebook dalla **Meta Business Suite**, con il testo approvato dal Collaudo. La macchina
**prepara solo il testo del post**. I numeri che contano sono quelli delle **inserzioni**, che i Numeri leggono da Meta.

## Quando si usa
- **Martedì**, nello stesso giro delle schede della Regia (conta come un lavoro solo): un testo per ogni scheda.
- **Dopo un collaudo giallo o rosso sul testo**: la versione nuova, con la correzione scritta dal Collaudo.
- Frasi tipiche: "prepara i testi dei post", "il testo del reel di Brian", "sistema il testo dopo il collaudo".

## Cosa legge all'inizio
1. `CLAUDE.md` (pagina degli annunci in "Impostazioni"), `conoscenza/apprendimenti.md`, `regole/decisioni.md`.
2. L'ultimo file `campo/AAAA-MM-GG-testi-post.md` (testi già scritti: non si rifanno).
3. La scheda del pezzo `regia/<id-scheda>.md`: argomento, promessa ammessa (riga di `arya-oggi.md`), promozione
   citata, tre ganci, chiusura.
4. `conoscenza/arya-oggi.md` (solo righe "vendibile"), `conoscenza/offerta.md` (specchio di `elenco_promozioni`),
   `conoscenza/customer-language.md`, `conoscenza/glossario.md`, `regole/regole-adv.md` §5.1, §23, §26.
5. Per una correzione: l'esito del Collaudo accanto al pezzo, `macchina-adv/consegne/<id-scheda>/collaudo-AAAA-MM-GG.md`
   (l'ultimo), e `domande.txt` se c'è.

Nel file prodotto: versione e data di ogni file letto.

## Cosa produce
1. **Nella cartella delle consegne** su OneDrive, `Company/Marketing/macchina-adv/consegne/<id-scheda>/testo-post.txt`
   (una correzione: `testo-post-v2.txt`, `-v3`…, mai sovrascritto). Lì lo trovano il Collaudo e la persona social.
2. **Nell'archivio** `campo/AAAA-MM-GG-testi-post.md`: tutti i testi della settimana, uno per id della scheda, con la
   riga di `arya-oggi.md` della promessa e il codice della promozione. In fondo **Cosa non so**.

### Com'è fatto `testo-post.txt`
```
id: <id-scheda> · versione: v1 · scritto il AAAA-MM-GG

FACEBOOK
<testo: il problema nelle prime parole, poi la promessa, poi l'invito>
<link: pagina degli annunci + parametri, sotto>

INSTAGRAM
<stesso testo, senza link: l'invito dice "trovi la pagina nel link del profilo">
```
- **Le prime parole dicono il problema** (§5.1) e il messaggio sta nei **primi 125 caratteri**.
- **Una sola promessa**, quella della scheda, presa da una riga "vendibile" di `arya-oggi.md`.
- **Prezzi e promozioni** solo se la scheda li cita e solo com'è scritto in `offerta.md`; il Collaudo li controlla in
  `elenco_promozioni`.
- **L'invito** dice cosa succede davvero sulla pagina Arya: chiama il numero, prova la chat, fatti richiamare (§3.1).
- **Il link** (solo Facebook, dove si clicca): pagina degli annunci letta da `CLAUDE.md` ogni volta, più
  `?promo=<codice>&canale=<telefono|chat|email>&utm_source=facebook&utm_medium=organico&utm_campaign=organico&utm_content=<id-scheda>`
  (schema dei parametri nella skill `campo`; `canale` si omette se il pezzo parla di tutta la suite; codice: quello della
  scheda o la promozione "predefinita"; decisioni 23 e 24).
- Parole dei clienti; il test della recensione; il test degli attributi personali (§23).
- **Mai** "intelligenza artificiale", nomi di clienti, numeri non misurati, "sostituisce il personale", le parole vietate
  della skill `collaudo`.

## Come lavora
1. Per ogni scheda della settimana senza testo: scrive `testo-post.txt` e lo mette nella cartella delle consegne (se la
   cartella non c'è, la crea con lo stesso id). Se OneDrive non risponde, il testo resta nell'archivio e si scrive in
   "Cosa non so" e in `direttore/da-rivedere.md`.
2. **Dopo il Collaudo:** se l'esito chiede di cambiare il testo, scrive la versione nuova copiando **esattamente** la
   riscrittura del Collaudo, niente di più; il pezzo torna al Collaudo (ricollaudo). Un testo verde non si tocca più.
3. **Non pubblica.** Il pezzo verde lo pubblica la persona social dalla Meta Business Suite, copiando l'ultima versione
   di `testo-post.txt` che il Collaudo ha dato verde (il file dell'esito lo dice).

## Cosa non fa
- Non pubblica, non programma, non promuove (niente "metti in evidenza" a pagamento): pubblica la persona social.
- Non usa strumenti social o servizi a pagamento (decisione 34). Non tocca Meta né il CRM.
- Non mette nel testo nomi, telefoni o email di persone esterne.
- Non manda email o messaggi a nessuno.
- Non cambia un testo che il Collaudo ha dato verde. Non inventa promesse o prezzi: se manca un dato, "Cosa non so".

## Come chiude
a) **Apprendimenti**: una riga se si è imparato qualcosa, indizio o confermato.
b) **Salva su `main`**: un commit, es. "organico: testi dei post per le 8 schede del 17 novembre".
c) **Copia leggibile** di `campo/AAAA-MM-GG-testi-post.md` su OneDrive `Company/Marketing/macchina-adv/campo/`.
d) **Da rivedere**: solo i blocchi (cartella che manca, promessa non vendibile nella scheda).
