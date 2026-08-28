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

### Stato Live — v3.0.0 · +648 commit | Sessione #162 | 28 Aug 2026 15:12

*Le barre sono metriche di gestione interna (STATE.json live), non misure fisiche:
lo stato reale della V32 oggi è un telaio in piedi + componentistica scelta.*

| Pilastro | Avanzamento gestione | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | Al telaio — in costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (sistema modulare d'acciaio) | `███░░░░░░░ 30%` | Attende la pressa VULCAN |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Adesso** — Il sistema si mantiene da solo. Di notte scrive gli episodi, si fa l'audit, si ripara e committa: dieci notti su undici senza che io tocchi niente. E soprattutto ha imparato a controllare se stesso — quando raccontava di sé qualcosa di falso, ora c'è una guardia che lo ferma prima che finisca in pubblico. Un sistema che si accorge dei propri errori vale piu' di uno che non ne fa mai perche' non prova.

**Prossimo** — Dare a GENESIS un organigramma vero. Gli agenti che lavorano di notte esistono gia', ma vivevano sparsi tra file e cartelle: adesso hanno un database che li tiene in albero, con un solo posto da cui si interroga. Il passo dopo e' vederli nella dashboard come si guarda un reparto in officina: chi fa cosa, chi risponde a chi, cosa e' acceso adesso.

<details>
<summary>🔩 Dettaglio tecnico — milestone attivo e ultimi lavori verificati (per chi vuole i dadi e i bit)</summary>

**Milestone attivo:** Sessione #71 (27/08): SMENTITO l'handoff. Il sistema NON era spento: si e' riacceso da solo il 17/08 e ha lavorato 10 notti su 11 (night_audit, inventario, nina_rag_loop, story_agent). API :5001 non e' giu': 17 endpoint su 18 danno 200; md-files non e' rotto ma lento (4,0s); il RAG e' rientro non perdita (21.630 il 16/08 -> 22.637 il 26/08, sale). GUASTO VERO trovato: /api/view-index dava 500 dal 20/08 perche' DATA/view_index.json era TRONCATO a meta' scrittura; la radice e' md_view_pipeline._update_index che riscriveva l'indice INTERO in modo non atomico a ogni singolo file (487 finestre di corruzione, O(n^2)) -> scrittura atomica tmp+fsync+os.replace con retry Windows, indice tollerante al file corrotto, rebuild che scrive UNA volta sola. Indice ricostruito: 487 view, endpoint 200. canon_guard non era nemmeno eseguibile a mano (UnicodeEncodeError su console cp1252): stdout in utf-8, stesso fix su genesis_seed --albero (mai arrivato in fondo). Igiene: _VAULT escluso dalla view pipeline (generava view di CREDENZIALI_BACKUP.md servite dall'API; nessun leak in git, entrambi gitignorati). BATCH 3 GRUPPO 1 applicato dopo aver letto le frasi in contesto: 10 episodi (16/19/35/38/41/53/54/62 + 10 e 44 che il tool non copriva, variante GENESIS/TITANIUM_OS), 25 sostituzioni, idempotente, 0 bloccati dalla guardia carosello. GATE canone: da 22 righe a 8, e le 8 sono esattamente i 7 episodi sospesi. S3 CHIUSO: CORE/repos.py, grep SELECT fuori = 0.

**Prossimo step:** 1) SOSPESI del batch 3 (decide Matteo): per 03/05/46/48/56 il collasso generico su GENESIS e' SBAGLIATO - non ripulisce, sposta il falso dal pilastro meccanico a quello software (ripetibilita'/calibrazione = V32; golden template = MIMS/VULCAN; il 48 diventa sgrammaticato; il 46 e' misto). Proposta: 5 riscritture mirate, una frase l'una. 2) EP_N2_28 e 55 da RIGENERARE (troncati a meta' parola, confermato leggendoli). 3) EP_N2_16: due numeri inventati spacciati per FATTI ('70% dell'affidabilita'', 'errori da 10% a 2-3%') che la regola generica non vede. 4) S4 della scala: organigramma dal db in DASHBOARD (oggi l'albero si vede solo da CLI). 5) Igiene notturna arretrata (night_audit 26/08): critiche stantie da 49gg, _CANONE.md fermo a EP_N2_64 mentre su disco c'e' il 67, AI news watcher muto da 4 giorni, 8 CVE fixabili. 6) Push: 2 commit automatici del 26/08 + i fix di questa sessione, non ancora committati.

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
| `MENTE RAG v4.2` | ChromaDB hybrid BM25+semantico+CrossEncoder, chunking heading-aware + GraphRAG-lite — ~22.637 chunk, si aggiorna da solo a ogni modifica |
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
- *Il Turno di Guardia*
- *Il Grande Loop: quando il gesto rimane*
- *Il Nodo che Respira*
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

Calcoli di progetto (non ancora dimostrati sul campo): BEP V32 **61 ore** | Tariffa target **EUR 45/h**

---

*Aggiornato automaticamente ogni notte da TITANIUM_OS · TI_NightPush 04:07*
