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

### Stato Live — v1.1.0 | Sessione #44 | 10 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #34: CLAUDE.md v4.1.0 + RAG→WIKI Graphify in produzione + AI News Watcher v1 keyless + UI anti-sovraccarico (Centro di Controllo, STORIE a fisarmonica) + RETE riparata e integrata col grafo Graphify (toggle Conoscenza/Sistema) + binario AVVENTURA: bozza Mappa multi-livello + vista 'Mappa dell'Avventura' + 3 episodi (EP_AV_00/01/02: Loop→Automazione→LLM). Tutto committato+pushato.
**Prossimo step:** [Matteo al risveglio] Guardare: CONTROLLO, STORIE rifatta, RETE→toggle 'Sistema' (dopo restart API), CONTROLLO→Mappa dell'Avventura, e i 3 episodi di Nina. Poi decidere: rinomina nomi sidebar (⚠ collisione 'Bussola'), schedulare watcher 48h (UAC), incoerenza ⟡ pilota-vs-arco, scrivere EP_AV_03+ (RAG/Wiki/Agenti/Orchestrazione).

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
- AI News Watcher catturato: BRAIN/AI_NEWS_WATCHER_BRIEF.md (30+ creator + handle, logica tier 48h con rotazione) + scaffold DATA/ai_news_watcher_state.json (07/06/2026)
- AI News Watcher v1 KEYLESS costruito+testato: NODES/AI_NEWS_WATCHER/watcher.py + launcher night_ai_watch.bat; 4 sorgenti (GitHub via gh, siti RSS, YouTube RSS) zero chiavi, tier+rotazione, 67+30 segnali reali (07/06/2026)
- UI anti-sovraccarico: vista CONTROLLO (Centro di Controllo: ogni strumento cosa fa/come si usa/se acceso) + STORIE v3.0 a fisarmonica; skill salva +memoria/+grafo; apertura→CONTROLLO (07/06/2026)
- RETE riparata + integrata Graphify: era rotta (doppio api_server, indice stale); toggle sorgente Conoscenza(RAG)/Sistema(Graphify), nuovo endpoint /api/graph/graphify (stessa forma → motore 3D invariato), endpoint RAG blindato (07/06/2026)
- Binario AVVENTURA esteso: bozza MAPPA_AVVENTURA.md multi-livello (Mondo→7 Regioni dell'arco IA→semi tecnici→Pietre) + vista navigabile 'Mappa dell'Avventura' (AvventuraMapView) + 3 episodi definitivi EP_AV_00/01/02 (Loop→Automazione→LLM), build verde (09/06/2026)

### Episodi recenti
- *La Mente che Parla*
- *L'Incantesimo che si Ripete*

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
