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

### Stato Live — v1.1.0 | Sessione #118 | 14 Jul 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #58 (14/07): LINEE GUIDA COMPLETE per i due binari - ecosistema pianificato porta a porta (~165 caroselli). Sidebar: faccia SISTEMA (EPISODI/GIORNO0/LINEA GUIDA) pareggiata con NINA (+LINEA GUIDA). Vetrine giorno-0 vuote fino al publish-ready (lezione: piano prima di compilare). Canone nuovo: GUIDA 2-bis copertina-poster (safe-zone/miniatura/collezione), PONTE_SG_NINA (cameo 1-4-9 + preamboli che si presentano a vicenda), provenienza componenti (canale usato, mai prezzi per-pezzo), LINEA_GUIDA_NINA v2 (12 guardie QC), piani produzione: SG S1 68 + stagioni S2-S6, Nina PRE 4 + cammino 53 + stagioni N1-N5. Regola: titoli adattivi = linea guida non regola. Colli di bottiglia attaccati con soluzione (n.1 = binario notturno bozze). Obsidian rigenerato coi connettori.
**Prossimo step:** DOMATTINA su input Matteo (gestione autonoma): triage notturno + colli piccoli (QC copertina, render_queue, _TEMPLATE/components SVG) + PRODURRE serie PRE_SG_01-04 (Claude 100%) + design binario notturno bozze. PRE_01 Nina resta INSIEME. Gated Matteo: hardware UPS+ER20+Vevor, prerequisiti Meta (~1h), Semantic Scholar key.

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
- Sessione #55: pulizia dashboard — NodeKit.tsx (NodeTile/NodeLevel condivisi: erano 4 copie identiche-a-tema-diverso, -256 righe, tsc verde + screenshot prima/dopo pixel-identici, critica gc01 chiusa). Vista CRITICHE ELIMINATA su decisione Matteo ('non si aggiorna') -> CRITICHE.md stile bussola in root (critiche_md.py: polso + canone per progetto + auto-audit aperte), rigenerato ogni notte da night_audit e auto-committato da night_push; fonti = i 2 JSON vivi
- Verita' sparsa CHIUSA (08/07 sess#56): SYSTEM_TREE derivato da mappaData.ts (adapter SkillNode->MapNode, % computate nodeProgress, ROOT=media, -84 righe a mano, pct_sync v1.1 ritirato da MappaView) + % MIMS/GENESIS con nome esplicito (voci mappa vs pilastro STATE) + AUTOMATIONS_MASTER v1.3 archivio storico con 4 fonti vive
- LE 3 FACCE (08/07 sess#56, decisione Matteo): sidebar TITANIUM/NINA/PUBBLICAZIONI (deep-link intatti, Archivio sotto-voce), RIPASSO_S32-56.md (5 fasi+canone operativo+carattere), PubblicazioniView (trovato/pipeline/criteri/scaletta 9 passi), vincoli ri-verificati doc Meta (10 slide max, LinkedIn PDF, slide 1080x1350 gia' a norma, Postiz MCP), binario nuovo 'voce Matteo', tsc verde + screenshot
- Sessione #57 (13/07): igiene profonda + campo di battaglia — RAG v4.3 self-heal inverso + 2 recovery HNSW (18004==18004, snapshot fresco), watcher v1.2 (RETIRED_HANDLES + watchlist completa, 26 sorgenti), finetune v3.0 su venv dedicato (sistema 0 CVE su 194), caroselli a convenzione completa (P7/F6/F7 attacco chiusi), GUIDA_CAROSELLI+QC automatico+sentinella, Obsidian 561 note/3012 ponti, -5GB detriti. Rotta: PRE_01 da 0 + storie voce Matteo gestione Claude 100%. tsc verde, 0 orfani
- Ecosistema contenuti pianificato porta a porta: linee guida due binari + piani produzione (~165 caroselli) + PONTE SG-Nina + standard copertina + colli di bottiglia con soluzione; sidebar SISTEMA pareggiata con NINA; build verde, RAG e Obsidian aggiornati (14/07/2026)

### Episodi recenti
- *Il Dito che Insegna*
- *Il Direttore Invisibile*

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
