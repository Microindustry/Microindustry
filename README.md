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

### Stato Live — v1.1.0 | Sessione #31 | 06 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione autonoma #31: P4a chat RAG + P4b leva locale + P1b cartella clinica viva + audit agenti P5 (tutto committato, build verde)
**Prossimo step:** DECISIONI MATTEO: (1) installare Ollama + `ollama pull qwen2.5:7b-instruct-q4_K_M` per accendere leva locale · (2) restart api_server (SERVICES/restart_api.ps1) per endpoint live · (3) prune roster agenti (AGENTS_AUDIT.md: aqua/plc) · LAVORO: P1a AUTOMAZ a livelli+stato live · P1c livelli da progressi reali · P2 storia-avventura

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
- Firewall 5173 aperto + Tailscale loggato sul fisso (100.125.152.124) — dashboard via LAN e da remoto (03/06/2026)
- n8n self-hosted attivo (account locale, no cloud) + pnpm installato; avvio al login operativo (03/06/2026)
- Vista METODO sul sito — spiegazione chi/cosa/come del sistema, nata dalle domande di un dev esterno (03/06/2026)
- Automazioni notturne portabili: _ti_paths.bat (resolver TI_ROOT/PYTHON/GH no-hardcode), night_research/push/finetune + story_agent de-Getac, finetune GPU/fp16 + guard llamafactory, register_night_tasks.ps1 con auto-UAC (03/06/2026)
- Notturne ottimizzate + self-audit: RAG CANONE vs RICERCA (-448 chunk garbage purgati), gate rilevanza ricerca (--min-rel), topic puliti, night_audit.py su Sonnet genera cartella clinica automatica (DATA/audit), TI_NightAudit @03:52 (05/06/2026)

### Episodi recenti


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
