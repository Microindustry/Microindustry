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

### Stato Live — v1.1.0 | Sessione #151 | 27 Jul 2026 04:07

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

**Milestone attivo:** Sessione #68 (21/07): ATTACCO ECOSISTEMA su TUTTO il progetto. 5 fix applicati e verificati a 4gg (25/07): finetune torchaudio 2.6.0 nel venv isolato (era 2.11 incompatibile, WinError 127); esplosione BACKUPS 42.141->353 con tetto keep-N in retention.py (700MB liberati, solo backup gitignored, zero file di progetto toccati); spam log werkzeug->WARNING; TI_NightCaroselli StartWhenAvailable=True; 2 path hardcoded resi env-derived. + hook globale Claude Code SessionStart (auto-orientamento ogni sessione, verificato funziona). Sicurezza repo BUONA (0 segreti hardcoded). Report DOCS/ATTACCO_20260721. I fix hanno TENUTO da soli: backup a 353, audit fresco, catena notturna verde.

**Prossimo step:** Al RIENTRO (30/07, promemoria Calendar) caricare i 3 post rimasti -> 21/21 (Nina EP_N2_05 19/08 + EP_N2_06 23/08, Sistema GENESIS EP_SG_02_04 21/08). Poi decidere i 3 filoni PROPOSTI #68: (A) smoke-test organi vitali, (B) audit bare-except, (C) pin requirements.txt. TI_FineTune conferma il fix torchaudio al run 26/07. Da revisionare: nuovi EP_N2_58-61 + bozze prodotti dagli agenti in vacanza.

**Ultimi 5 milestone verificati:**
- Sessione #67b (20-21/07): Pagina FB 'Il Mondo di Nina' creata e collegata a @ilmondodinina.ms (coppia FB+IG in Business Suite) - superato il labirinto Meta multi-account: si gestisce come owner Matteo Mims (benenatimatteo.mb@gmail.com), non come i profili IG che sono utenti limitati (blocked_ig_user_in_mbs).
- Sessione #67b: 18/21 caroselli programmati con date certe su 2 profili separati (Business Suite auto-pubblica). Sistema 10/11 (PRE_SG_01->V32+MIMS+VULCAN, fino 18/08, mar+ven 10:00); Nina 8/10 (PRE_01->EP_N2_04, fino 16/08, mer+dom). Restano 3 bloccati solo dal tetto 29gg (Nina EP_N2_05/06, Sistema GENESIS) -> promemoria Calendar 30/07.
- Sessione #67b: slide-ponte cross-profilo (slide 8 di PRE_04->@microindustry.ms e PRE_SG_04->@ilmondodinina.ms) rigenerate con nuovo tool riusabile CAROSELLI/_render_slide.py (chrome headless, 1 slide 1080x1350). Verificate a occhio, ricaricate.
- Sessione #67b: riorganizzati i sorgenti caroselli (git mv EP_N2_04/05/06 da _BOZZE/ a NINA/ perche in coda; _BOZZE = solo vere bozze). Handle corretto @ilmondodinina.ms ovunque. Doc di controllo _SCALETTA_INTERSECATA.md a moduli SEPARATI Nina/Sistema + STATO + PONTI. File copia-incolla _NINA_/_SISTEMA_COPIA_INCOLLA.md.
- Sessione #68 (21/07): ATTACCO ECOSISTEMA tutto il progetto — 5 fix applicati/verificati (finetune torchaudio 2.6.0; BACKUPS 42k->353 keep-N in retention.py; log werkzeug->WARNING; TI_NightCaroselli StartWhenAvailable; 2 path env-derived) + hook globale SessionStart auto-orientamento; sicurezza repo 0 segreti; report DOCS/ATTACCO_20260721; verifica 25/07 i fix hanno tenuto (backup bounded, audit fresco, nightly verde).

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
- *Il Nodo che Respira*
- *Il Dito nel Fango*

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
