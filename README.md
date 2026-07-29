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

### Stato Live — v1.1.0 | Sessione #154 | 29 Jul 2026 04:07

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

**Milestone attivo:** Sessione #69 (28/07): RECUPERO ARRETRATO con 3 agenti read-only in parallelo (episodi/bozze, dashboard, critiche+proposte), Claude verificatore. FIX APPLICATI E VERIFICATI: corsia caroselli NINA sbloccata dopo 7 notti ferme (coda con EP_N2_04/05/06 ancora 'bozza_verde' benche' promossi -> tetto backlog 6>=6 falso; backlog reale 6->3); 4 episodi persi recuperati (audit_episodes match-per-titolo rimosso, story_agent riusa 'Episodio 69' -> 252->256 episodi, 0 orfani); vista RETE sorgente SISTEMA riparata (4 endpoint mancavano dal proxy vite -> tornavano index.html); troncatura episodi Nina risolta (nina_agent max_tokens 4000->8000, si perdeva l'open-loop in meta' serie); -10 critiche/notte di rumore (legenda organi_vivi=eta'-in-giorni nel SYSTEM_PROMPT + warning HF zittito in vault_intersect). RITIRATI 2 miei errori: la paginazione chromadb NON risolve il 503 (segmento HNSW incoerente: limit=10 da' 0 embedding -> cura = rag_recover --drop-hnsw, click Matteo) e i '101 bare-except' del #68 erano falsi (1 solo nel codice proprio). TROVATO problema di VERITA': MIMS descritto come software/AI in 5 episodi su 8 recenti (acronimo inventato) mentre e' meccanica - e MIMS e' il PROSSIMO progetto dopo caroselli+ecosistema.

**Prossimo step:** ATTACCARE E CORREGGERE (ordine Matteo #69): 1) fermare la contaminazione MIMS alla radice - iniettare _CANONE.md nel prompt dell'Architetto (nina_agent.py:188) con regola 'se non c'e' aggancio reale lascia vuoto' + regola canon_guard che segnala MIMS/VULCAN descritti come software; 2) correggere i 5 episodi gia' contaminati (EP_N2_57/59/60/63/64) e le fonti fabbricate nei FATTI; 3) fix meccanici residui (casella '?' in nina_rag_loop.py:180, guardia titoli unici, commit del loop Nina, sentinella canone su hash non mtime, euristiche rumorose _cid/rate-limit/open-loop/canon_guard); 4) implementare le NOVITA' IA ingegnerizzandole nel progetto; 5) bozze: 6 pronte + EP_N2_09 (slide vuota) + EP_SG_03_03 (numero vietato + open-loop all'indietro). POI: finire i caroselli, settare l'ecosistema, e partire con MIMS (prossimo progetto).

**Ultimi 5 milestone verificati:**
- Sessione #67b: 18/21 caroselli programmati con date certe su 2 profili separati (Business Suite auto-pubblica). Sistema 10/11 (PRE_SG_01->V32+MIMS+VULCAN, fino 18/08, mar+ven 10:00); Nina 8/10 (PRE_01->EP_N2_04, fino 16/08, mer+dom). Restano 3 bloccati solo dal tetto 29gg (Nina EP_N2_05/06, Sistema GENESIS) -> promemoria Calendar 30/07.
- Sessione #67b: slide-ponte cross-profilo (slide 8 di PRE_04->@microindustry.ms e PRE_SG_04->@ilmondodinina.ms) rigenerate con nuovo tool riusabile CAROSELLI/_render_slide.py (chrome headless, 1 slide 1080x1350). Verificate a occhio, ricaricate.
- Sessione #67b: riorganizzati i sorgenti caroselli (git mv EP_N2_04/05/06 da _BOZZE/ a NINA/ perche in coda; _BOZZE = solo vere bozze). Handle corretto @ilmondodinina.ms ovunque. Doc di controllo _SCALETTA_INTERSECATA.md a moduli SEPARATI Nina/Sistema + STATO + PONTI. File copia-incolla _NINA_/_SISTEMA_COPIA_INCOLLA.md.
- Sessione #68 (21/07): ATTACCO ECOSISTEMA tutto il progetto — 5 fix applicati/verificati (finetune torchaudio 2.6.0; BACKUPS 42k->353 keep-N in retention.py; log werkzeug->WARNING; TI_NightCaroselli StartWhenAvailable; 2 path env-derived) + hook globale SessionStart auto-orientamento; sicurezza repo 0 segreti; report DOCS/ATTACCO_20260721; verifica 25/07 i fix hanno tenuto (backup bounded, audit fresco, nightly verde).
- Sessione #69 (28/07): RECUPERO ARRETRATO multi-agente - corsia Nina sbloccata (7 notti), 4 episodi persi recuperati (252->256, 0 orfani), vista RETE/SISTEMA riparata (proxy vite), troncatura Nina risolta (max_tokens 8000), -10 critiche/notte di rumore; verificato tsc 0 errori + storie_lint 0 violazioni; ritirati 2 miei errori (paginazione chromadb, 101 bare-except); trovato MIMS inventato come software in 5/8 episodi recenti (contamina il RAG sul prossimo progetto).

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
- *Il Sussurratore che Indovina*
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
