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

### Stato Live — v1.1.0 | Sessione #101 | 02 Jul 2026 15:44

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #50 (26-27/06): NINA ha un VOLTO definitivo (3D). Bloccato nina_DEFINITIVA (=nina_genio_1): mora, mix colombiana+sud Italia, coda alta, lentiggini, sguardo sicuro. REGOLA: ogni futura Nina deve avere QUESTO viso (slide_2=riferimento vincente); NO bionda, NO logo. Pipeline avatar DECISA: 3D via Gamma (stylePreset 3D, flux-2-klein). Versione VITA=giacca denim. Scene riusabili Nina/_SCENE (studio, ponte). Slide montate (ritratto in cornice + figura intera nella scena). PRE_03 carosello 'I Personaggi' SOLO NINA col volto vero, 6 slide. Canone in MENTE/KNOWLEDGE/NINA_DESIGN_DEFINITIVO.md. Altri personaggi per ora = simboli/Pietre.
**Prossimo step:** PROSSIMA SESSIONE #51: (1) decidere se serve un episodio 'Personaggi' dedicato o se Nina si presenta DENTRO l'episodio 4; (2) controllare PRE_01/PRE_02, rifinire PRE_03, poi PRE_04; (3) ricontrollare EP_1 effettivo; (4) Nina versioni officina/tech; (5) rag-update per indicizzare il canone Nina.

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
- Adobe Express + caroselli Nina (25/06 sess#48): export_html_to_express provato (account auth) -> EP_N2_01 carosello 8 slide in Express (font Adobe kit zhv2kry). Org POSTER/CAROSELLI/<EP_ID>/ (carosello.html+caption.txt+README.md+slides/). BIBBIA_VISIVA_CAROSELLI.md + BRIEF_ILLUSTRATORE_PERSONAGGI.md. Simboli mondo definitivi. Preambolo PRE_01 'Il Mondo di Nina' 8 slide illustrate ricche (porta/luna/calibro/ponte/mappa Pietre, filo-ponte, PNG pronti). Stile blueprint-anime alla Geronimo Stilton, no foto reali, personaggi via illustratore. tsc -b verde, 0 orfani episodi
- PRE_01 preambolo Nina -> CAROSELLO a 17 slide che SPIEGA il progetto (25/06 sess#49): iterato v1->v10 (stile buonanotte + flusso sfumato continuo su x globale; scartata v8 vignette). v10 = Cover/Cos-e/Perche/Per-chi-e/Patto/Nina/Themis/Atomi-Bit/4-simboli/Giuntura/8-Pietre/Cosa-imparerai/Come-funziona/Si-ripassa/Da-dove-nasce/Promessa/Si-parte. 17 PNG singole; versioni in _VERSIONI/+INDEX; tool _render_pair.py; integrato RAG+Obsidian. Verifiche: 0 orfani, build 215, tsc EXIT 0
- PRE_02 "Come funziona Nina" — 2o carosello del preambolo (16 slide, 26/06 sess#49): integra la visione Libro-IA in lingua semplice (Organismo, Mappa Viva, doppio fondo, test della sarta, sotto-i-piedi RAG/GPU vero, ancoraggio, motore infinito, cresce-da-se, scalabilita, Provalo tu, Nina<->HR, eredita, Episodio 1). 16 PNG singole + README + caption. Serie preambolo: PRE_01 overview + PRE_02 come funziona, stesso flusso continuo
- Sessione #50 (26-27/06): VOLTO DI NINA BLOCCATO (nina_DEFINITIVA=nina_genio_1) — mora, mix colombiana+sud Italia, coda alta, lentiggini; pipeline avatar 3D via Gamma flux-2-klein; versione VITA=giacca denim; scene riusabili (studio/ponte); slide-personaggio + slide-scena; PRE_03 carosello 'I Personaggi' SOLO NINA col volto vero (6 slide); canone in MENTE/KNOWLEDGE/NINA_DESIGN_DEFINITIVO.md + memoria project_nina_avatar. Decisione: altri personaggi per ora solo simboli/Pietre. REGOLA: ogni futura Nina = quel viso
- Sessione #50: PRE_01 slide 11 (le 8 Pietre) ridisegnata — da 8 diamanti col numero a 8 gemme con ICONA senza numeri (⟡0 dado=Atomi, ⟡5 rete=Bit) + nomi sotto (Materia..Direttore); versione _VERSIONI/v12_icone-8-pietre

### Episodi recenti
- *Il Sussurratore che Indovina*
- *Il semaforo che mente*

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
