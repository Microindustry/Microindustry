# AGENTS.md — TITANIUM_OS

> **Questo file è la FONTE UNICA delle regole.**
> `CLAUDE.md`, `BRAIN/RULES.md`, `DASHBOARD/AGENTS.md` e `DASHBOARD/.cursorrules`
> sono **derivati** da qui con `python AUTOMATIONS/tools/sync_regole.py`.
> Per cambiare una regola si cambia questo file. Mai i derivati.

Formato [AGENTS.md](https://agents.md/) — standard della Agentic AI Foundation
(Linux Foundation), letto da Claude Code, Cursor, Copilot, Windsurf, Aider, Zed,
VS Code e JetBrains. Gli agenti leggono il file **più vicino** nell'albero delle
cartelle: `DASHBOARD/AGENTS.md` vince dentro `DASHBOARD/`, questo vince ovunque
altrove. La specificità si ottiene con la cascata, **non duplicando**.

---

## CHE COS'È QUESTO PROGETTO

TITANIUM_OS è il sistema operativo personale di Matteo Benenati — artigiano
industriale, 15 anni di officina, costruttore della fresatrice CNC **V32**.
Il sistema gestisce la costruzione di sé stesso (regola 5).

Pilastri: **V32** (fresatrice 3 assi) · **GENESIS** (ecosistema AI) ·
**MIMS** (sistema modulare d'acciaio) · **VITA NATURA** (centro estetico).

---

## LE 12 REGOLE — TITANIUM_OS OPERATING PRINCIPLES

> *Un sistema che gira da solo vale più di 10 abitudini che dipendono dalla volontà.*

**La numerazione 1-10 non cambia mai:** mezzo repo cita "regola N".

1. **Niente è finito — ogni cosa è una versione.**
   Non aspettare la perfezione. Una versione funzionante oggi > una versione perfetta mai.

2. **Identifica → Automatizza → Scala.**
   Se lo fai 3 volte: script. Se lo fai ogni giorno: nodo. Se il nodo produce valore: scala.

3. **Cattura mentre costruisci — non ricordare, documenta.**
   Ogni decisione tecnica in `MENTE/`. Ogni sessione Claude in `MENTE/SESSIONI/`. Il RAG la recupera domani.

4. **Leva cognitiva: 1 input → N output.**
   Un milestone → episodio + reel + LinkedIn + RAG update. Ogni azione deve produrre più artefatti.

5. **Costruisci ciò che usi — meta-ricorsività.**
   TITANIUM_OS gestisce la costruzione di TITANIUM_OS. Il sistema si autoalimenta.

6. **Output misurabile prima di tutto.**
   Se non posso misurarlo (mm, ore, euro, chunk RAG, commit), non esiste.

7. **Tutto si connette — nessun silo.**
   V32 → episodio → dataset LLM → RAG → Claude più informato su V32. Il loop è intenzionale.

8. **Proteggi il sapere.**
   `_VAULT/` per i segreti. RAG per la conoscenza. Git per il codice. Backup AES-256 per tutto.

9. **Reinvesti il margine — 60% anno 1.**
   BEP V32 = 61 ore. Ogni ora sopra il BEP è reinvestita in strumenti, formazione, scala.

10. **Libertà sopra profitto.**
    Il capannone entro 2030 non è un obiettivo lavorativo — è un obiettivo di sovranità.

11. **Il sistema PROPONE, l'umano APPROVA.**
    Nessun agente modifica codice, chiavi o canone da solo: scrive una proposta, decide Matteo.
    **Eccezione a canone:** la corsia Nina è AUTO — genera e auto-promuove da sola (#44).

12. **Insegna ciò che impari.**
    Spiegare forza la chiarezza (effetto Feynman): se non sai raccontarlo, non l'hai capito.
    Ogni concetto tecnico diventa un episodio, un carosello, un post.

---

## FATTI E NON-FATTI — leggere prima di scrivere numeri

Questa sezione esiste perché la sessione #70 (16/08/2026) ha dovuto rimuovere
numeri inventati che erano stati spacciati per FATTI, e una fonte fabbricata che
non è mai esistita. Il costo è stato una sessione intera di bonifica su 16 file.

**Regole per qualunque agente che scrive su questo repo:**

1. **Un numero senza misura non si scrive.** Massa, frequenza, tolleranza, resa,
   percentuale: se non c'è una misura o un calcolo tracciabile alle spalle, non
   entra nel testo. Meglio vuoto che inventato.
2. **"Numero di progetto" ≠ "misura".** La qualifica fa parte del dato e non si
   perde mai per strada, in nessun file, nemmeno in quelli che istruiscono altri
   agenti. Numeri di progetto noti: **massa V32 178 kg**, **±0,019 mm RSS**,
   **BEP 61 ore**, **tariffa 45 €/h**. Sorvegliati da `canon_guard.scan_public()`
   e da `GUIDA §7.7`: mai presentati come fatti sulla superficie pubblica.
   Scrivere "178 kg" senza "di progetto" è già una violazione.
3. **Stato reale della V32, ad oggi:** un **telaio in piedi**, in acciaio saldato
   TIG, corpo unico, 3 assi, con la componentistica scelta. Le prestazioni della
   macchina le dirà la macchina quando potrà dimostrarle.
4. **Non saldare i pilastri.** Scrivere "GENESIS/V32" come soggetto unico è
   sempre sbagliato, qualunque verbo segua (regola strutturale `[pilastri-fusi]`).
5. **MIMS non è software.** È il sistema modulare d'acciaio. L'ecosistema AI si
   chiama GENESIS. Confonderli ha contaminato il RAG una volta.
6. **Le percentuali dei pilastri sono metriche di gestione interna**, lette da
   `BRAIN/STATE.json`. Non sono avanzamento fisico e non vanno presentate come tale.

---

## REGOLE CODICE (non negoziabili)

Header obbligatorio in ogni file Python:

```python
# nome_modulo.py | TITANIUM_OS / NODO / SOTTOSISTEMA | vX.Y | YYYY-MM-DD
```

I path si derivano, non si scrivono a mano:

```python
BASE = Path(__file__).resolve().parents[N]     # sì
"C:\\Users\\benen\\..."                        # MAI: rompe su altre macchine
```

---

## DOVE VA OGNI FILE

Non inventare percorsi. La mappa completa è in `CLAUDE.md` §FILESYSTEM,
che è derivato da questo repo e resta la tabella di riferimento operativa.

---

## FONTI DI VERITÀ

| Cosa | Fonte | Note |
|------|-------|------|
| Regole | **questo file** | tutto il resto è derivato |
| Stato del sistema | `BRAIN/STATE.json` | verificare `last_update` prima di citarlo |
| Cose da fare | `DA_FARE_FATTO.md` + `DATA/audit/bussola_todos.json` | la BUSSOLA |
| Azioni non delegabili | `AZIONI_MATTEO.md` | solo Matteo |
| Salute del sistema | `CRITICHE.md` | la cartella clinica |
| Regole grafiche | `BRAIN/REGOLE_GRAFICHE.md` | specifiche, non duplicare qui |

**Prima di citare un dato, guarda quanto è vecchio.** Un dato vecchio va
etichettato come vecchio, mai presentato come attuale.
