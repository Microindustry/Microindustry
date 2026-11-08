# Tre comandi rapidi — gestione personale

Generati il 27/08/2026. **File veri, importabili.** Non riguardano la V32 né i
progetti: servono a te.

---

## ⚠ Leggi questo prima

**Non ho potuto provarli.** Sono costruiti secondo il formato di Apple e riletti
correttamente come plist validi, ma **non ho un iPhone su cui eseguirli**. Gli
identificatori delle azioni vengono dal formato documentato, non da una prova.

Per come ho lavorato tutto il giorno — provare prima di consegnare — questa è
l'eccezione, e va detta. Se uno non si importa o dà errore, **in fondo c'è la
ricetta manuale**: si rifà a mano in novanta secondi, e in più impari lo
strumento.

**Prima di importare:** Impostazioni → Comandi Rapidi → **Consenti comandi rapidi
non attendibili**. Compare solo dopo che ne hai eseguito almeno uno, quindi apri
l'app e lancia un comando qualsiasi prima.

**Crea prima due note** in Note, vuote, chiamate esattamente **`Cattura`** e
**`Diario`**: due dei comandi ci scrivono dentro.

---

## 1. `Scadenza` 🟠

**Il problema che risolve.** Nella tua casella ci sono tre avvisi *"bolletta in
scadenza"* mai aperti — A2A luce il 07/07 con scadenza l'08/07, luce il 06/05
con scadenza il 07/05, gas il 16/04. Più i promemoria acqua di Gruppo CAP,
marcati importanti. Gli avvisi arrivano. Il punto è che non li vedi.

Questo comando sposta il momento in cui la scadenza esiste: **da quando te ne
accorgi, a quando ti sarà utile saperlo.**

```
Chiedi "Cosa scade?"  →  Chiedi "Quando?"  →  Promemoria con avviso  →  Conferma
```

Lo lanci quando una scadenza ti passa davanti — da Siri, dal widget, dal
pulsante Azione — e il promemoria suona da solo quando serve.

## 2. `Nota veloce` 🟢

**Il problema che risolve.** Le cose che ti vengono in mente con le mani sporche
non hanno un posto dove cadere: o le ricordi, o le perdi.

```
Detta (italiano)  →  Aggiungi alla nota "Cattura"  →  Conferma
```

Non tocchi lo schermo. *"Ehi Siri, Nota veloce"*, parli, è salvato.

## 3. `Fine giornata` 🟣

```
"Cosa ho chiuso oggi?"  →  "La prima cosa di domani?"
   →  scrive entrambe nella nota "Diario"
   →  crea il promemoria di domani
```

Due domande, trenta secondi. Chiude la giornata e apre quella dopo. È la regola 3
applicata a te invece che al codice: **non ricordare, documenta.**

---

## Come renderli comodi

- **Siri**: funzionano già col nome. *"Ehi Siri, Scadenza"*.
- **Pulsante Azione** (se il tuo iPhone ce l'ha): assegnalo a `Nota veloce`.
  È il gesto più corto fra un pensiero e un posto dove tenerlo.
- **Automazione serale**: Comandi Rapidi → Automazione → Ora del giorno → 21:00
  → `Fine giornata`. Togli "Chiedi prima di eseguire" e parte da solo.
- **Widget** in schermata home per `Scadenza`.

---

## Ricette manuali — se l'importazione non va

Ognuna è di tre o quattro azioni. Nuovo comando rapido → cerca l'azione per nome
→ aggiungi.

### Scadenza
1. **Chiedi input** — Prompt: `Cosa scade?` · Tipo: **Testo**
2. **Chiedi input** — Prompt: `Quando?` · Tipo: **Data**
3. **Aggiungi nuovo promemoria** — Titolo: `SCADE:` + variabile del passo 1 ·
   Avviso: **attivo**, data = variabile del passo 2
4. **Mostra notifica** — `Promemoria creato`

### Nota veloce
1. **Detta testo** — Lingua: Italiano
2. **Aggiungi alla nota** — Nota: `Cattura` · Input: il testo dettato
3. **Mostra notifica** — il testo dettato

### Fine giornata
1. **Chiedi input** — `Cosa ho chiuso oggi?` · Testo
2. **Chiedi input** — `La prima cosa di domani?` · Testo
3. **Aggiungi alla nota** — Nota: `Diario` · Input: `FATTO: ` + passo 1 +
   a capo + `DOMANI: ` + passo 2
4. **Aggiungi nuovo promemoria** — Titolo: variabile del passo 2

---

## Perché questi tre e non altri

Non li ho scelti a caso né per fare numero. Vengono da quello che ho misurato
oggi nella tua casella e nel tuo repo:

- **`Scadenza`** perché le scadenze ti arrivano e non le vedi — dimostrato, con
  le date.
- **`Nota veloce`** perché passi le giornate con le mani occupate, e le sessioni
  sono memoria volatile: quello che non è fissato non esiste.
- **`Fine giornata`** perché il tuo `STATE.json` è fermo dal 16 agosto. Il
  sistema non si aggiorna da solo quando chiudi una sessione — e nemmeno tu.
  Trenta secondi la sera valgono più di una ricostruzione a settimana.

Nessuno dei tre tocca la V32, GENESIS o la bussola. Quelli hanno già i loro nodi.
