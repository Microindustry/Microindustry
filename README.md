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

Quando ho iniziato a costruire la mia fresatrice CNC da zero — 178 kg, 3 assi, ±0.019 mm — ho capito che avevo bisogno di un sistema per non perdere il filo. Da lì è nato TITANIUM_OS.

Nessuna laurea. Solo proof-of-work reali.

---

### Processo evolutivo

| Anno | Evento |
|------|--------|
| 2008 | Saldatura TIG titanio — scarichi MotoGP @ SCProject |
| 2012 | Programmazione robot ESSEGI — packaging industriale |
| 2015 | Operatore presse DATWLER + QC LU.VE refrigerazione |
| 2024 | Inizio costruzione fresatrice CNC V32 da zero |
| Gen 2025 | TITANIUM_OS v1.0 — primo scaffolding Python + STATE.json |
| Feb 2026 | V32: 178 kg assemblati, asse X completo, guide + vite + servo |
| Mar 2026 | TITANIUM_OS v2.1 — Dashboard React live, 28 automazioni |
| Mar 2026 | TITANIUM_OS v3.0 — NeuroMapView SVG immersiva |
| Mar 2026 | TITANIUM_OS v3.2 — Content Engine, podcast episodes, MATTEO map |

---

### Progetti attivi

**🔩 V32 — Fresatrice CNC 3 assi**
Costruzione da zero. Struttura in alluminio 7075, viti a ricircolo di sfere, servo Siemens. Stato: `Config G — 65%`. Obiettivo: lavorazione MIMS tiles.

**🧠 TITANIUM_OS — Sistema operativo cognitivo**
Dashboard React 19 + Vite + Tailwind v4. 34 automazioni Python + n8n. Mappe SVG drill-down, Content Engine per episodi podcast, database SINAPSI layer dei progetti. `v3.2 live`.

**🔌 MIMS — Connettori modulari fisici**
Protocollo proprietario di connettori fisici modulari. Tile lavorabili su V32. Applicazione prevista: Fit Park 4.0 (area fitness con tornello MIMS). `Prototipo`.

**⚡ VULCAN — Pressa 20t + ricette polimeri**
Pressa Vevor 20t + colonne guida DATWLER + ricette polimeri A/B/C. Brevetto di processo in sviluppo. Moat competitivo per MIMS. `R&D`.

**🤖 EVA — AI assistant per centro estetico**
WhatsApp bot + Claude API per Vita Natura (centro estetico, Boffalora sopra Ticino). Gestione appuntamenti, FAQ, follow-up clienti. `Beta`.

---

### TITANIUM_OS — Architettura v3.2

```
TITANIUM_OS/
├── DASHBOARD/                React 19 + Vite + Tailwind v4
│   ├── NeuroMapView          Mappa SVG drill-down immersiva — dark glow + spring
│   ├── NeuroOSLayout         Vista mappa: dot grid + pulse rings + drillZoom
│   ├── CanvasLayout          Vista canvas draggabile per stato progetti
│   ├── LayersView            SINAPSI — database layer strutturato per progetto
│   └── StorieView            14 episodi podcast + dataset LLM training
├── AUTOMATIONS/              34 automazioni (13 attive, 14 WIP, 7 Content Engine)
│   └── core/                 state_updater.py, content_pipeline.py, social_dist.
├── BRAIN/
│   ├── STATE.json            Stato corrente: milestone, WIP, prossimo step
│   └── KNOWLEDGE/            15 file di contesto per LLM (sistema, progetti, CV)
├── CONTENT_ENGINE/           Pipeline auto-generazione episodi da STATE.json
│   ├── scripts/              milestone_to_episode.py + state_watcher.py
│   └── DATABASE/             Episodi .md con frontmatter LLM-ready
├── MATTEO/                   Mappa ecosistema personale (SVG standalone, vanilla JS)
└── SINAPSI/                  Documentazione strutturata: CV, VULCAN, MIMS, EVA
```

---

### Stack

```
Frontend    React 19 · TypeScript · Vite · Tailwind v4 · Lucide Icons
Backend     Python · Flask · SQLite · n8n · Claude API (Anthropic)
Hardware    TIG/MIG · Alluminio 7075 · Siemens S7-314C · Saldatura titanio
Infra       Git · GitHub Actions (WIP) · self-hosted · Windows
```

---

### Changelog TITANIUM_OS

```
v3.2  Mar 2026  NeuroOSLayout immersivo, StorieView podcast, MATTEO map standalone
v3.0  Mar 2026  NeuroMapView v3: SVG drill-down, dark glow, spring animation
v2.1  Mar 2026  Dashboard React live, 28 automazioni, Content Engine base
v2.0  Feb 2026  FileBrowser, MdManager, LayersView, CanvasLayout
v1.5  Feb 2026  API server Flask, state_updater.py, automazioni core
v1.0  Gen 2026  Scaffolding Python, STATE.json, primo sistema di tracking
```

---

### Filosofia

> *Il sistema è lo scaffolding cognitivo.*
> *Ogni automazione è un'ora di attenzione recuperata.*
> *Ogni episodio del podcast è un mattone di proof-of-work documentato.*
> *Costruisco per capire. Documento per non perdere.*

---

[![TITANIUM_OS](https://img.shields.io/badge/TITANIUM__OS-v3.2-10b981?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![V32](https://img.shields.io/badge/V32_CNC-65%25-f59e0b?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![VULCAN](https://img.shields.io/badge/VULCAN-R%26D-ef4444?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![MIMS](https://img.shields.io/badge/MIMS-Prototipo-8b5cf6?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![EVA](https://img.shields.io/badge/EVA-Beta-3b82f6?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
