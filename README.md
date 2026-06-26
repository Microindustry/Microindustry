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

### Stato Live — v1.1.0 | Sessione #97 | 26 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #49 (25/06): PRE_01 preambolo Nina come CAROSELLO che SPIEGA il progetto. Iterato v1->v10: stile buonanotte + FLUSSO sfumato continuo (onda su x globale). Scartato v8 vignette/fumetto. v10 ATTUALE = 17 slide, linguaggio semplice/ricco: Cover, Cos-e, Perche, Per-chi-e, Il Patto, Nina, Themis, Atomi<->Bit, I 4 simboli, La Giuntura, Le 8 Pietre, Cosa imparerai, Come funziona, Si ripassa, Da dove nasce, La promessa, Si parte. 17 PNG singole slides/slide_1..17. Versioni in _VERSIONI/. Integrato in RAG+Obsidian.
**Prossimo step:** Matteo manda un FILE da leggere/riflettere -> se serve cambiare il preambolo si fa ORA (prima di bloccarlo). Poi export Adobe Express (export_html_to_express, readiness skill). Aperti: scelta onda v5 sfumata (attuale) vs v4 intreccio; altri caroselli; EP_N2_01 a questo livello.

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
- MIMS connettori = Via B DECISO (24/06): compressione VULCAN (processo proprietario per B2, capitale basso, dentro il moat-Formula) a canone SCHEDA §5 + STATE. Silent block V8 -> v.B Ø18mm (reversibile). Sblocca BEP/B2
- De-hardcode benen completo (24/06): 5 registrar legacy AUTOMATIONS/tools resi portabili in place ($PSScriptRoot/%~dp0 + env, ASCII-norm, fix bug && PS5.1) poi RIMOSSI (git rm, recuperabili) perche' ridondanti con register_night_tasks.ps1. Zero hardcode benen veri nel repo
- RAG v4.2 SOTA-2026 (24-25/06): chunking heading-aware (.md, +breadcrumb) + snapshot chroma_db in _VAULT/BACKUPS (rotazione 3) + GraphRAG-lite wikilink-expansion (rag_linkgraph.json, espande [[link]] dai top-3 cap+8, reranker gata). _DA_ORDINARE->_ARCHIVIO fuori dal canone (V6 superato non inquina piu'). HNSW rigenerato via rag_recover (UAC). Prova: EP_N2_51 grounded+connesso. Nina=auto-promozione decisa. Build verde, pushato (79908408+a0f6a9b9+9e3bde3a)
- RETE visiva da 2 link (Konik+Hermes) (25/06 sess#47): (1) orfani di RETE nella cartella clinica (vault_intersect v2.1->vault_orphans.json, night_audit v1.4 critica RETE, setup_obsidian lo lancia di notte; 393 note/2 orfani veri); (2) orfani colorati nella RETE 3D (anello rosso+filtro); (3) RETE viva: freschezza mtime + hub degree + memoria 2 livelli Hermes (core/vault) + legenda (/api/rag/vectors +orphan+degree+age_days+tier); (4) transizioni morbide (scena WebGL persistente + fade-in, no remount al filtro). Commit 38bd6fc0+b3675b3c+91fb8672+98fd7109. tsc -b + py_compile verdi
- Adobe Express + caroselli Nina (25/06 sess#48): export_html_to_express provato (account auth) -> EP_N2_01 carosello 8 slide in Express (font Adobe kit zhv2kry). Org POSTER/CAROSELLI/<EP_ID>/ (carosello.html+caption.txt+README.md+slides/). BIBBIA_VISIVA_CAROSELLI.md + BRIEF_ILLUSTRATORE_PERSONAGGI.md. Simboli mondo definitivi. Preambolo PRE_01 'Il Mondo di Nina' 8 slide illustrate ricche (porta/luna/calibro/ponte/mappa Pietre, filo-ponte, PNG pronti). Stile blueprint-anime alla Geronimo Stilton, no foto reali, personaggi via illustratore. tsc -b verde, 0 orfani episodi

### Episodi recenti
- *Il Sussurratore che Indovina*
- *Il semaforo che mente*
- *La scatola magica dei compiti*

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
