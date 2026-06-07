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

### Stato Live — v1.1.0 | Sessione #34 | 07 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #32: P1a fatto (AUTOMAZ a stato reale+live) · leva locale Ollama/Qwen ACCESA (model_ready=true) · P2 binario AVVENTURA lanciato (bibbia del mondo + pilota EP_AV_00 'La Bambina e la Giuntura', stagione AV). Tutto committato, build verde.
**Prossimo step:** P2: EP_AV_01..04 (bozza su Qwen/M3, rifinitura) · collegare Critiche=quest e MAPPA=mondo · P1c livelli da progressi reali · cablare MiniMax M3 nel toggle chat (serve key OpenRouter in _VAULT). ANOMALIA TI_NightAudit: RISOLTA (gira @03:52 OK).

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
- n8n self-hosted attivo (account locale, no cloud) + pnpm installato; avvio al login operativo (03/06/2026)
- Vista METODO sul sito — spiegazione chi/cosa/come del sistema, nata dalle domande di un dev esterno (03/06/2026)
- Automazioni notturne portabili: _ti_paths.bat (resolver TI_ROOT/PYTHON/GH no-hardcode), night_research/push/finetune + story_agent de-Getac, finetune GPU/fp16 + guard llamafactory, register_night_tasks.ps1 con auto-UAC (03/06/2026)
- Notturne ottimizzate + self-audit: RAG CANONE vs RICERCA (-448 chunk garbage purgati), gate rilevanza ricerca (--min-rel), topic puliti, night_audit.py su Sonnet genera cartella clinica automatica (DATA/audit), TI_NightAudit @03:52 (05/06/2026)
- P1a il grosso: view AUTOMAZ riscritta con stato operativo reale (persistente/event/scheduled/on-demand/dormiente) + badge live da /api/watchdog/status e /api/tasks/notturne; ~14 file 'da creare' erano falsi (esistono su disco), 5 sottostimati event-driven corretti; anomalia TI_NightAudit risolta (gira @03:52 OK). Commit 5f148a7+b70b4e2, build verde (06/06/2026)

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
