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

### Stato Live — v1.1.0 | Sessione #89 | 24 Jun 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #44 (24/06): NINA COPRE LA MAPPA — 50 episodi EP_N2. Driver nina_map_cover.py genera un episodio Nina per ogni concetto DISTINTO della mappa senza versione (31 fonte: Graphify/RETE/t-SNE/orchestratore/watcher/controllo) -> copertura in ampiezza ⟡0→⟡7, auto-canone grounded sul RAG. +3 dal loop nativo. RAG RESUSCITATO (corruzione HNSW + commit-leak 56GB liberato, --drop-hnsw). Menu Storie a 3 voci top-level. EP_N2_01 riscritto come vero inizio. Poster pilota (Claude Design). 2 rinforzi (rag_recover anti-commit-leak; chromadb-ops valutato e rifiutato). Vetrina pubblica README + ECOSYSTEM_MANIFEST riallineati ai 15 nodi reali (erano 8).
**Prossimo step:** DA DECIDERE CON MATTEO (svegli): gitignore DATA/views(298 auto-gen)+logs; raggruppare/indicizzare AUTOMATIONS/core(~30 script piatti); pulire INBOX; irrobustire resolver YouTube watcher. Candidato RAG: implementare WAL→HNSW commit contro 0.5.23. Nina: 50 ep nel canone, mappa coperta -> prossimo naturale = animatic pilota EP_N2_01 (era in pausa) o verticali nuovi (FORGE saldatura, MIMS).

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
- BLACKOUT recovery RAG a 2 livelli (23/06): rag_recover.ps1 + rag_engine --probe/--drop-hnsw/--rebuild-hard; L1 sposta solo il segmento HNSW (Chroma ricostruisce da sqlite, no ri-embed), L2 rebuild HARD; copre corruzione (probe) E divergenza (stats); agganciato al self-heal notturno night_research.bat (sostituisce rebuild_rag_clean). Commit d1863576
- Fix bug radice crash post-blackout (23/06): api_server hidden ha stdout/stderr handle OS invalidi -> torch nativo crasha (reset su /api/rag/search); redirect su logfile in restart_api/rebuild_rag_clean/rag_recover/rag_update_exclusive + guardia devnull in api_server.py + guardia stdout in rag_engine.py
- RESET FISICO chroma_db (23/06, commit 04c3f71a): su chromadb 0.5.23 il reset-per-id NON azzera lo spazio-label hnswlib -> label fantasma > count -> KeyError np.uint64 su alcune query; --rebuild-hard + reset_chroma_dir() spostano la cartella fisica (HNSW da 0). RAG verificato 32974 chunk, 6/6 query ok
- GPU rimessa + research_agent v1.2 (23/06): rag_device.txt=cuda (init CUDA non satura piu' il commit, query ~5x); research_agent backoff esponenziale 429/503 + API-key opzionale + guardia globale (log JSON, niente catena abortita), testato live
- OBSIDIAN titoli + intersect (23/06, MENTE d9b044a): 108 titoli normalizzati (H1+frontmatter title da source/notebook) ADDITIVO senza rename (967 wikilink intatti, no clobber heading corpo); fix_titoli_vault.py; intersect rigenerato vault(2881)+storie(950,0 isolati)+ponti+wiki(651 note)

### Episodi recenti
- *Il semaforo che mente*
- *La scatola magica dei compiti*
- *Il Libro delle Ricette di Nonna*
- *La Tela — Chi guarda il quadro?*
- *La Stanza della Visione*

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
