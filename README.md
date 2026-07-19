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

### Stato Live — v1.1.0 | Sessione #137 | 19 Jul 2026 04:07

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

**Milestone attivo:** Sessione #66 (19/07): LANCIO SOCIAL. Identita microindustry (logo M oro + banner "COSTRUIRE MODULO A MODULO"), IG @microindustry.ms passato a Business, Pagina LinkedIn 136056455. Strategia SPLIT: LinkedIn best-first (V32 manuale lun 20/07), Meta (FB+IG) preambolo in ordine 2/sett. Scaletta 8 post Meta + 10 post Nina programmate in _SOCIAL_QUEUE (JPG rinominate 01-10). Account Nina preparato (foto profilo dal volto PRE_03, bio, coda). Notturno autonomo: generazione EP viva, coda Nina estesa a 10, 3 bozze SISTEMA (MIMS/VULCAN/GENESIS) canon-clean da approvare di giorno.

**Prossimo step:** Matteo: compilare profili IG (microindustry + creare account Nina @ilmondodinina), collegare Pagina FB, programmare i post via Business Suite; lun 20/07 caricare V32 su LinkedIn (PDF pronto). Poi approvare le 3 bozze SISTEMA.

**Ultimi 5 milestone verificati:**
- Sessione #62 ONDATA C: finetune vero - episodes_to_dataset ricorsivo (30->176 episodi Matteo-voce, esclusi Nina/staging) + night_finetune --overwrite_output_dir + verifica global_step>0 (no piu' finto-verde); RandomDelay sui 3 task GPU (StoryAgent/NightResearch/FineTune) contro il MemoryError al boot
- Sessione #62 BACKLOG RAG (attacco #2 dominio 2): #7 fatti_reflux a rotazione trimestrale (fatti_dalle_storie_YYYYQn.md, i trimestri chiusi non cambiano -> zero re-embed, verificato idempotente, 5 monoliti migrati) + #8 demote_dirs opt-in (malus selezione simmetrico al canone, wired night_caroselli/nina_agent/story_agent + /api/rag/search?demote=STORIE) + #6 check_doppioni_copia in night_audit (trova i *_copia accanto all'originale) + #10 daily-note YYYY-MM-DD fuori dall'indice (_is_nav_file). Dominio RAG dell'attacco #2 completo.
- Sessione #64 (17/07): Postiz montato fino al bordo (repo tools/postiz-docker-compose, JWT_SECRET generato, config in _VAULT/ACCOUNTS/postiz.md, redirect LinkedIn deciso) + WSL2+Docker Desktop 4.82 installati (manca reboot). + profilo GitHub v2.1: sintesi umana Adesso/Prossimo + dettaglio tecnico a scomparsa (<details>), canon_guard passato, additivo con fallback BRAIN/profile_public.json. + baseline LinkedIn PRE_SG_01 letto: pubblico perfetto (saldatori/metalmecc/Milano valida binario SG "parla ai pari"), engagement thin (2 reaz/0 salv) -> leva=hook, formato 4:5 a norma.
- Sessione #65 (17/07): POSTIZ montato e VIVO (Docker Desktop 4.82, 8 container sani, UI localhost:4007, admin creato). App LinkedIn microindustry-postiz creata+VERIFICATA (id 247572507, Pagina microindustry 136056455), Client ID/Secret nel compose (env confermato nel container), prodotti Sign-In OIDC + Share concessi. Errore redirect_uri RISOLTO (2 redirect accettati, diagnosi da URL reale + provider code). BLOCCO su timbro LinkedIn: pubblicare su Pagina richiede scope organization = Community Management API, richiesta e in attesa concessione (muro esterno, non config). Ripresa in 1 click quando concessa. Stack stoppato per la notte (RAM notturne GPU). Stato in _VAULT/ACCOUNTS/postiz.md.
- Sessione #66 (19/07): LANCIO SOCIAL - identita visiva microindustry (logo/banner/kit IG in POSTER/BRAND, rigenerabili via chrome headless), IG Business, strategia SPLIT decisa, scaletta 8 post Meta (PRE_SG_01-04 + EP_SG_01_01/02/03 + EP_SG_02_01) programmata in _SOCIAL_QUEUE con JPG rinominate 01-10 (fix ordine carosello), regola caption hook+domanda+hashtag-primo-commento, tutte canon_guard.scan_public clean. Account Nina preparato (volto PRE_03 -> foto profilo, NINA_IG_PROFILO, coda 10 post ritmo buonanotte mer+dom in _SOCIAL_QUEUE_NINA). Notturno: EP gen verificata viva (bozze SISTEMA+Nina, QC ok), coda Nina estesa auto-promuovendo EP_N2_04/05/06.

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

Calcoli di progetto (non ancora dimostrati sul campo): BEP V32 **61 ore** | Tariffa target **EUR 45/h**

---

*Aggiornato automaticamente ogni notte da TITANIUM_OS · TI_NightPush 04:07*
