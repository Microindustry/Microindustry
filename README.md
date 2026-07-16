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

Quando ho iniziato a costruire la mia fresatrice CNC da zero — progetto **corpo unico** in acciaio saldato TIG, 3 assi; oggi è un **telaio in piedi**, coi componenti scelti uno a uno — ho capito che avevo bisogno di un sistema per non perdere il filo. Da lì è nato TITANIUM_OS. I numeri della macchina li dirà la macchina, quando potrà dimostrarli.

Nessuna laurea. Solo proof-of-work reali.

---

## TITANIUM_OS — Il sistema operativo della mia vita

> *Un sistema che gira da solo vale più di 10 abitudini che dipendono dalla volontà.*

**TITANIUM_OS** è il sistema che costruisco mentre costruisce me. Ogni nodo elimina un carico mentale. Ogni automazione libera energia per il lavoro fisico.

### Stato Live — v1.1.0 | Sessione #133 | 17 Jul 2026 00:05

*Le barre sono metriche di gestione interna (STATE.json live), non misure fisiche:
lo stato reale della V32 oggi è un telaio in piedi + componentistica scelta.*

| Pilastro | Avanzamento gestione | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | Al telaio — in costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (sistema modulare d'acciaio) | `███░░░░░░░ 30%` | Attende la pressa VULCAN |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Adesso** — Il sistema ha iniziato a consegnare da solo. Di notte produce i caroselli, li controlla con un QC automatico e li impagina per i social; la prima uscita pubblica su LinkedIn è andata. Il lavoro non lo devo più ricordare: si documenta e si racconta da sé.

**Prossimo** — Pubblicazione completamente automatica — un episodio finito diventa un post LinkedIn senza tocco umano (Postiz self-hosted, collegato via autorizzazione sicura, non con password).

<details>
<summary>🔩 Dettaglio tecnico — milestone attivo e ultimi lavori verificati (per chi vuole i dadi e i bit)</summary>

**Milestone attivo:** Sessione #62 (16/07): ESECUZIONE ONDATA A/B/C + promozione. ONDATA A completa (A1 canon-pin salta i wikilink SUPERSEDED; A2 coda auto-refill+multi-bozza col tetto; A3 fonti allineate _CANONE 53->56/piano/watcher.log rotante; A4 14,8 GB liberati via retention R6/R7 + .obsidian fuori canone). EP_SG_02_01 «V32» revisionato §7.7 e promosso (S1 4/69). ONDATA B: PDF LinkedIn per episodio (pdf_export, 15/15); dieta RAG (hash-manifest anti re-embed + lock build_index + early-exit no-op); CORSIA NINA apprendista (night_caroselli_nina impagina i testi EP_N2 canonici, no invenzione/no GPU, task @04:35, prova del fuoco EP_N2_04 verde). ONDATA C: finetune vero (dataset 30->176 episodi Matteo-voce + --overwrite_output_dir + verifica step) + RandomDelay sui task GPU. 16 commit repo + 3 MENTE, tutti additivi/verificati. | + BACKLOG RAG CHIUSO: #7 riflusso FATTI a rotazione trimestrale (stop re-embed monolite, idempotente), #8 demote STORIE (i 3 generatori groundano sul FATTI curato, no camera d'eco), #6 sentinella doppioni _copia, #10 daily-note fuori indice. L'intero dominio RAG dell'attacco #2 e' coperto.

**Prossimo step:** PROSSIMA (#63): risultati test LinkedIn PRE_SG_01 -> taratura PDF; export Express (con Matteo); register_night_tasks.ps1 (UAC) per RandomDelay+task caroselli; revisione bozze notturne SG@04:15+Nina@04:35; gated: app Meta, pin repo, UPS. Effetti pieni #7/#8 al restart API/incrementale notturna.

**Ultimi 5 milestone verificati:**
- Sessione #62: EP_SG_02_01 «V32 - il cuore che taglia» revisionato (QC verde, §7.7 slide 9 STATO REALE, slide 6 TP900+bronzine/scalini verificata grounded) e PROMOSSO in CAROSELLI/SISTEMA (S1 4/69, apre CAP 2)
- Sessione #62 ONDATA B: pdf_export.py - un carosello.pdf per episodio (post-documento LinkedIn, canale NON-Meta), 15/15 creati; dieta RAG (hash contenuto nel manifest = stop re-embed di massa da touch + lock msvcrt su build_index + early-exit no-op)
- Sessione #62: CORSIA NINA apprendista - night_caroselli_nina.py impagina i testi EP_N2 canonici (no invenzione, no GPU) + nina_queue.py (seed 53) + sg_builder voce parametrica/scene Nina + task TI_NightCaroselliNina @04:35; prova del fuoco EP_N2_04 verde
- Sessione #62 ONDATA C: finetune vero - episodes_to_dataset ricorsivo (30->176 episodi Matteo-voce, esclusi Nina/staging) + night_finetune --overwrite_output_dir + verifica global_step>0 (no piu' finto-verde); RandomDelay sui 3 task GPU (StoryAgent/NightResearch/FineTune) contro il MemoryError al boot
- Sessione #62 BACKLOG RAG (attacco #2 dominio 2): #7 fatti_reflux a rotazione trimestrale (fatti_dalle_storie_YYYYQn.md, i trimestri chiusi non cambiano -> zero re-embed, verificato idempotente, 5 monoliti migrati) + #8 demote_dirs opt-in (malus selezione simmetrico al canone, wired night_caroselli/nina_agent/story_agent + /api/rag/search?demote=STORIE) + #6 check_doppioni_copia in night_audit (trova i *_copia accanto all'originale) + #10 daily-note YYYY-MM-DD fuori dall'indice (_is_nav_file). Dominio RAG dell'attacco #2 completo.

</details>

---

### Nodi GENESIS attivi

| Nodo | Descrizione |
|------|-------------|
| `MENTE RAG v4.2` | ChromaDB hybrid BM25+semantico+CrossEncoder, chunking heading-aware + GraphRAG-lite — ~19.600 chunk, si aggiorna da solo a ogni modifica |
| `Story Agent` | Milestone verificato → episodio narrativo (02:07 ogni notte) — il lavoro si documenta da solo |
| `Nina Agent` | Il binario educativo: favole vere generate a 2 stadi con grounding RAG |
| `Apprendista notturno` | Bozze di caroselli Instagram in quarantena (@04:15) — QC automatico + canon_guard, promozione solo umana di giorno |
| `Research Agent` | Paper e segnali da 13 sorgenti (arXiv, Semantic Scholar, GitHub...) |
| `Watchdog + self-heal` | Il sistema si sorveglia e si ripara (RAG recovery a 2 livelli, sentinelle notturne) |
| `Daily Brief` | Briefing quotidiano 07:30 |
| `API Server` | Flask localhost:5001 — media, foto, agenti, RAG |
| `Dashboard` | React+Vite — 3 facce: TITANIUM (sistema) · NINA (favola vera) · PUBBLICAZIONI |
| `Personal LLM` | Fine-tuning sui miei episodi (domenica notte) |

---



### Episodi recenti
- *La mano che insegna alla notte*
- *La Giuntura che Respira*

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

Calcoli di progetto (non ancora dimostrati sul campo): BEP V32 **61 ore** | Tariffa target **EUR 45/h**

---

*Aggiornato automaticamente ogni notte da TITANIUM_OS · TI_NightPush 04:07*
