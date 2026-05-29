## Matteo Benenati — Microindustry

```
╔══════════════════════════════════════════════════════════════════════╗
║  ARTIGIANO INDUSTRIALE + SYSTEM BUILDER                              ║
║  15 anni di officina. Titanio, robot, presse, CNC da zero.           ║
║  Il codice è la mia seconda officina.                                ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

### Chi sono

Non vengo dal software. Vengo dall'officina.

Ho saldato scarichi in titanio per le moto del MotoGP da SCProject. Ho programmato robot ESSEGI per linee di packaging industriale. Ho operato presse DATWLER e fatto QC su impianti di refrigerazione LU.VE. Ho costruito macchine con le mani per 15 anni prima di scrivere la prima riga di codice seria.

Quando ho iniziato a costruire la mia fresatrice CNC da zero — 178 kg, struttura corpo unico in acciaio saldato TIG, 3 assi, ±0.019 mm — ho capito che avevo bisogno di un sistema per non perdere il filo. Da lì è nato TITANIUM_OS.

Nessuna laurea. Solo proof-of-work reali.

---

### Il problema che ho risolto (in parole semplici)

Ogni mattina mi sedevo davanti al computer e non ricordavo esattamente dove eravamo rimasti. Quale vite avevo ordinato? Quella decisione sulle molle l'avevo presa o no? Ogni sessione perdevo tempo a ricostruire il contesto.

La soluzione ovvia sarebbe prendere appunti. Ma io dimentico anche di prendere appunti.

Allora ho costruito un sistema che si aggiorna da solo:

- **Ogni volta che finisco di lavorare** → il computer salva automaticamente decisioni, misure, prossimi step. Un diario che si scrive da solo.
- **Ogni volta che riapro** → l'AI legge quel file e sa già dove eravamo. Niente spiegazioni, si riparte.
- **Quando ho bisogno di ricordare qualcosa** → cerco nel sistema e lui trova il documento giusto tra centinaia di note. Come Google, ma solo per il mio progetto.
- **Quando completo un pezzo fisico** → il sistema lo trasforma in episodio podcast, post LinkedIn, reel. Una cosa fatta → più contenuti. Senza riscrivere niente.

---

### Processo evolutivo

| Periodo | Evento |
|---------|--------|
| 2008–2011 | Saldatura TIG titanio — scarichi MotoGP @ SCProject |
| 2012–2014 | Programmazione robot ESSEGI — packaging industriale |
| 2015–2023 | Operatore presse DATWLER · QC LU.VE refrigerazione · officina propria |
| Gen 2025 | TITANIUM_OS v1.0 — scaffolding Python + STATE.json + prime automazioni |
| Feb 2026 | V32: 178 kg assemblati · HMI TP900 Comfort acquisito · 8 bronzine lavorate |
| Mar 2026 | TITANIUM_OS v2.1 → v3.2 — Dashboard React live, Content Engine, SINAPSI |
| Mag 2026 | **V32 — decisione corpo unico** (abbandonato sistema a molle) |
| Mag 2026 | **TITANIUM_OS v5.1** — MCP 5 tool · RAG 50+ chunk · Dashboard CommandBar |
| Mag 2026 | **ASSOLUTO V7** — documento master unico (10 ATTI, ~50K parole) |
| Mag 2026 | **RAG v4.0 hybrid** — BM25 + ChromaDB + CrossEncoder reranker, incrementale |
| Mag 2026 | **Research Agent v1.1** — 13 sorgenti (BASE, POLITesi, Unpaywall + preset ITA/MIMS) |
| Mag 2026 | **Stop Hooks orchestratore** — 3 hook paralleli, RAG detached (4.7s vs 45s+) |
| Mag 2026 | **Sistema Agenti** — 8 agenti validatori (TESLA, FORGE, AQUA, LEX, SIEMENS, THEMIS, ARIA, EVA) |

---

### Progetti attivi

**V32 — Fresatrice CNC 3 assi**
Struttura corpo unico 178 kg, tubolari acciaio S235 saldati TIG, viti a sfere SFU1605, servo Siemens, PLC S7-314C + HMI TP900 Comfort. Riempimento Epoxy Granite per smorzamento vibrazioni. Stato: `Config G — 65%`. Target: ±0.019 mm (IT6-IT7). Investimento: EUR 2.250 (100% componenti recupero).

**TITANIUM_OS — Sistema operativo cognitivo personale**
Dashboard React + Vite + Zustand + TanStack Query. MCP Server (5 tool Claude Code integrati). ChromaDB RAG v4.0 hybrid 2376+ chunk (IT/EN multilingue). API Flask + n8n. CommandBar Ctrl+K. Content Engine v2 — 10 episodi core + dataset JSONL. `v5.2 live`.

**MIMS — Micro-Industry Modular System**
Sistema modulare industriale con tile 190×190 mm, piastrine 40×40 mm, 3 giunti proprietari (Eco-Snap 0-tool, Quick-Twist 0-tool, Tech-Bolt). 7 materiali dallo stesso standard geometrico. Blue ocean: prezzo da EUR 30, vs Bosch/Item EUR 150+. MOQ zero. `Design completo — attende V32`.

**VULCAN — Pressa VCM per tiles MIMS**
Pressa 15 ton recupero industriale + Edwards RV3 vacuum + ROPEX termico. Processo VCM (Vacuum Compression Molding) proprietario — 18 step, 6 ricette polimeriche. Brevetto processo in pipeline. `Attende V32`.

**EVA — AI assistant per Vita Natura**
WhatsApp bot + Claude API per centro estetico (Boffalora sopra Ticino, MI). Gestione appuntamenti, FAQ automatiche, follow-up. `Setup API WhatsApp pending`.

---

### ASSOLUTO V7 — Documento Master

Il documento tecnico completo dell'ecosistema Titanium Ventures — 10 ATTI unificati in file singolo. Fisico + Digitale + Economico + Strategico.

📄 [`DOCS/ASSOLUTO/ASSOLUTO_V7.md`](DOCS/ASSOLUTO/ASSOLUTO_V7.md) — sorgente markdown  
📕 [`DOCS/ASSOLUTO/ASSOLUTO_V7.pdf`](DOCS/ASSOLUTO/ASSOLUTO_V7.pdf) — layout industriale (cover navy/brass, tabelle, code blocks)

```
ATTO I   — Il Presente (inventario, CV, laboratorio)
ATTO II  — L'Ecosistema (5 pilastri, 10 regole, modello economico)
ATTO III — V32 (specs, corpo unico, Config G, PLC, Epoxy Granite, BOM)
ATTO IV  — MIMS (geometria, 3 giunti, 7 materiali, analisi competitiva)
ATTO V   — Materiali e Produzione (VULCAN, VCM 18 step, 6 ricette)
ATTO VI  — GENESIS (MCP, RAG, Dashboard v5.2, EVA, Content Engine)
ATTO VII — Economia e Verdetto (BEP, ROI, Verdetto 3 assi, timeline 2026-2030)
ATTO VIII— Mercato (TAM EUR 4.2B, SAM EUR 180M, SOM Y3 EUR 350-550K, GTM)
ATTO IX  — Proprietà Intellettuale (3 brevetti, 6 trade secrets, 4 marchi)
ATTO X   — Media Strategy (Titanium Lab, 3 serie, 7 revenue stream)
```

---

### TITANIUM_OS — Architettura v5.2

```
TITANIUM_OS/
├── DASHBOARD/              React + Vite + Zustand + TanStack Query
│   ├── CommandBar          Ctrl+K — navigazione rapida nodi
│   ├── PillarProgress      5 pilastri live con % da STATE.json
│   ├── StorieView          10 episodi core + dataset JSONL
│   └── MatteoSection       skill tree · interessi · principi · 2030
├── MCP/                    titanium_mcp_server.py — 5 tool Claude Code
│   ├── get_state           → BRAIN/STATE.json live
│   ├── update_milestone    → aggiorna milestone/blockers
│   ├── search_mente        → query RAG ChromaDB ibrido
│   ├── get_daily_brief     → brief formattato
│   └── list_content_ready  → episodi pronti produzione
├── NODES/
│   ├── MENTE_RAG/          RAG v4.0 hybrid: BM25+ChromaDB+CrossEncoder reranker
│   │                       2376+ chunk · paraphrase-multilingual · incrementale
│   ├── MENTE_SCANNER/      818+ estrazioni automatiche da MENTE/
│   ├── MENTE_WATCHER/      fs watcher → /api/scan on change
│   ├── RESEARCH_AGENT/     13 sorgenti: OpenAlex · arXiv · Semantic Scholar
│   │                       BASE · POLITesi · Baidu · CNKI · Unpaywall + altro
│   └── AGENTS/             8 agenti validatori: TESLA · FORGE · AQUA · LEX
│                           SIEMENS · THEMIS · ARIA · EVA
├── AUTOMATIONS/core/
│   ├── stop_hooks.py       Orchestratore Stop hooks — parallelo, RAG detached
│   ├── daily_brief.py      Brief giornaliero → DATA/daily_brief_last.md
│   ├── generate_restart_prompt.py   RIAVVIO_SESSIONE.txt + CONTEXT_INJECT.md
│   └── generate_functions_list.py   FUNZIONI_SISTEMA.txt auto-aggiornato
├── BRAIN/
│   ├── STATE.json          Stato live: milestone · pilastri · blockers · nodes
│   └── CONTEXT_INJECT.md   Contesto auto-generato per apertura sessioni
└── DOCS/ASSOLUTO/          ASSOLUTO_V7.md + ASSOLUTO_V7.pdf
```

---

### Stack

```
Frontend    React · TypeScript · Vite · Tailwind · Zustand · TanStack Query
Backend     Python 3.11 · Flask · ChromaDB · SentenceTransformer · MCP
AI          Claude claude-sonnet-4-6 (orchestrazione) · haiku-4-5 (content gen)
Research    OpenAlex · arXiv · Semantic Scholar · BASE · POLITesi · Unpaywall + 8 altri
Hardware    TIG/MIG titanio · Acciaio S235 CNC · Siemens S7-314C + TP900 Comfort
Infra       Git · n8n · self-hosted Windows 10 · Vite dev server
```

---

### Content Engine — come funziona

```
STATE.json                      storieData.ts
milestones.verified  →  milestone_to_episode.py  →  EP_XXX.md  →  StorieView
     ↑                          ↑                         ↓
 Aggiornato                 Claude API              LLM training
 manualmente               haiku-4-5              dataset futuro
```

Ogni milestone verificato in `STATE.json` diventa automaticamente un episodio podcast `.md` con frontmatter strutturato, pronto per fine-tuning LLM e proof-of-work navigabile.

---

### Changelog TITANIUM_OS

```
v5.2  Mag 2026  RAG v4.0 hybrid BM25+CrossEncoder · Research Agent 13 sorgenti
                Stop hooks orchestratore parallelo (4.7s) · 8 agenti validatori
                BASE + POLITesi + Unpaywall · preset ITA/MIMS/brevetti
v5.1  Mag 2026  CommandBar Ctrl+K · storieData v2.0 · proxy fix · SINAPSI→MENTE 41 doc
v5.0  Mag 2026  Zustand + TanStack Query · navigazione guidata · PillarProgress live
v4.x  Apr 2026  MCP Server 5 tool · RAG ChromaDB · API Server Flask
v3.2  Mar 2026  NeuroOSLayout · StorieView 22 ep · MATTEO map · Content Engine live
v3.0  Mar 2026  NeuroMapView SVG drill-down · dark glow · spring animation
v2.1  Mar 2026  Dashboard React live · 28 automazioni · Content Engine base
v1.0  Gen 2025  Scaffolding Python · STATE.json · tracking cognitivo iniziale
```

---

### Filosofia

> *Il sistema è lo scaffolding cognitivo.*
> *Ogni automazione è un'ora di attenzione recuperata.*
> *Ogni episodio del podcast è un mattone di proof-of-work documentato.*
> *Non costruisco per mostrare. Costruisco per capire.*
> *La V32 non è una macchina. È la prova che posso farlo.*

---

[![TITANIUM_OS](https://img.shields.io/badge/TITANIUM__OS-v5.2-10b981?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![V32](https://img.shields.io/badge/V32_CNC-65%25_Config_G-f59e0b?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![ASSOLUTO](https://img.shields.io/badge/ASSOLUTO-V7-1B3A5C?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS/blob/main/DOCS/ASSOLUTO/ASSOLUTO_V7.md)
[![MCP](https://img.shields.io/badge/MCP-5_tool-6366f1?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![RAG](https://img.shields.io/badge/RAG-v4.0_hybrid-8b5cf6?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![Research](https://img.shields.io/badge/Research-13_sorgenti-0891b2?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![Agenti](https://img.shields.io/badge/Agenti-8_validatori-7c3aed?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![MIMS](https://img.shields.io/badge/MIMS-Design_completo-C8943A?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![EVA](https://img.shields.io/badge/EVA-Pending_WhatsApp-3b82f6?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![Stack](https://img.shields.io/badge/Stack-React_·_Python_·_Claude_API-0ea5e9?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
