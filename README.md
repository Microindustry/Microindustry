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

### Stato Live — v2.8.0 | Sessione #15 | 30 May 2026

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `████████░░ 83%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Config G - Rinforzi colonne Z+U
**Prossimo step:** Saldare 4 gusset 200mm sulla colonna Z sinistra

---

### Nodi GENESIS attivi

| Nodo | Descrizione |
|------|-------------|
| `MCP Server` | 8 tool Claude — get_state, search_mente, update_milestone, update_session_context |
| `MENTE RAG v4.0` | ChromaDB hybrid BM25+semantic+CrossEncoder — 6000+ chunk |
| `Story Agent` | Genera episodi narrativi dai commit git (02:07 ogni notte) |
| `Research Agent` | Cerca paper su 13 sorgenti (arXiv, Semantic Scholar, GitHub...) |
| `NEXUS Swarm` | Orchestratore agenti paralleli — ThreadPoolExecutor + RAG graph 114 nodi |
| `Daily Brief` | Briefing quotidiano 07:30 |
| `API Server` | Flask localhost:5001 — media, foto, agenti, RAG |
| `Dashboard v7.0` | React+Vite — sidebar + AgentsView + dot grid |
| `Personal LLM` | Fine-tuning TinyLlama-1.1B sui miei episodi (domenica notte) |

---

### Open source tools

Parts of TITANIUM_OS extracted as standalone tools:

| Tool | What it does |
|------|-------------|
| [`hybrid-rag`](https://github.com/Microindustry/hybrid-rag) | Local hybrid RAG: ChromaDB + BM25 + CrossEncoder reranker. No cloud. |
| [`git-narrator`](https://github.com/Microindustry/git-narrator) | Turns git history into structured narrative episodes. Runs nightly. |
| [`multi-source-research`](https://github.com/Microindustry/multi-source-research) | Search arXiv, Semantic Scholar, GitHub and 10 more sources in one command. |
| [`claude-session-bridge`](https://github.com/Microindustry/claude-session-bridge) | Persistent context across Claude Code sessions via auto-generated resume file. |

---

### Ultimi 5 milestone verificati
- NEXUS swarm orchestrator v1.0 + RAG graph-aware v5.0 (114 nodi, 218 archi) (30 Mag 2026)
- Session continuity system — RIAVVIO_SESSIONE.txt + stop hook + MCP update_session_context (30 Mag 2026)
- Dashboard v7.0 - sidebar verticale collassabile + AgentsView glassmorphism + dot grid (29 Mag 2026)
- Story Agent v1.0 - generazione episodi automatica da git log, cron 02:07 + stop hook (29 Mag 2026)
- Logging centralizzato - CORE/log.py + 34 file aggiornati, RotatingFileHandler DATA/logs/ (29 Mag 2026)

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
