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

### Stato Live — v3.0.0 · +726 commit | Sessione #183 | 31 Oct 2026 06:32

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

**Milestone attivo:** #74: analisi del rifacimento grafico;

**Prossimo step:** Pulizia della dashboard (codice morto, 11 dipendenze), poi la fonte dati del ferro: l'API legge distinte, MENTE e FOTO

**Ultimi 5 milestone verificati:**
- Sessione #70 (16/08): REGOLE unificate - erano 3 liste DIVERGENTI (CLAUDE.md, BRAIN/RULES.md fermo al 02/06 e servito alla dashboard, RIPASSO_S32-56) con numerazione sfasata: 'regola 6' voleva dire due cose diverse. Ora CLAUDE.md e' fonte unica a 12 regole (1-10 INVARIATE perche' mezzo repo le cita; +11 'il sistema propone, l'umano approva' rimessa nel testo dopo essere stata tolta il 20/06 pur restando legge nel codice e persino pubblicata in un episodio; +12 'insegna cio' che impari' recuperata da RULES.md dov'era l'unica regola viva). RULES.md ora DERIVATO via AUTOMATIONS/tools/sync_regole.py (marcatori, la sezione PDF_TO_MEMORY resta intatta, --check per il gate). Tappata la RADICE: setup.py:539 riscriveva RULES.md con la lista vecchia a ogni esecuzione. + BRAIN/REGOLE_GRAFICHE.md: le 2 regole rimandate a 'da fare insieme' dalla #57 finalmente scritte, decise contando l'uso reale su 68 file - palette slate + emerald/cyan/amber/indigo/rose + red, doppioni ritirati (zinc/green/sky/yellow/violet/pink), applicazione ADDITIVA senza repaint; lingua icone lucide=interfaccia (41 file su 68 gia' cosi'), emoji=solo contenuto, le frecce -> sono tipografia (261 delle 523 occorrenze). Servito anche alla dashboard. tsc -b verde.
- Sessione #70 (16/08) VERIFICA FINALE: ritirata la mia dichiarazione che A3 fosse chiuso - il gate era verde perche' canon_guard era CIECO, non perche' la contaminazione fosse finita (EP_N2_03/19/41/54 dicevano la stessa falsita' con parole fuori lista). Curato alla radice con una regola STRUTTURALE [pilastri-fusi]: la barra in GENESIS/V32 salda i pilastri in un soggetto solo ed e' sempre sbagliata, qualunque verbo segua; 0 falsi positivi su MENTE verificati. Trovato che la falsita' era gia' colata nel riflusso FATTI (fatti_dalle_storie_2026Q3.md, il file che alimenta il RAG): il tool ora lo copre. Batch 3 analizzato riga per riga e scomposto in 3 gruppi (10 sicuri, 4 da giudicare, 2 TRONCATI da rigenerare). Aggiunta la guardia anti-divergenza che non si fida delle scalette social (stantie: davano EP_SG_02_02 e EP_N2_04 non pubblicati mentre erano gia' pubblici) ma dell'artefatto carosello.
- Sessione #74 (28/09): prima accensione con la catena d'avvio verificata - esito 0 per catena e push, critiche 300 -> 19
- Sessione #74 (28/09): VULCAN pilastro in STATE, db GENESIS e dashboard (home, barra di stato, pitch verificati a schermo, tsc -b verde); FIT-PARK fuori dal db
- Sessione #74 (28/09): tre distinte del ferro (V32, VULCAN, MIMS) in MENTE come fonte unica, trovabili dal RAG; martinetto Vevor da comprare, non adesso

</details>

---

### Nodi GENESIS attivi

| Nodo | Descrizione |
|------|-------------|
| `MENTE RAG v4.2` | ChromaDB hybrid BM25+semantico+CrossEncoder, chunking heading-aware + GraphRAG-lite — ~24.345 chunk, si aggiorna da solo a ogni modifica |
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
- *Il Diario che Pensa*
- *La Giuntura che Respira*
- *Il Libro delle Ricette di Nonna*
- *La mano che insegna alla notte*

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
