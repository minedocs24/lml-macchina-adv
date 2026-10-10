---
name: campo
description: Reparto Messa in campo della macchina pubblicitaria di Arya. Il venerdì, dopo che Ivan ha approvato il pacchetto della settimana, prepara IN PAUSA campagne, gruppi, creatività e inserzioni su Meta (e la scheda per Google) verso la porta principale (pagina Arya con numero, chat di prova, fatti richiamare) o la seconda porta (modulo Meta), una scrittura alla volta con rilettura dopo ognuna, sempre seguendo meta-scrittura-sicura, e scrive il verbale di montaggio. Usala quando si dice "metti in campo il pacchetto", "carica la settimana su Meta", "preparala in pausa", "monta le campagne", "cosa resta da fare a me per partire?". Non attiva mai, non cambia mai un budget, non elimina, non scrive nel CRM; in ottobre 2026 (costruzione) non fa nessuna chiamata a Meta.
---

# Reparto Messa in campo — tutto pronto, niente acceso

## Quando si usa
- **Venerdì** (ritmo della settimana in `CLAUDE.md`): Ivan approva il pacchetto (secondo cancello) e decide la spesa
  (terzo cancello); Campo prepara tutto **in pausa** e gli lascia l'elenco di cosa resta a lui.
- Frasi tipiche: "metti in campo i pezzi verdi", "caricali in pausa", "prepara la campagna del modulo",
  "cosa manca per attivare?".
- **Mai in un'automazione che scrive su Meta.** Nelle automazioni Meta è solo lettura (`CLAUDE.md`): lì Campo può solo
  preparare il verbale "a carta". Le scritture si fanno in una sessione con Ivan presente, che risponde in conversazione.

### La fase di costruzione (ottobre 2026): nessuna chiamata a Meta
Finché la macchina è in costruzione, Campo **non chiama Meta, nemmeno in lettura**. Prepara il **montaggio a carta**: lo stesso
verbale, con tutti i parametri pronti e gli ID segnati "da creare". La fase finisce solo quando Ivan lo scrive (riga in
`direttore/da-rivedere.md` chiusa con il suo sì, o decisione in `regole/decisioni.md`). Anche dopo, nessuna campagna dei
prodotti si prepara per l'attivazione se il ricontatto di ARYA non è provato con almeno 20 contatti finti per ciascuna
porta (§3.1, §26): si può montare in pausa, ma nel verbale il cancello resta aperto.

## Cosa legge all'inizio
Sempre:
1. `CLAUDE.md`, `conoscenza/apprendimenti.md`, `regole/decisioni.md`.
2. L'ultimo file datato in `campo/` (cosa è già in campo, cosa era rimasto a Ivan, entità di scarto).

Per questo reparto:
3. `.claude/skills/meta-scrittura-sicura/SKILL.md` — **sempre, per intero, prima di ogni scrittura**. Resta com'è.
4. `regole/regole-adv.md` 3.0: §0.1, §1, §3.1, §6, §8, §9, §13, §14, §17, §23, §24bis, §26, §29.
5. Il collaudo della settimana in `collaudo/` (esito di ogni pezzo) e le schede dei pezzi in `regia/`.
6. Il pacchetto approvato da Ivan e il piano in `piano/` (cosa provare, quale porta, quale budget).
7. `conoscenza/arya-oggi.md`, solo per verificare che i testi non siano cambiati dopo il collaudo.
8. `references/parametri-porte.md` (parametri del connettore, letti il 7/10/2026) e `references/verbale-montaggio.md`.

Nel verbale: versione e data di ogni file letto.

### Dove meta-scrittura-sicura è rimasta a settembre
`meta-scrittura-sicura` si usa così com'è per **come** si scrive: proposta, sì, una scrittura, rilettura. Ma i suoi numeri
sono di settembre. **Dove dice cose diverse, valgono §8 e §9 di `regole-adv.md` 3.0 e `regole/decisioni.md`:**
| meta-scrittura-sicura dice | Vale invece |
|---|---|
| 300 € al mese, 10 € al giorno per campagna | Decisioni 5 e 12 e §9: ottobre nessuna campagna nuova; dalla Prova (metà novembre) 1.500 €/mese su Meta, cioè 50 €/giorno, + 400 € Google; gen-mar 3.000 €/mese; apr-set 5.000-10.000 € solo dopo i controlli |
| Aumenti del 20-30% ogni 3-4 giorni | Decisione 6: +20% ogni 2 settimane, solo se un cliente costa meno di 600 €. E gli aumenti li fa Ivan, non Campo |
| Account Minedocs in sola lettura "fino a ottobre 2026" | §8: le campagne dell'agenzia restano su Minedocs, si leggono e non si toccano; cosa fare dopo ottobre lo decide Ivan. Campo non scrive mai su Minedocs |
| Fronti ARYA (Meta), LML (Meta), IVAN (LinkedIn) | §6 e §8: ARYA = prodotti su Meta **e Google**; LML = consulenza su Meta; IVAN = personal brand su LinkedIn. Formato e esempi del nome dalla §8 |
| Legge `regole-adv.md` e `product-marketing.md` su OneDrive `lml-adv` | Si leggono `regole/regole-adv.md` e `conoscenza/arya-oggi.md` in questo archivio |

## Cosa produce
- `campo/AAAA-MM-GG-<pacchetto>.md` — il **verbale di montaggio** (modello in `references/verbale-montaggio.md`). Un file per
  montaggio, mai sovrascritto. Sezioni: stato finale (in pausa / a carta) e spesa a oggi · pacchetto e sì di Ivan testuali ·
  fondamenta (account, valuta, pagina, campagne attive) · una riga per scrittura con parametri, ID restituito e rilettura ·
  anteprime con gli indirizzi · errori e scarti · **cosa resta a Ivan** · **Cosa non so** (ultima, sempre).
- Le entità su Meta, **tutte non attive** (in bozza o in pausa: vedi sotto), solo fuori dalla fase di costruzione.
- Per Google: la **scheda dei parametri** dentro lo stesso verbale. In questo ambiente non c'è un connettore Google: la
  campagna la crea Ivan a mano.

## Come lavora
1. **Controlla i cancelli prima di tutto.** Per ogni pezzo: collaudo **verde**, oppure giallo con la decisione scritta di
   Ivan. Rosso: non si monta. Pacchetto approvato da Ivan: si copia il suo sì **testuale**. Un "procedi" generico su un
   piano non vale come sì sulle scritture (meta-scrittura-sicura, regola zero).
2. **Sceglie la porta di ogni pezzo come scritto nel piano**, senza decidere da sé:
   - **porta principale, pagina Arya** (chiama il numero, prova la chat, fatti richiamare), su Meta e su Google.
     L'indirizzo è la **pagina degli annunci** scritta in `CLAUDE.md` ("Impostazioni"): si legge da lì ogni volta, non si
     ricopia. Il link di ogni inserzione è quell'indirizzo più `?promo=<codice>` della promozione del pezzo (scheda in
     `regia/`; se non ne cita nessuna, la "predefinita" di `elenco_promozioni`; decisioni 23 e 24);
   - **seconda porta, modulo Meta**: nome, telefono, attività facoltativa, consenso separato con informativa.
   Mai una campagna dei prodotti direttamente verso una chat WhatsApp (§26). Un fronte solo per campagna (§6).
3. **Struttura.** La dice il pacchetto approvato. Se non la dice, proposta di partenza da far approvare: una campagna per
   porta, un gruppo con pubblico largo (solo Italia, nessun interesse), un'inserzione per pezzo. Al massimo due campagne
   attive in tutto (§0.1). Nessun pubblico costruito a mano; retargeting solo quando quei pubblici esistono (§0.1, §14).
4. **Nomi.** Campagna nel formato §8 `[FRONTE] - [OBIETTIVO] - [OFFERTA] - [MESE ANNO]`, es.
   `ARYA - Contatti - Pagina Arya - 11 2026`. Gruppo: `<porta> - Italia - Largo - <settimana>`. Inserzione: lo stesso
   titolo breve della scheda in `regia/` più versione e formato (`<titolo-breve>-A-9x16`), così Numeri ritrova il pezzo
   in `regia/archivio-pezzi.md`.
5. **Fondamenta (sola lettura, fuori dalla costruzione).** Verifica a quali account risponde il connettore: deve esserci
   `lml-adv` (`2214221312473862`), in euro. Se non c'è, **si ferma**. Legge il minimo di budget per giorno, l'ID della
   pagina LML e, per il modulo, se la pagina ha accettato i termini dei moduli. Conta le campagne attive.
6. **Una scrittura alla volta, ognuna con la frase di proposta di meta-scrittura-sicura (passo 3), il sì di Ivan in
   conversazione, poi la rilettura.** Ordine: campagna → gruppo → file (immagini, video: si aspetta che il video sia
   pronto) → creatività e inserzioni, una per pezzo. Dopo ogni scrittura si rilegge l'entità e si scrive nel verbale
   **cosa si vede davvero**: nome, stato, porta, pubblico, budget. Mai due creazioni di fila senza rilettura in mezzo.
7. **Budget.** Si scrive solo alla creazione, solo il numero giornaliero scritto nel pacchetto approvato, dentro §9, in
   centesimi (50 € = `5000`), riletto prima e dopo. Se il pacchetto non dice un importo giornaliero, o è fuori §9, ci si
   ferma e si chiede. Dopo la creazione **nessun budget si cambia**: né importo, né tetto, né spostamenti.
8. **Testi e file si copiano dal pezzo collaudato**, senza ritocchi. Se un testo non convince, torna al Collaudo. In ogni
   creatività: ID della pagina, file, testo, titolo, pulsante che dice cosa succede, indirizzo della porta. Per il video,
   la copertina è il primo fotogramma del gancio, controllato. Dichiarazione europea: beneficiario e pagante
   `LML Technologies S.r.l.`.
9. **Anteprime.** Per ogni inserzione almeno feed mobile, storie e Reels; gli indirizzi vanno nel verbale e nella risposta a
   Ivan. Si controlla: titolo intero, messaggio prima del taglio, niente coperto, pulsante giusto.
10. **Google (da novembre, decisione 5).** Scheda per Ivan: campagna sul nostro nome e campagna sulle parole del problema
    **sempre separate**, parole escluse dal primo giorno (lavoro, stipendio, gratis, corso, cos'è, come funziona,
    tutorial), destinazione pagina Arya, budget dal pacchetto dentro i 400 €/mese (§29).
11. **Scrive il verbale** e in chat riassume: cosa è pronto, in pausa, con gli ID, e cosa resta a Ivan.

### "In pausa" con il connettore di oggi
**Decisione 19 (Ivan, 7/10/2026):** Campo usa **solo gli strumenti che leggono e quelli che creano in pausa**. **Mai
attivare, mai eliminare.** Nessun altro strumento di scrittura (modifiche di budget, stato, pubblici, pixel, eliminazioni,
archiviazioni) si usa da Campo.

Dalle descrizioni degli strumenti lette il 7/10/2026 (nessuna chiamata): il connettore lavora in **modalità bozza**. Ogni
creazione finisce nella bozza di Gestione inserzioni (stato DRAFT) e **non è pubblicata**. La pubblicazione si fa con
lo strumento di attivazione, e quello che si pubblica parte **subito attivo**. Quindi:
- per Campo "in pausa" vuol dire **bozza non pubblicata o PAUSED**; si verifica rileggendo lo stato effettivo;
- lo strumento di attivazione (`ads_activate_entity`) **Campo non lo chiama mai**: pubblicare la bozza è attivare la
  spesa, ed è di Ivan;
- oggi il connettore accetta anche lo stato "eliminato", che è **definitivo** (la §24bis diceva il contrario):
  Campo non manda mai DELETED né ARCHIVED. Un'entità sbagliata si rinomina `SCARTO-AAAA-MM-GG` e la toglie Ivan.

### Se qualcosa va storto
| Cosa succede | Cosa fare |
|---|---|
| Scrittura rifiutata | Non ritentare uguale. Leggere l'errore, correggere il parametro, ripresentare a Ivan |
| Entità nata sbagliata | Lasciarla non attiva, rinominarla `SCARTO-<data>`, segnalarla nel verbale per Ivan |
| Testo sbagliato in un'inserzione | Le creatività non si modificano: creatività nuova e inserzione nuova, dopo un nuovo sì |
| Video non ancora pronto | Aspettare e rileggere lo stato; mai un'inserzione con un file non pronto |
| Il connettore non vede `lml-adv` | Fermarsi. I parametri esatti vanno nel verbale; li esegue Ivan a mano |
| Anteprima che non si apre | Riprovare una volta con l'ID della creatività; se l'errore parla di accesso, segnalarlo |

## Cosa non fa
- **Non attiva, non pubblica la bozza, non cambia budget o tetti, non sposta soldi** (terzo cancello, decisione 7).
- Non scrive su Meta in un'automazione, né senza il sì di Ivan in conversazione, né in fase di costruzione.
- Non elimina e non archivia niente. Non scrive su Minedocs.
- Non monta un pezzo rosso o un giallo senza la decisione scritta di Ivan; non cambia testi, promesse o nomi.
- Non inventa parametri, ID di interessi o di moduli: se un valore non è letto o dato, si scrive cosa manca.
- Non scrive nel CRM (solo lettura, e qui non serve). Non manda email o messaggi a nessuno.
- Nessun nome, telefono o email di persone esterne nel verbale o nei parametri (decisione 9).

## Come chiude
a) **Apprendimenti**: in `conoscenza/apprendimenti.md` una riga per lezione (data; indizio, o confermato solo se regge in
   due periodi diversi; cosa si è visto; spesa e tempo — "0 € — montaggio in pausa"; cosa cambia). Es.: un parametro che il
   connettore rifiuta, un comportamento nuovo del connettore. Niente si cancella: una lezione smentita diventa
   "superata il AAAA-MM-GG — motivo".
b) **Salva**: un commit, messaggio in italiano, es. "campo: pacchetto 16 ottobre a carta, 8 inserzioni pronte, nessuna
   chiamata a Meta (costruzione)".
c) **Copia leggibile su OneDrive** in `Company/Marketing/macchina-adv/campo/`.
d) **Ivan**: in `direttore/da-rivedere.md` una riga con cancello "spesa" per l'attivazione (anteprime da vedere, cancelli
   aperti, budget e tetto da impostare dentro Meta e Google, pubblicazione della bozza) e una per ogni entità di scarto.

## Da dove viene
| Skill di settembre | Cosa è stato preso | Cosa è stato lasciato e perché |
|---|---|---|
| `lml-montaggio-campagna` (SKILL, `parametri.md`, `verbale-montaggio.md`) | Una scrittura alla volta con rilettura; ordine campagna → gruppo → file → creatività e inserzioni; budget in centesimi riletto prima e dopo; minimo di budget per valuta; pagina dentro ogni creatività; dichiarazione europea `LML Technologies S.r.l.`; pubblico largo, mai interessi inventati; creatività che non si modificano; nomi di creazione diversi da quelli di modifica; leggere gli obiettivi validi dalla risposta; video pronto prima dell'uso; anteprime con indirizzi; tabella degli errori; entità di scarto; "cosa serve per attivare"; struttura del verbale | Destinazione WhatsApp, pulsante "Invia messaggio", messaggio di apertura precompilato, ottimizzazione per conversazioni (ora pagina Arya o modulo Meta, §3.1); budget 10 €/giorno = `1000` (ora §9, dal pacchetto); nomi per settore e blocco (ora pezzi settimanali, decisione 4); "un angolo per gruppo"; collaudo per blocco; "Claude non può eliminare" (il connettore di oggi accetta l'eliminazione definitiva: qui è vietata); percorsi `montaggi/<settore>/` |
| `meta-scrittura-sicura` | Usata com'è: regola zero, frase di proposta, sì in conversazione, rilettura sempre, sì separato per attivare e per i budget, quando fermarsi | Non modificata. Superati solo i numeri e i riferimenti elencati nella tabella sopra (§8, §9, decisioni 5-6) |
| Regole nuove (3.0, decisioni, `CLAUDE.md`) | Venerdì; tre cancelli; automazioni solo in lettura; costruzione senza chiamate a Meta; due porte; Google dal lancio con campagne separate; ricontatto provato con 20 contatti finti per porta | — |
