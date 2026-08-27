# Trovato nell'inbox — roba che sta ferma lì

27/08/2026. Emerso cercando cosa proteggere. **Sola lettura, niente modificato.**

---

## 1. Il Claude API è spento dal 22 agosto — e forse è la risposta

```
Da:      no-reply@mail.anthropic.com
Data:    22 agosto 2026, 10:10
Oggetto: [Action needed] Your Claude API access is turned off
Stato:   NON LETTA
Testo:   "Your access to the Claude API has been disabled because your
          organization 'Matteo's Individual Org' is out of usage credits."
```

Stamattina hai detto: *"gli agenti sono comunque da rivedere, penso che ci sia
qualcosa che non funzioni benissimo."*

**Guarda le date.** L'API è spenta dal 22 agosto. Lo `STATE.json` di TITANIUM_OS
è fermo al 16 agosto. Il repo riceve ancora i commit del `night_audit` — quelli
sono script Python, non chiamano il modello — ma qualunque agente che passa dalla
Claude API (Story Agent, Nina, apprendista caroselli, research) da cinque giorni
non ha credito per girare.

**Non è una diagnosi, è una coincidenza di date molto forte.** Va verificata sui
log al PC. Ma è la prima cosa da controllare, e si risolve in due minuti dalla
pagina Billing.

Non è la prima volta: **30 maggio 2026**, stesso identico messaggio, stessa
organizzazione. Quel giorno sono anche partiti tre solleciti:

```
Da:      failed-payments@mail.anthropic.com
Data:    30 maggio 2026, 16:07 · 16:08 · 16:12
Oggetto: $12.20 payment to Anthropic, PBC was unsuccessful
```

Tre tentativi di addebito falliti sulla carta, in cinque minuti. Poi l'API giù.
È già successo, con lo stesso meccanismo, e non l'hai visto nemmeno allora.

**Se c'è una sola cosa da fare oggi, è aggiornare il metodo di pagamento su
Anthropic.** Altrimenti il ciclo si ripete a ogni rinnovo.

---

## 2. Altre cose ferme in inbox

### Token GitHub scaduto
```
09/04/2026  token classico "titanium-scanner" creato (scope repo)
09/04/2026  ampliato con scope workflow
02/05/2026  "will expire in 6 days"     — non letta
08/05/2026  "will expire in about 9 hours" — non letta
```
Il token è scaduto a maggio. Se `titanium-scanner` serve a qualche automazione,
quella automazione è rotta da tre mesi e nessuno l'ha notato.

### 2FA GitHub
Cinque solleciti `[ACTION REQUIRED]` tra maggio e luglio. **Risolto**: il
17/07 è arrivata la mail dei codici di recupero. Da archiviare, non da fare.

### Bollette non lette
- `noreply@a2aenergia.it` — "La tua bolletta di energia elettrica è in scadenza",
  07/07/2026, **non letta**. Scadenza indicata: 08/07. Il giorno dopo.
- `noreply@a2aenergia.it` — "La tua bolletta luce è in scadenza", 06/05/2026,
  **non letta**. Scadenza: 07/05.
- `noreply@a2aenergia.it` — bolletta gas in scadenza 16/04/2026, **non letta**.
- `noreply@gruppocap.it` — promemoria scadenza acqua, giugno 2026 e gennaio 2026,
  marcate IMPORTANT.
- `info.it@ing.com` — promemoria rata mutuo, ricorrente. Non letti.

Non so se poi le hai pagate. So che gli avvisi sono arrivati e sono rimasti chiusi.

### Codici monouso Microsoft
Diverse mail `account-security-noreply@accountprotection.microsoft.com` con
codici di accesso monouso, non lette, ferme in inbox. Sono scaduti da tempo e non
li riporto qui. Vale però la regola generale: **i codici di sicurezza non restano
in una casella che non guardi.** Vanno archiviati o cancellati dopo l'uso.

---

## 3. Una correzione al piano del censimento

Avevo proposto di proteggere *"tutti i thread in cui c'è una tua risposta"*, come
criterio automatico per salvare le conversazioni vere.

La ricerca `in:inbox from:benenatimatteo.mb@gmail.com` ha restituito **zero
risultati**. Non significa che il criterio sia sbagliato: il thread con
`Simona.DiLiberti@gigroup.com` contiene due tuoi messaggi inviati ed è in inbox,
quindi quei thread esistono. **La query era formulata male** — va usata la forma
`from:me`, e verificata prima di costruirci sopra qualunque automazione.

Lo annoto perché ci stavo per appoggiare l'intera fase di protezione.

---

## 4. Un dettaglio tecnico utile

`resultCountEstimate` non è sempre tappato a 201: la ricerca sui mittenti di
sicurezza ha restituito **41**, un numero reale. Il tappo scatta sopra le ~200.
Quindi per qualunque insieme sotto quella soglia **il conteggio esatto è
ottenibile** — utile per misurare l'effetto dei filtri prima di applicarli.

---

## 5. Perché non ho fatto niente

Tutte le operazioni di scrittura sulla casella sono bloccate in questa sessione:
sei tentativi di `create_label`, tutti respinti con richiesta di approvazione che
non passa. Stessa cosa per la creazione della Routine.

Le letture funzionano. Le scritture no. Quindi: analisi completa, esecuzione zero.
