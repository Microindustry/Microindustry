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

### Stato Live — v1.1.0 | Sessione #46 | 11 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #35: SISTEMA VERIFICA reale (git pulito, build TS 0 errori, RAG GPU ok) + RETE riparata (restart API → /api/graph/graphify e /api/rag/vectors da 404/500 → 200, toggle Conoscenza/Sistema LIVE) + n8n installato GLOBALE (2.25.6) e avvio-al-login riagganciato (START_LOGIN.bat usa binario globale, fallback npx) + diagnosi STORIE (124 ep ma lavoro recente 0 episodi) + VISIONE Nina-PRODOTTO catturata nel canone (BIBBIA §0-bis: derivazione educativa di MIMS, scaletta/changelog-driven, scope tech+finanza).
**Prossimo step:** STORIE: creare i 'semi' tecnici reali del lavoro recente che hanno 0 episodi (Graphify/RAG→Wiki, RETE-grafo, AI Watcher, Centro di Controllo) → CONTENT_ENGINE/DATABASE/episodes + build_episodes_json.py. POI Nina rifatta da zero (impronta validata, agganciata alla scaletta). POI nodo SELF_IMPROVE (agente autonomo notturno, read-only+PR, mai merge auto su main).

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
- RETE riparata + integrata Graphify: era rotta (doppio api_server, indice stale); toggle sorgente Conoscenza(RAG)/Sistema(Graphify), nuovo endpoint /api/graph/graphify (stessa forma → motore 3D invariato), endpoint RAG blindato (07/06/2026)
- Binario AVVENTURA esteso: bozza MAPPA_AVVENTURA.md multi-livello (Mondo→7 Regioni dell'arco IA→semi tecnici→Pietre) + vista navigabile 'Mappa dell'Avventura' (AvventuraMapView) + 3 episodi definitivi EP_AV_00/01/02 (Loop→Automazione→LLM), build verde (09/06/2026)
- SISTEMA VERIFICA + RETE riparata: restart API ha portato /api/graph/graphify e /api/rag/vectors da 404/500 → 200 (toggle RETE Conoscenza/Sistema ora LIVE); git pulito, build TS 0 errori, RAG GPU verificato (10/06/2026)
- n8n installato globale (npm i -g n8n, 2.25.6) + avvio-al-login riagganciato: START_LOGIN.bat step 4 usa binario globale (%N8N% start) con fallback npx — niente più reinstall ~4min a ogni login (10/06/2026)
- VISIONE Nina-PRODOTTO a canone (BIBBIA §0-bis): Nina = versione educativa introduttiva di MIMS (derivazione del prodotto), scaletta/changelog-driven (persona curiosa che sbaglia→sistema→aggiorna), scope > arco IA (anche 'cos'è un ambiente Python') + verticale finanza personale; nodo SELF_IMPROVE (agente autonomo notturno read-only+PR) messo in bussola dopo gli episodi (10/06/2026)

### Episodi recenti
- *Il Direttore*
- *L'Esercito Silenzioso*
- *Chi guardare più spesso — il tier a rotazione 48h*
- *Guardare senza chiavi — gh, RSS, YouTube*
- *Il gate di rilevanza — tenere il segnale, buttare il rumore*

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
