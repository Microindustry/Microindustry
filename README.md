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

### Stato Live — v1.1.0 | Sessione #109 | 08 Jul 2026 04:07

| Pilastro | Progresso | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | In costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (stampo tegole) | `███░░░░░░░ 30%` | Attende V32 |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #55 (07/07): PIANO #54 COMPLETO — ondate A-B-C tutte chiuse + filone verita' sparsa (1a tranche). Boot sporco curato alla radice (legacy CORE/watchdog respawnava doppioni -> single-instance su watchdog/watcher/api, guardia porta 5001, START_ECOSYSTEM stub, fix vite7 --silent). Retention disco (5 regole, 2.24GB) + deep_freeze senza chroma (2035->216MB). Canone ENFORCED: canon-pin RRF (27 note _CANONE) + rebuild esclusivo 18113==18113 (535 chunk persi recuperati) + indici cammino/pietre agganciati al build. 4 sentinelle notturne nuove (organi vivi, canone vault, pip-audit 42 CVE fixabili, QC 51 episodi). CLOBBER STATE.json trovato in flagrante e curato (load fail-safe + write atomico) — 68 milestone/107 sessioni ripristinate + snapshot giornaliero. NodeKit (4 copie -> 1, -256 righe, pixel-identici). Vista CRITICHE eliminata (decisione Matteo) -> CRITICHE.md notturno.
**Prossimo step:** PROSSIMA SESSIONE #56, in ordine: (1) resto filone verita' sparsa — SYSTEM_TREE duplicato in MappaView (au18), % MIMS computata-vs-dichiarata, doc AUTOMATIONS_MASTER; (2) EP_N2_03 'la Misura' carosello 16 slide; (3) sessione CVE (42 fix, test finetune dopo); (4) decisione Matteo su viste doppie neuro/sinapsi. GATED MATTEO: hardware Vevor+ER20+UPS, chiave Semantic Scholar, trade secrets in _VAULT.

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
- Sessione #55: igiene disco A REGOLA — retention.py (R1 chroma-debris keep-1+7gg, R2 BACKUPS/ts 45gg, R3 FULL keep-1, R4 log 30gg, R5 snapshots=3; dry-run default, report DATA/retention_last.json) in night_push; prima passata 2.24GB. Radice del gonfiore: deep_freeze zippava le chroma_db (2035MB il 05/07 vs 185 il 21/06) -> esclusione + freeze rigenerato 216MB AES verificato
- Sessione #55: canone ENFORCED (07 P1) — canon-pin nel retrieval (set wikilink _CANONE.md, 27 note, cache mtime: bonus RRF in selezione + slot riservato top-k + campo canon in output; reranker resta giudice) + night_audit.check_canone_vault (id-collision note attive + freshness/copertura _CANONE 51==51). Rebuild esclusivo TOP10 #3: semantico==bm25 18113==18113, 535 chunk persi dal boot sporco recuperati, 0 chunk archivio
- Sessione #55: 4 sentinelle notturne — organi vivi (7 output con soglia gg: organo che tace = critica), pip-audit settimanale (42 CVE fixabili in 9 pacchetti, solo fixabili = no rumore da stack pinnato), QC strutturale 51 EP_N2 (0 rotture; 28/51 senza open-loop = metrica), graphify update in coda notturna (grafo era fermo al 7/6: ora 7338 nodi). Indici cammino/pietre agganciati a build_episodes_json (step 7): un documento-verita' che si rigenera non deriva
- Sessione #55: STATE.json CLOBBER trovato in flagrante (20:40) e CURATO — state_updater._load_state su decode error (lettura a meta' scrittura) restituiva il template default e il watcher lo salvava sopra: 68 milestone/107 sessioni/6 blockers cancellati e RIPRISTINATI dalla copia in contesto. Fix: load fail-safe (illeggibile = salta, mai ricreare) + _save_state ATOMICO (tmp+os.replace) + state_snapshot.py giornaliero (_VAULT, rotazione 14, valida prima di copiare). ERA la causa storica delle percentuali divergenti (au08/gc04)
- Sessione #55: pulizia dashboard — NodeKit.tsx (NodeTile/NodeLevel condivisi: erano 4 copie identiche-a-tema-diverso, -256 righe, tsc verde + screenshot prima/dopo pixel-identici, critica gc01 chiusa). Vista CRITICHE ELIMINATA su decisione Matteo ('non si aggiorna') -> CRITICHE.md stile bussola in root (critiche_md.py: polso + canone per progetto + auto-audit aperte), rigenerato ogni notte da night_audit e auto-committato da night_push; fonti = i 2 JSON vivi

### Episodi recenti
- *Il Battito del Guardiano*
- *Il Cartellino sulla Stoffa*

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
