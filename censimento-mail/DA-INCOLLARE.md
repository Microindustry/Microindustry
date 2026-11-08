# Query pronte da incollare in Gmail

27/08/2026. **Tutte verificate in sola lettura su questa casella.** Nessuna
eseguita.

**Serve Gmail da browser sul PC.** L'app mobile non ha "seleziona tutte le
conversazioni che corrispondono", che è l'unica cosa che rende questo lavoro
di trenta secondi invece che di ore.

**Come si usa ogni query:** incolla nella barra di ricerca → invio → spunta la
casella in alto a sinistra → clicca **"Seleziona tutte le conversazioni che
corrispondono a questa ricerca"** → poi il pulsante Archivia o l'etichetta.

> **Perché non l'ho fatto io.** Non è solo il blocco sulle scritture: anche con
> i permessi, l'API archivia **un thread per chiamata**. Venticinquemila thread
> sono venticinquemila chiamate. Gmail da browser lo fa in un click. Questo è
> lo strumento giusto, non un ripiego.

---

## FASE 0 — Spegnere la sorgente propria

Non è una query. Vai su **GitHub → Settings → Notifications** e togli le email
per l'attività CI/Actions.

Verificato: `in:inbox from:notifications@github.com` restituisce **23 thread**,
tutti diretti a `TITANIUM_OS@noreply.github.com`. È il tuo sistema che ti scrive
addosso. Spegnere la sorgente prima di filtrare, altrimenti nascondi e basta.

---

## FASE 1 — Proteggere (fare per prima, sempre)

Crea l'etichetta **`TIENE`**, poi applica con queste due query.

### 1a. Utenze, banca, pagamenti, sicurezza

```
in:inbox from:(a2aenergia.it OR gruppocap.it OR ing.com OR mail.anthropic.com OR accountprotection.microsoft.com OR noreply-accounts@google.com OR noreply@github.com)
```

Verificata: restituisce bollette luce/gas A2A, fatture acqua Gruppo CAP,
estratti conto e promemoria mutuo ING, ricevute e pagamenti falliti Anthropic,
avvisi di sicurezza Microsoft, Google e GitHub.

⚠️ Prende anche il marketing di quei mittenti (`smile@a2aenergia.it`,
newsletter ING). Non è un problema: meglio proteggere qualche promozione in
più che perdere una bolletta.

### 1b. Solo i documenti con allegato

```
in:inbox has:attachment from:(a2aenergia.it OR gruppocap.it OR ing.com OR mail.anthropic.com)
```

Verificata. È il sottoinsieme che conta davvero — le bollette in PDF e le
fatture. Se vuoi essere selettivo, usa questa invece della 1a.

### 1c. Le stellate

```
in:inbox is:starred
```

53 thread. Li hai stellati tu: sono già una tua decisione, vanno rispettati.

---

## ⛔ Una cosa che avevo proposto e che RITIRO

Avevo scritto due volte che il criterio migliore per salvare le conversazioni
vere fosse **"i thread in cui hai risposto"**. L'ho verificato, e **non
funziona su Gmail**:

```
in:inbox from:me                                    → 1 risultato, ed è spam
in:inbox from:benenatimatteo.mb@gmail.com           → 0 risultati
```

Il motivo è strutturale: i tuoi messaggi inviati portano l'etichetta `SENT`,
non `INBOX`. La query chiede a un **singolo messaggio** di essere
contemporaneamente in inbox e scritto da te — cosa che non succede mai. Il
thread con `gigroup` contiene due tue risposte ed è in inbox, eppure nessuna
delle due query lo trova.

**Non usare quel criterio.** Se lo avessi automatizzato come proposto,
avrebbe protetto zero conversazioni e le avrebbe archiviate tutte.

Al suo posto, per la corrispondenza umana: hai già l'etichetta
**`ricerca lavoro`** (639 messaggi), ed è lì che sta di fatto tutto lo scambio
con persone vere. La escludo da ogni archiviazione qui sotto.

---

## FASE 2 — Archiviare il rumore

Una query per volta, dalla più sicura. **Archivia, non cancellare**: resta
tutto cercabile.

### 2a. Le notifiche CI (23 thread)
```
in:inbox from:notifications@github.com
```

### 2b. Commercio e promozioni
```
in:inbox from:(aliexpress.com OR ryanairemail.it OR myprotein.com OR email.subito.it OR reply.ebay.it OR zumub.com OR instant-gaming.com OR giardineria.com OR kasanova.com OR photosi.com OR vivaticket.com OR tisvapo.it OR sony-europe.com OR emails.tomtom.com OR gopro.com OR email.samsung.com OR email.playstation.com OR news.mcdonalds.it OR amazonmusic.com OR e.battle.net OR comms.activision.com)
```

### 2c. Social e raccomandazioni
```
in:inbox from:(pinterest.com OR service.tiktok.com OR mail.instagram.com OR facebookmail.com OR em.linkedin.com OR newsletters-noreply@linkedin.com OR jobalerts-noreply@linkedin.com OR nextdoor.com OR mail.crunchyroll.com OR mydramawave.com OR freeletics.com)
```

### 2d. Newsletter di strumenti
```
in:inbox from:(ifttt.com OR news.n8n.io OR info.n8n.io OR m.ngrok.com OR ollama.com OR notify.thinkific.com OR marketing.descript.com OR airtable.com OR mail.notion.so OR tradingview.com OR shapr3d.com OR printables.com OR assocral.org)
```

### 2e. Annunci di lavoro automatici
> Solo se ti va. Sono alert automatici, non persone. Ma decidi tu — l'etichetta
> `ricerca lavoro` resta comunque intatta e fuori da questa query.
```
in:inbox from:(push.infojobs.it OR notification-noreply-mkt@randstad.it OR news-it.adecco.com OR jobalert@orienta.net) -label:"ricerca lavoro"
```

### 2f. La spazzata storica — per ultima, dopo aver protetto
```
in:inbox older_than:2y -is:starred -label:"ricerca lavoro" -label:TIENE -from:(a2aenergia.it OR gruppocap.it OR ing.com OR mail.anthropic.com OR accountprotection.microsoft.com OR noreply-accounts@google.com OR noreply@github.com)
```

Verificata: il campione è puro rumore (infojobs, battle.net, Call of Duty,
tutto del 2024). Le esclusioni tengono fuori stellate, ricerca lavoro, TIENE e
i mittenti critici.

**Questa è quella che sposta i numeri.** Falla solo dopo la Fase 1.

---

## FASE 3 — Che non torni

Gmail → **Impostazioni → Filtri e indirizzi bloccati → Crea un nuovo filtro**.
Incolla la query nel campo **"Da"**, poi spunta **"Ignora Posta in arrivo"** +
**"Applica l'etichetta: RUMORE"**.

Un filtro per ciascuna delle query 2b, 2c, 2d. Metti la spunta anche su
**"Applica il filtro anche alle conversazioni corrispondenti"** e la Fase 2 e
la Fase 3 si fanno in un colpo solo.

---

## FASE 4 — Le 60 bozze

```
in:drafts
```

Sessanta bozze mai partite. Non le ho lette. È l'unico posto della casella dove
potrebbe esserci qualcosa di **tuo** rimasto a metà — vale i cinque minuti.

---

## Ordine consigliato

```
0 → 1a (o 1b) → 1c → 2a → 2b → 2c → 2d → [2e] → 2f → 3 → 4
```

La Fase 1 prima di tutto. Se salti quella e parti dalla 2f, archivi le bollette
insieme al resto — restano cercabili, ma perdi il colpo d'occhio su ciò che
scade.
