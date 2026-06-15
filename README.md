## Matteo Benenati — Microindustry

```
╔══════════════════════════════════════════════════════════════╗
║  ARTIGIANO INDUSTRIALE + SYSTEM BUILDER                      ║
║  15 anni di officina. Titanio, robot, presse, CNC da zero.  ║
║  Il codice è la mia seconda officina.                        ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Chi sono

Non vengo dal software. Vengo dall'officina.

Ho saldato scarichi in titanio per le moto del MotoGP da **SCProject**. Ho programmato robot **ESSEGI** per linee di packaging industriale. Ho operato presse **DATWLER** e fatto QC su impianti di refrigerazione **LU.VE**. Ho costruito macchine con le mani per 15 anni prima di scrivere la prima riga di codice seria.

Quando ho iniziato a costruire la mia fresatrice CNC da zero — **178 kg, struttura corpo unico in acciaio saldato TIG, 3 assi, ±0.019 mm** — ho capito che avevo bisogno di un sistema per non perdere il filo. Da lì è nato TITANIUM_OS.

Nessuna laurea. Solo proof-of-work reali.

---

## TITANIUM_OS — Il sistema operativo della mia vita

> *Un sistema che gira da solo vale più di 10 abitudini che dipendono dalla volontà.*

**TITANIUM_OS** è il sistema che costruisco mentre costruisce me. Ogni nodo elimina un carico mentale. Ogni automazione libera energia per il lavoro fisico.

### Stato Live — v1.1.0 | Sessione #54 | 15 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #37: rifare le STORIE a 2 ASSI (RUOLO+NINA) rebuild-safe integrati coi N-livelli sui contenuti (parent/level/children) + Mappa di Nina percorribile data-driven dall asse_nina (Regioni 0-7, +verticale FINANZA) + ARCO NINA COMPLETO 8/8 (EP_AV_M0 Materia ... EP_AV_06 Direttore) + canon BIBBIA 0-ter (Nina ha il suo OS) + indice PIETRE auto-generato + FATTI(per il RAG) sui 4 semi. 153 ep, build TS verde, ~14 commit isolati.
**Prossimo step:** Approvare UAC del restart API (RAG torna 200). Poi: FINANZA reg2 "Spendere meno di quanto entra" (open loop pronto). FOCUS: usare Fable 5 (entro 22/06) per SELF_IMPROVE/red-team (audit critico 360 + migliorie prioritizzate, proposte PR mai merge auto su main). Decisioni aperte: scalare asse_nina ai 129, viste 2 assi in dashboard, Nina 0 MATERIA gia fatto (EP_AV_M0).

---

### Nodi GENESIS attivi

| Nodo | Descrizione |
|------|-------------|
| `MCP Server` | 5 tool Claude — get_state, search_mente, update_milestone |
| `MENTE RAG v4.0` | ChromaDB hybrid BM25+semantic+CrossEncoder — 6000+ chunk |
| `Story Agent` | Genera episodi narrativi dai commit git (02:07 ogni notte) |
| `Research Agent` | Cerca paper su 13 sorgenti (arXiv, Semantic Scholar, GitHub...) |
| `Computer Use` | Controllo desktop via Anthropic API — screenshot+click+tastiera |
| `Daily Brief` | Briefing quotidiano 07:30 |
| `API Server` | Flask localhost:5001 — media, foto, agenti, RAG |
| `Dashboard v7.0` | React+Vite — sidebar + AgentsView + dot grid |
| `Personal LLM` | Fine-tuning TinyLlama-1.1B sui miei episodi (domenica notte) |

---

### Ultimi 5 milestone verificati
- Mappa di Nina percorribile a LV illimitati, data-driven dall asse_nina: Regioni 0-7 (Tech) + verticale FINANZA (1-4) si popolano da sole; rinominata Mappa, mappa di sistema -> ARCHITETTURA (11/06)
- ARCO NINA COMPLETO 8/8: EP_AV_M0 Materia, AV_00 Loop, 01 Automazione, 02 LLM, 03 RAG, 04 Wiki, 05 Agenti, 06 Orchestrazione; +EP_AV_FIN_01 Il Valore (verticale finanza) (11/06)
- Canon BIBBIA 0-ter: Nina ha il suo OS (si perde come Matteo, glielo costruisce il papa-meccanico; la Mappa E l OS di Nina) (11/06)
- Indice PIETRE.md auto-generato (Tech+Finanza) + blocco FATTI(per il RAG) sui 4 semi + riflusso MENTE/KNOWLEDGE/genesis_nodi_fatti.md (11/06)
- Fix crash dashboard: rimossa MAPPA_RADICE (ReferenceError TDZ, usava REGIONI prima dell init); radice ora data-driven in buildMappa (11/06)

### Episodi recenti
- *Prima la Mano, Poi la Macchina*
- *La Mappa Viva*
- *Mille Volte Uguale*
- *Il Soffio di Troppo*
- *La Bambina che Chiedeva Perché*

---

### Stack

```
Python 3.11 · ChromaDB · SentenceTransformer · Flask · MCP
React + Vite · Tailwind · n8n · Claude API · Windows 10
LLaMA-Factory · PyAutoGUI · Anthropic Computer Use API
```

---

### Obiettivo 2030

**Capannone artigianale proprio** — 15 Luglio 2030.
Non è un obiettivo lavorativo. È un obiettivo di sovranità.

BEP V32: **61 ore = 1.4 mesi** | ROI Anno 1: **322%** | Tariffa: **EUR 45/h**

---

*Aggiornato automaticamente ogni notte da TITANIUM_OS · TI_NightPush 04:07*
