# Migrazione a AGENTS.md — istruzioni operative

Preparato dalla sessione mobile del 27/08/2026. **Nulla di questo è stato applicato
a TITANIUM_OS**: l'accesso in scrittura a quel repo è stato negato dal classificatore
di sicurezza della modalità auto. Questi file sono pronti da copiare.

---

## 1. Perché AGENTS.md e non "un altro file di regole"

Oggi le regole vivono in almeno **dieci** posti. Nella #70 ne hai unificati tre.
Restano divergenti, tra gli altri: `DASHBOARD/.cursorrules`,
`BRAIN/KNOWLEDGE/system/rules/` (quattro file), `BRAIN/ECOSYSTEM_MANIFEST.md`,
`DASHBOARD/src/data/sistema_linea_guida.md`.

`AGENTS.md` risolve il problema alla radice per due proprietà:

- **Un solo file letto da tutti gli agenti.** Claude Code, Cursor, Copilot,
  Windsurf, Aider, Zed, VS Code, JetBrains. Oggi Cursor legge una verità e Claude
  ne legge un'altra.
- **Cascata sull'albero delle cartelle**, come `.gitignore`: vince il file più
  vicino. `DASHBOARD/` ottiene le sue regole specifiche **senza duplicare** quelle
  della radice — e duplicare è esattamente come è nata la divergenza della #70.

---

## 2. I file

| File preparato | Va salvato in TITANIUM_OS come |
|---|---|
| `AGENTS.md` | `/AGENTS.md` |
| `DASHBOARD-AGENTS.md` | `/DASHBOARD/AGENTS.md` |

Dopo la migrazione, la catena diventa:

```
AGENTS.md  (FONTE UNICA)
   ├─→ CLAUDE.md §LE REGOLE      derivato, fra marcatori
   ├─→ BRAIN/RULES.md            derivato, fra marcatori  (già così oggi)
   └─→ DASHBOARD/.cursorrules    derivato, puntatore
```

---

## 3. Il motivo per cui `.cursorrules` va sostituito subito

Non è una questione di ordine. `DASHBOARD/.cursorrules` contiene, sotto un titolo
che dice letteralmente **"PROJECT CONTEXT (THE TRUTH)"**:

```
Titanium V32: A CNC machine built with Epoxy Granite.
Critical stats: 178kg mass, 3.83Hz nat freq.
```

> **Nota di metodo.** La prima stesura di questa sezione diceva che quei numeri
> erano inventati e che il materiale contraddiceva il canone. Un `grep` sul repo
> mi ha smentito su entrambi i punti, e li ho ritirati. Quello che resta sotto è
> ciò che regge alla verifica.

**Cosa dice davvero il repo:**

- `CLAUDE.md:107` → *"Massa V32: 178 kg **di progetto** — **corpo unico**"*.
  Il numero è nel canone, con la qualifica esplicita.
- `canon_guard.py:13` → *"scan_public(): numeri di PROGETTO non ancora misurati
  (massa 178 kg, …)"*. Il guardiano **conosce** questo numero e lo sorveglia.
- `update_github_profile.py:4` → *"canone GUIDA §7.7 — MAI numeri di progetto
  come fatti (178kg/±0,019 tolti…)"*. Nella #61 li hai già rimossi dal profilo
  pubblico proprio per questa ragione.
- *Epoxy Granite* è nel canone del progetto: compare in `EP_02 — IL REATTORE`
  ("Epoxy Granite: Colata Zero"), nella saga Config A→G e in `night_topics.py`.
  **Non è una contraddizione.**

**I problemi che restano, verificati:**

1. **La qualifica è sparita.** `.cursorrules` scrive `178kg mass` sotto
   *"THE TRUTH"*, senza il *"di progetto"* che `CLAUDE.md` porta e che
   `GUIDA §7.7` impone. Nella #61 hai tolto quel numero dal profilo pubblico per
   non spacciarlo per misura: in `.cursorrules` è rimasto, e senza qualifica.
   Un agente che legge "THE TRUTH" lo tratta come misurato.
2. **`3.83Hz nat freq` non ha fonte.** Cercato in tutto il repo — `.md`, `.json`,
   `.ts`, `.py` — compare **solo** in questo file. Nessun "di progetto", nessun
   calcolo alle spalle, nessuna misura. È l'unico numero davvero scoperto.
3. **`canon_guard` non guarda qui.** `scan_public()` sorveglia la superficie
   pubblica e gli episodi. `.cursorrules` non è mai passato sotto nessun gate —
   ed è il file che istruisce un agente *diverso da Claude*, che scrive codice
   nella dashboard.
4. **Identità divergente.** Il file assegna a Cursor il ruolo di *"Lead Engineer
   for Titanium Ventures"* con obiettivo *"ASSOLUTO V3.0"*, mentre il repo è
   Microindustry e il documento di riferimento è ASSOLUTO V6.

Il guasto vero, quindi, non è "un numero inventato": è che **la disciplina che
hai costruito sui numeri di progetto non si applica ai file che istruiscono gli
altri agenti**. Il canone si ferma dove inizia Cursor.

### Sostituzione proposta

`DASHBOARD/.cursorrules` diventa un puntatore derivato, generato dallo script:

```
# DERIVATO — non editare a mano.
# Fonte unica: /AGENTS.md (radice) + /DASHBOARD/AGENTS.md
# Rigenerato da: python AUTOMATIONS/tools/sync_regole.py
#
# Le regole di questo progetto stanno in AGENTS.md, che Cursor legge
# nativamente. Questo file esiste solo per le versioni di Cursor che
# ancora cercano .cursorrules.
#
# NON scrivere qui numeri, materiali o prestazioni della V32:
# i fatti verificati stanno in /AGENTS.md §FATTI E NON-FATTI.
```

---

## 4. Patch a `sync_regole.py`

Lo script funziona già ed è ben fatto: estrae le regole con
`SEZIONE_RX` / `REGOLA_RX`, scrive fra marcatori, è idempotente e ha `--check`
per il gate notturno. **Serve solo cambiare la sorgente e aggiungere i target.**

Oggi (righe 23-28):

```python
BASE = Path(__file__).resolve().parents[2]
SORGENTE = BASE / "CLAUDE.md"
DERIVATO = BASE / "BRAIN" / "RULES.md"

INIZIO = "<!-- REGOLE:start (derivato da CLAUDE.md — non editare a mano) -->"
FINE = "<!-- REGOLE:end -->"
```

Dopo:

```python
BASE = Path(__file__).resolve().parents[2]
SORGENTE = BASE / "AGENTS.md"
DERIVATI = [
    BASE / "BRAIN" / "RULES.md",
    BASE / "CLAUDE.md",
]

INIZIO = "<!-- REGOLE:start (derivato da AGENTS.md — non editare a mano) -->"
FINE = "<!-- REGOLE:end -->"
```

Poi `main()` cicla su `DERIVATI` invece di lavorare sul singolo `DERIVATO`.
Il resto — estrazione, rendering, `--check`, rimozione del TOC — resta identico.

**Vincolo da rispettare:** `AGENTS.md` deve mantenere il titolo di sezione
`## LE 12 REGOLE — ...` e chiudere con `---`, perché `SEZIONE_RX` cerca
esattamente quello. Il file preparato lo rispetta.

**Attenzione a un dettaglio.** `CLAUDE.md` diventa derivato **solo nella sezione
regole**, fra i marcatori. Tutto il resto (FILESYSTEM, DATI MASTER, SETUP MACCHINA,
PERSONAGGI AI) resta scritto a mano e non va toccato — esattamente come oggi
`sync_regole.py` lascia intatta la sezione PDF_TO_MEMORY di `RULES.md`.

---

## 5. Ordine di esecuzione

1. Copiare `AGENTS.md` nella radice di TITANIUM_OS.
2. Copiare `DASHBOARD-AGENTS.md` in `DASHBOARD/AGENTS.md`.
3. Inserire i marcatori `REGOLE:start` / `REGOLE:end` attorno alla sezione regole
   di `CLAUDE.md`.
4. Applicare la patch a `sync_regole.py`.
5. Eseguire `python AUTOMATIONS/tools/sync_regole.py` e verificare che
   `BRAIN/RULES.md` e `CLAUDE.md` risultino invariati nel contenuto delle regole
   (devono esserlo: il testo è stato copiato verbatim).
6. Eseguire `python AUTOMATIONS/tools/sync_regole.py --check`: deve uscire 0.
7. Sostituire `.cursorrules` col puntatore del §3.
8. Agganciare `--check` al gate notturno, se non c'è già.

**Verifica finale:** `grep -rn "178kg\|3.83Hz\|Epoxy Granite" .` deve tornare vuoto
fuori dai file storici e dagli episodi.

---

## 6. Cosa resta aperto

Le altre sedi di regole non le ho toccate. Vanno classificate una per una —
**legge**, **appunto** o **derivata**:

```
BRAIN/ECOSYSTEM_MANIFEST.md
BRAIN/SCALA-GENESIS.md
BRAIN/KNOWLEDGE/system/rules/lex-digitalis.md
BRAIN/KNOWLEDGE/system/rules/ai-behavior.md
BRAIN/KNOWLEDGE/system/rules/neuro-sincrono.md
BRAIN/KNOWLEDGE/system/rules/documentation-rules.md   ← fermo alla v1.0 del 10/03/2026
DASHBOARD/src/data/sistema_linea_guida.md
```

`BRAIN/REGOLE_GRAFICHE.md` **non** va fuso: è legittimamente specifico ed è già
richiamato da `DASHBOARD/AGENTS.md`.

---

## 7. AGGIORNAMENTO 27/08 — la patch esiste ed è stata provata

I §4 e §5 qui sopra descrivevano la migrazione a parole. **Ora è codice, costruito
ed eseguito sul clone reale di TITANIUM_OS.**

### Il file

```
proposta-regole/migrazione-agents-md.patch     571 righe, 6 file
```

| File | Cosa cambia |
|---|---|
| `AGENTS.md` | **nuovo** — fonte unica, 143 righe |
| `DASHBOARD/AGENTS.md` | **nuovo** — regole dashboard, 60 righe |
| `AUTOMATIONS/tools/sync_regole.py` | v1.0 → v2.0: sorgente AGENTS.md, lista di derivati, due formati di resa |
| `CLAUDE.md` | la sezione regole diventa derivata, fra marcatori |
| `BRAIN/RULES.md` | marcatori aggiornati, resta derivato come prima |
| `DASHBOARD/.cursorrules` | sostituito da un puntatore, senza numeri |

### Come si applica

```bash
cd <percorso-TITANIUM_OS>
git checkout -b claude/regole-agents-md
git apply migrazione-agents-md.patch
python AUTOMATIONS/tools/sync_regole.py --check    # deve uscire 0
```

### Cosa ho verificato davvero, non a occhio

- `py_compile` sullo script: OK.
- Prima esecuzione: rigenera entrambi i derivati.
- Seconda esecuzione: *"già allineato"* su entrambi → **idempotente**.
- `--check`: **exit 0**.
- **12 regole** presenti sia in `CLAUDE.md` sia in `BRAIN/RULES.md`.
- Le **annotazioni storiche delle regole 11 e 12** — quelle che la #70 aveva
  faticato a recuperare — sopravvivono in entrambi i derivati.
- Il **TOC di `CLAUDE.md` resta intatto**.
- Patch applicata da capo su un repo pulito: `git apply --check` OK, e il gate
  passa anche dopo la riapplicazione.

### Tre difetti che ho trovato provandola, e corretto

Li scrivo perché sarebbero passati inosservati fino al PC.

1. **Spogliavo `CLAUDE.md` del suo TOC.** Il `re.sub` che toglie il TOC era stato
   scritto per `RULES.md`, dove l'indice copriva solo le regole. In `CLAUDE.md`
   l'indice copre **tutte e 12 le sezioni**: toglierlo distruggeva la navigazione
   di roba che non c'entra niente con le regole. Ora la rimozione avviene solo sui
   derivati in formato `titoli`.
2. **Il mio `AGENTS.md` aveva tagliato le annotazioni delle regole 11 e 12** — la
   nota su `SELF_IMPROVE` propose-only e quella sul recupero da `RULES.md`. Cioè
   esattamente il testo che la #70 aveva rimesso dopo che era sparito il 20/06.
   Ripristinato integralmente.
3. **Indentazione e accenti.** Le regole a due cifre usano 4 spazi, non 3, e
   l'epigrafe l'avevo riscritta con gli apostrofi (`piu'`, `volonta'`) invece degli
   accenti. Ora l'indentazione si calcola dalla larghezza del numero e il testo è
   quello originale.

**Un falso allarme, per onestà:** avevo scritto che `CLAUDE.md` perdeva una
sezione `##`. Non era vero — avevo contato male io. Il diff delle intestazioni è
vuoto: sono identiche.

### Cosa NON contiene

La classificazione delle altre sedi di regole (§6). Quelle vanno guardate una per
una insieme: non è lavoro da patch.
