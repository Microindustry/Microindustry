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

### Stato Live — v1.1.0 | Sessione #114 | 13 Jul 2026 09:20

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #56 (08/07): VERITA' SPARSA punto 1 CHIUSO (au18 Mappa derivata da mappaData.ts, au09 % con nome esplicito, au16 MASTER declassato ad archivio) + LE 3 FACCE (decisione Matteo): sidebar TITANIUM/NINA/PUBBLICAZIONI, ripasso #32-56 in DOCS/RIPASSO_S32-56.md, vista PUBBLICAZIONI (stack Postiz+Graph API ri-verificato: IG max 10 slide, LinkedIn=PDF, slide gia' 1080x1350 a norma, Postiz ha MCP server) con scaletta attivazione 9 passi. Nuovo binario deciso: storie di sistema in prima persona (voce Matteo). Nina = primo treno, la forza e' la pipeline.
**Prossimo step:** PROSSIMA SESSIONE #57 in MODO INGEGNERIZZATO (requisiti->design->additivo->verifica misurabile), in ordine: (1) analisi VALORE per pilastro (doc MENTE poi card home derivata); (2) HR/CV vivo (CV attuale = rumore); (3) attivazione PUBBLICAZIONI (passi 1-4 gated Matteo: mail, FB/IG, app Meta, Docker); (4) EP_N2_03 formato doppio; (5) CVE + viste doppie + backlog #52. GATED: hardware Vevor+ER20+UPS, chiave Semantic Scholar, trade secrets in _VAULT.

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
- Sessione #55: 4 sentinelle notturne — organi vivi (7 output con soglia gg: organo che tace = critica), pip-audit settimanale (42 CVE fixabili in 9 pacchetti, solo fixabili = no rumore da stack pinnato), QC strutturale 51 EP_N2 (0 rotture; 28/51 senza open-loop = metrica), graphify update in coda notturna (grafo era fermo al 7/6: ora 7338 nodi). Indici cammino/pietre agganciati a build_episodes_json (step 7): un documento-verita' che si rigenera non deriva
- Sessione #55: STATE.json CLOBBER trovato in flagrante (20:40) e CURATO — state_updater._load_state su decode error (lettura a meta' scrittura) restituiva il template default e il watcher lo salvava sopra: 68 milestone/107 sessioni/6 blockers cancellati e RIPRISTINATI dalla copia in contesto. Fix: load fail-safe (illeggibile = salta, mai ricreare) + _save_state ATOMICO (tmp+os.replace) + state_snapshot.py giornaliero (_VAULT, rotazione 14, valida prima di copiare). ERA la causa storica delle percentuali divergenti (au08/gc04)
- Sessione #55: pulizia dashboard — NodeKit.tsx (NodeTile/NodeLevel condivisi: erano 4 copie identiche-a-tema-diverso, -256 righe, tsc verde + screenshot prima/dopo pixel-identici, critica gc01 chiusa). Vista CRITICHE ELIMINATA su decisione Matteo ('non si aggiorna') -> CRITICHE.md stile bussola in root (critiche_md.py: polso + canone per progetto + auto-audit aperte), rigenerato ogni notte da night_audit e auto-committato da night_push; fonti = i 2 JSON vivi
- Verita' sparsa CHIUSA (08/07 sess#56): SYSTEM_TREE derivato da mappaData.ts (adapter SkillNode->MapNode, % computate nodeProgress, ROOT=media, -84 righe a mano, pct_sync v1.1 ritirato da MappaView) + % MIMS/GENESIS con nome esplicito (voci mappa vs pilastro STATE) + AUTOMATIONS_MASTER v1.3 archivio storico con 4 fonti vive
- LE 3 FACCE (08/07 sess#56, decisione Matteo): sidebar TITANIUM/NINA/PUBBLICAZIONI (deep-link intatti, Archivio sotto-voce), RIPASSO_S32-56.md (5 fasi+canone operativo+carattere), PubblicazioniView (trovato/pipeline/criteri/scaletta 9 passi), vincoli ri-verificati doc Meta (10 slide max, LinkedIn PDF, slide 1080x1350 gia' a norma, Postiz MCP), binario nuovo 'voce Matteo', tsc verde + screenshot

### Episodi recenti
- *Il Direttore Invisibile*
- *Il Battito del Guardiano*

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
