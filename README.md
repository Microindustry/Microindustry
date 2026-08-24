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

### Stato Live — v1.1.0 | Sessione #158 | 24 Aug 2026 15:50

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

**Milestone attivo:** Sessione #70 (16/08): BONIFICA CONTAMINAZIONE MIMS + SCALA GENESIS S0-S2. Scoperto che A1/A2 erano gia' fatti dal commit a77256f3 del 28/07 (sorgente chiusa da 19 giorni): non rifatti, verificati. A3 era il pezzo vero aperto -> canon_guard su 64 EP_N2 vivi ha trovato 8 episodi sporchi (i 5 in lista 57/59/60/63/64 + 3 fuori lista 01/13/52); nuovo tool AUTOMATIONS/tools/fix_pilastri_software.py ha applicato 40 sostituzioni su 16 file (repo + specchio MENTE, che e' quello che il RAG rilegge): MIMS-come-software -> GENESIS, rimossa la fonte FABBRICATA 'GENESIS/documentation_hallucination_2026' (non esiste), tolti 2 numeri inventati spacciati per FATTI (40-60% false credenze, sarta 1 su 1.000), corretta la falla [persone] di EP_N2_63 (dava una figlia a una bambina). VERIFICA: canon_guard 0 righe sugli episodi vivi + test di non-regressione dell'Architetto sui 2 concetti incriminati = entrambi agganciati a GENESIS, 0 violazioni. B: B3 era davvero aperto (run_story_agent committa solo S2_SISTEMA, la corsia Nina non l'ha mai committata nessuna automazione) -> commit aggiunto in night_research.bat; B4 sentinella canone ora su HASH del contenuto (DATA/audit/content_age.json: un touch non ringiovanisce piu' il canone); B5 firma stabile _sig() sul _cid. RITIRATO un numero del #69: '_cid = 6 cloni/notte' non regge sui dati (0 cloni a similarita' 0.80 su 261 critiche; a soglia bassa il merge fonde problemi DIVERSI) -> niente merge fuzzy, nasconderebbe guasti veri. C: SCALA-GENESIS.md ricreato (era scritto nella #69 ma mai salvato) e saliti 3 gradini: S0 FounderOS gira su :4100 (aggirato better-sqlite3/Node24 senza VS Build Tools), S1 CORE/genesis_db.py 8 tabelle + parent_id ricorsivo + costo nel run + FK attive, S2 CORE/genesis_seed.py idempotente (6 dipartimenti, 12 agenti veri, 7 tool con campo 'probe'), albero restituito da una CTE ricorsiva. TROVATO: il sistema e' stato MUTO dal 30/07 al 15/08 (17 notti, 0 commit automatici) - va riacceso.

**Prossimo step:** 1) RIACCENDERE IL SISTEMA: nina-loop, snapshot RAG, retention, inventario notturno e AI news watcher fermi da 17,5 giorni; API :5001 GIU' (dashboard gira ma 7 endpoint su 9 danno 500); RAG a 21.630 chunk (era ~32.800 il 24/06) - capire se e' rientro post-rebuild o perdita. 2) BATCH 3 (decisione Matteo, dry-run pronto, 0 bloccati dalla guardia): NON e' un blocco unico ma 3 gruppi - 10 episodi = correzione sicura; 4 da GIUDICARE (03/05/48/56, li' V32 non e' un'invenzione: ripetibilita' e calibrazione sono meccanica, e il 48 resterebbe sgrammaticato); 2 ROTTI non sporchi (EP_N2_28 e 55: Aggancio reale TRONCATO a meta' parola, residuo del bug max_tokens pre-#69, vanno RIGENERATI non rattoppati). 3) SCALA: S3 repository layer (chiude quando grep SELECT fuori da repos.py = 0). 4) SOCIAL: EP_N2_04 uscito il 16/08 alle ~09:00 invece che alle 21:00, capire perche'. NB canon_guard segnala 22 righe (non 0): il rilevatore e' stato riparato, il gate e' ambra fino al batch 3.

**Ultimi 5 milestone verificati:**
- Sessione #68 (21/07): ATTACCO ECOSISTEMA tutto il progetto — 5 fix applicati/verificati (finetune torchaudio 2.6.0; BACKUPS 42k->353 keep-N in retention.py; log werkzeug->WARNING; TI_NightCaroselli StartWhenAvailable; 2 path env-derived) + hook globale SessionStart auto-orientamento; sicurezza repo 0 segreti; report DOCS/ATTACCO_20260721; verifica 25/07 i fix hanno tenuto (backup bounded, audit fresco, nightly verde).
- Sessione #69 (28/07): RECUPERO ARRETRATO multi-agente - corsia Nina sbloccata (7 notti), 4 episodi persi recuperati (252->256, 0 orfani), vista RETE/SISTEMA riparata (proxy vite), troncatura Nina risolta (max_tokens 8000), -10 critiche/notte di rumore; verificato tsc 0 errori + storie_lint 0 violazioni; ritirati 2 miei errori (paginazione chromadb, 101 bare-except); trovato MIMS inventato come software in 5/8 episodi recenti (contamina il RAG sul prossimo progetto).
- Sessione #70 (16/08): contaminazione MIMS bonificata alla radice E nello storico - 8 episodi/16 file puliti (repo + MENTE), fonte fabbricata e numeri inventati rimossi, canon_guard 0 su tutti gli EP_N2 vivi, test di non-regressione VERDE; B3/B4/B5 chiusi (commit corsia Nina, sentinella su hash del contenuto, firma stabile delle critiche); ritirato il numero '6 cloni/notte' del #69 perche' non reggeva sui dati; SCALA-GENESIS.md ricreato e saliti S0-S1-S2 (FounderOS gira, genesis_db 8 tabelle, seed idempotente con albero da CTE ricorsiva). Verifiche: tsc -b 0 errori, py_compile 6/6, storie_lint 0 violazioni, 258 episodi 258 id unici.
- Sessione #70 (16/08): REGOLE unificate - erano 3 liste DIVERGENTI (CLAUDE.md, BRAIN/RULES.md fermo al 02/06 e servito alla dashboard, RIPASSO_S32-56) con numerazione sfasata: 'regola 6' voleva dire due cose diverse. Ora CLAUDE.md e' fonte unica a 12 regole (1-10 INVARIATE perche' mezzo repo le cita; +11 'il sistema propone, l'umano approva' rimessa nel testo dopo essere stata tolta il 20/06 pur restando legge nel codice e persino pubblicata in un episodio; +12 'insegna cio' che impari' recuperata da RULES.md dov'era l'unica regola viva). RULES.md ora DERIVATO via AUTOMATIONS/tools/sync_regole.py (marcatori, la sezione PDF_TO_MEMORY resta intatta, --check per il gate). Tappata la RADICE: setup.py:539 riscriveva RULES.md con la lista vecchia a ogni esecuzione. + BRAIN/REGOLE_GRAFICHE.md: le 2 regole rimandate a 'da fare insieme' dalla #57 finalmente scritte, decise contando l'uso reale su 68 file - palette slate + emerald/cyan/amber/indigo/rose + red, doppioni ritirati (zinc/green/sky/yellow/violet/pink), applicazione ADDITIVA senza repaint; lingua icone lucide=interfaccia (41 file su 68 gia' cosi'), emoji=solo contenuto, le frecce -> sono tipografia (261 delle 523 occorrenze). Servito anche alla dashboard. tsc -b verde.
- Sessione #70 (16/08) VERIFICA FINALE: ritirata la mia dichiarazione che A3 fosse chiuso - il gate era verde perche' canon_guard era CIECO, non perche' la contaminazione fosse finita (EP_N2_03/19/41/54 dicevano la stessa falsita' con parole fuori lista). Curato alla radice con una regola STRUTTURALE [pilastri-fusi]: la barra in GENESIS/V32 salda i pilastri in un soggetto solo ed e' sempre sbagliata, qualunque verbo segua; 0 falsi positivi su MENTE verificati. Trovato che la falsita' era gia' colata nel riflusso FATTI (fatti_dalle_storie_2026Q3.md, il file che alimenta il RAG): il tool ora lo copre. Batch 3 analizzato riga per riga e scomposto in 3 gruppi (10 sicuri, 4 da giudicare, 2 TRONCATI da rigenerare). Aggiunta la guardia anti-divergenza che non si fida delle scalette social (stantie: davano EP_SG_02_02 e EP_N2_04 non pubblicati mentre erano gia' pubblici) ma dell'artefatto carosello.

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
- *Il Segno che Rimane*
- *Il Ticchettio che Salva*

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
