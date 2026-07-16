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

### Stato Live — v1.1.0 | Sessione #129 | 16 Jul 2026 04:07

*Le barre sono metriche di gestione interna (STATE.json live), non misure fisiche:
lo stato reale della V32 oggi è un telaio in piedi + componentistica scelta.*

| Pilastro | Avanzamento gestione | Stato |
|----------|-----------|-------|
| **V32 CNC** (fresatrice 3 assi) | `██████░░░░ 65%` | Al telaio — in costruzione |
| **GENESIS** (ecosistema AI) | `███████░░░ 70%` | Building |
| **MIMS** (sistema modulare d'acciaio) | `███░░░░░░░ 30%` | Attende la pressa VULCAN |
| **VITA NATURA** (centro estetico) | `████░░░░░░ 40%` | Attivo |

**Milestone attivo:** Sessione #60 (15/07): TABELLONE CAROSELLI PULITO 14/14 (QC 0 falle, 0 legacy). PRE_04 'Tutto e' vero' creato -> SERIE PRE NINA COMPLETA 4/4 (patto di verita', slide PONTE al binario Sistema, onde 31-40). PRE_03 v6.1 volto grande/libero in copertina (ordine Matteo). EP_SG_01_03 'Il Distacco' revisionato+promosso -> FINE RODAGGIO apprendista 3/3 (S1 3/69); coda estesa: CAP 2 L'ORGANISMO 6 item pending (guardie esplicite negli angoli). EP_N2_03 'Mille Volte Uguale' compilato (scaletta approvata prima) = primo del cammino a standard; poi 'sistema': EP_N2_01 v3 + EP_N2_02 v2 a standard (16->10, open loop 02 corretto). Regione 0 completa a carosello (caselle 1-2-3), cammino 3/53, totale Nina 7/57. Convenzione onde: PRE 1-40, cammino casella N = fase 40+(N-1)*10. ATTACCO #2 colli di bottiglia IMPOSTATO: DOCS/ATTACCO_20260716/_PIANO.md (Fable 5, propose-only, ricognizione GitHub strumenti).
**Prossimo step:** PROSSIMA (#61): 1) P0 verifica AUTOGENERAZIONE episodi->RAG (story_agent/night_research/riflusso FATTI, con numeri) 2) P0 profilo GitHub personale aggiornato (README + pin 5 repo) 3) ATTACCO #2 colli di bottiglia (5 agenti Fable propose-only, piano in DOCS/ATTACCO_20260716) 4) risultati LinkedIn PRE_SG_01 (gated) 5) revisione bozza notturna EP_SG_02_01 V32.

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

### Ultimi 5 milestone verificati
- CAROSELLI a binari (NINA/SISTEMA) + scoperta ricorsiva negli script + README-segnaletica a ogni livello; QC 11 cartelle 0 falle post-riordino (15/07/2026)
- Serie PRE Nina COMPLETA 4/4: PRE_04 'Tutto e' vero' (patto di verita' + slide PONTE, onde 31-40) + PRE_03 v6.1 volto grande in copertina; QC verde (15/07/2026 #60)
- Apprendista notturno RODATO 3/3: EP_SG_01_03 revisionato (kicker par.7.5, caption famiglia) e promosso; coda estesa CAP 2 L'ORGANISMO 6 item con guardie esplicite (15/07/2026 #60)
- Cammino Nina a standard: EP_N2_03 compilato su scaletta approvata (precedente per i 53) + EP_N2_01 v3/EP_N2_02 v2 (16->10, open loop corretto); regione 0 completa, TABELLONE 14/14 QC 0 falle 0 legacy; convenzione onde cammino fase 40+(N-1)*10 (15/07/2026 #60)
- ATTACCO #2 impostato: DOCS/ATTACCO_20260716/_PIANO.md - colli di bottiglia ecosistema, 5 agenti Fable propose-only + ricognizione GitHub strumenti; P0 = verifica autogenerazione episodi->RAG + profilo GitHub (15/07/2026 #60)

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
