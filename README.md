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

### Stato Live — v1.1.0 | Sessione #107 | 07 Jul 2026 12:50

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #52 (02-03/07): ATTACCO ESERCITO su Fable COMPLETO — 7/7 specialisti rientrati (01 design, 02 sicurezza, 03 scrittura, 04 software, 05 news-IA, 06 gestionale, 07 integrita-RAG) in DOCS/ATTACCO_20260702/NN_*.md, additivo/propose-only con file:riga. Sintesi coordinata in _SINTESI.md (TOP 10 per leva). TUTTE le azioni (TOP 10 + backlog completo per dominio, ~49 voci) portate in DA_FARE_FATTO.md come [ ] DA FARE. Filo rosso: il sistema gira ma in 3 punti la fonte di verita e stantia (canone RAG _CANONE.md:13 punta a V32-su-molle/recuperato vietato; INDICE_CAMMINO 9/15 titoli sbagliati; pitch 3 errori) e 1 ordine hardware (Vevor+ER20+UPS ~250-350EUR) sblocca l'intera catena economica + le corruzioni HNSW. Niente committato del codice-proposta (gate SELF_IMPROVE).
**Prossimo step:** PROSSIMA SESSIONE #53 (APRIRE CON FABLE 5): (1) REVISIONARE OBSIDIAN e rendere l'ecosistema MENTE un VERO ecosistema (note/ponti/wikilink sani, verita unica _CANONE.md, zero orfani, MOC) via setup_obsidian + vault_intersect + storie_intersect + rag_linkgraph; si aggancia a TOP 10 #2/#3 (canone RAG stantio) e #9 (indice storie) e 07 P1. (2) POI prima ondata attacco per leva: TOP 10 #1 checkout hardware -> #2/#3 canone RAG. Tutte le azioni in DA_FARE_FATTO.md.

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
- Sessione #51: DECISO dove si presenta Nina — PRE_03 = scheda-personaggi statica del preambolo; Nina si presenta VIVA in azione dentro l'EP_1 reale, non in un episodio narrativo dedicato (preambolo=anagrafica, episodi=storia) (02/07)
- Sessione #51: EP_N2_01 'La Bambina che Chiedeva Perche' rifatto al NUOVO STANDARD — da 8 slide (pre-volto) a 16 slide blueprint SVG narrativo (scene disegnate, zero foto, stesso sfondo/flusso), 3 strati rispettati (bottoni=bambino, sarta=grande, pizzicore=cuore), generatore riusabile _build_ep.py+_render_all.py; snapshot v1_8slide_2506 + v2_blueprint-16slide (02/07)
- Sessione #51: EP_N2_02 'Il Soffio di Troppo' al nuovo standard (16 slide blueprint SVG narrativo) — la Fucina/Forge, mezzo mm=il patto, test della sarta, precisione=relazione, tolleranza gradi non si/no; stesso impianto di EP_01 (generatore+README+caption); snapshot v1_blueprint-16slide (02/07)
- Sessione #52-prep (02/07): infra refresh + RAG rebuild VERIFICATO. Default modello -> Fable 5 (.claude/settings.local.json, gitignored, repo pubblico). Dashboard riavviata (5173); Obsidian/ecosistema 595 note/3230 ponti/2 isolate; Pietre 9/82; 0 orfani; _CANONE.md ok 0 violazioni. RAG full rebuild-hard (post-Obsidian) allineato 25049 semantico==bm25 (HNSW pulito, heading-aware v4.1); query end-to-end conferma storie->RAG->Nina (EP_N2_02 top hit). PIANO D'ATTACCO esercito 7 domini (design/sicurezza/scrittura/software/news-IA/gestionale/integrita-RAG) ingegnerizzato e congelato in DOCS/ATTACCO_20260702/_PIANO.md, propose-only/additivo, da eseguire su Fable.
- Sessione #52 (02-03/07): ATTACCO ESERCITO su Fable COMPLETO E SINTETIZZATO — 7 agenti general-purpose model=fable in parallelo (design/sicurezza/scrittura/software/news-IA/gestionale/integrita-RAG), ognuno un report additivo propose-only con file:riga in DOCS/ATTACCO_20260702/. Coordinatore Fable ha scritto _SINTESI.md (quadro per dominio + TOP 10 per leva) e portato TUTTE le azioni (TOP 10 + backlog completo per dominio) in DA_FARE_FATTO.md come [ ] DA FARE. Finding chiave: (P0) _CANONE.md:13 punta alla verita V32 vecchia/vietata (molle+recuperato) su cui Nina grounda; (P0) 55 file versioni superate dentro il canone RAG; EVA eva_server.py:162 bind 0.0.0.0+/inbox PII senza auth; commit-leak RAG senza guardia in api_server; Anthropic News watcher morto da 25gg; FINANCE/ vuota+BEP Via B non calcolabile; MOSSA1 checkout hardware = massima leva. Zero modifiche applicate al codice (gate propose-only).

### Episodi recenti
- *Il Cartellino sulla Stoffa*
- *Mille Volte Uguale*
- *Il Sussurratore che Indovina (e a Volte Mente)*

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
