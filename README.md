# Matteo Benenati — Microindustry

```
╔══════════════════════════════════════════════════════════════════════╗
║  ARTIGIANO INDUSTRIALE + SYSTEM BUILDER                              ║
║  15 anni in officina. Titanio, robot, presse, CNC da zero.           ║
║  L'officina gira. Il sistema la gestisce. Io costruisco il prossimo. ║
╚══════════════════════════════════════════════════════════════════════╝
```

---

## Il problema che ha generato tutto questo

Ci sono persone che lavorano il metallo di giorno e scrivono codice di notte.

Ho saldato scarichi in titanio per i team MotoGP da SCProject. Ho programmato robot ESSEGI per linee di packaging industriale. Ho operato presse DATWLER e fatto controllo qualità su impianti di refrigerazione LU.VE. Quindici anni di industria pesante — mani nell'acciaio, testa sempre su più fronti contemporaneamente.

Il problema non era la competenza. Era la gestione cognitiva.

Un cervello che lavora ad alta frequenza — che connette segnali deboli, vede pattern, genera idee in continuazione — non può tenere tutto in memoria. Le idee arrivano a valanga, i progetti si moltiplicano, la concentrazione si spezza nel momento sbagliato. Un'agenda non basta. Un task manager non basta. Serviva qualcosa di strutturalmente diverso: non uno strumento, ma un **sistema operativo per la mente**.

Da lì è nato TITANIUM_OS.

---

## Cosa è Microindustry

Non un side project. Non un portfolio. Un'entità operativa.

**Microindustry** è la struttura che tiene insieme fisico e digitale. Da una parte: una fresatrice CNC di precisione costruita da zero, una pressa da 20 tonnellate, un sistema di connettori modulari (MIMS) che sfida i prodotti in alluminio estruso di mercato. Dall'altra: TITANIUM_OS — il sistema operativo cognitivo che gestisce tutto, che non dorme, che trasforma ogni decisione tecnica in conoscenza strutturata e ogni milestone in contenuto pubblicabile.

L'obiettivo non è impressionare. È produrre valore misurabile ogni giorno, con il minor attrito cognitivo possibile.

---

## La catena che produce valore

Ogni pezzo di questa catena è pensato per alimentare il prossimo:

```
V32 CNC di precisione
    │
    │  La fresatrice di precisione produce i componenti fisici.
    │  Costruita da zero. Costo: EUR 2.250. ROI anno 1: 322%.
    ▼
VULCAN — pressa 20t + ricette polimeri proprietarie
    │
    │  VULCAN stampa le tiles MIMS a caldo.
    │  Le ricette polimeri sono il moat competitivo.
    ▼
MIMS — sistema modulare proprietario
    │
    │  Il mercato è dominato dall'alluminio estruso (Item, Bosch Rexroth, MayTec):
    │  costoso, rigido, supply chain lunga, zero differenziazione.
    │  MIMS è diverso: polimero composito, connettore fisico brevettato,
    │  produzione locale on-demand. Chi entra nel sistema MIMS non ne esce.
    ▼
FIT PARK 4.0 — prima applicazione di mercato
    │
    │  Area fitness con strutture MIMS proprietarie + tornello connesso.
    │  Il prodotto che mostra il sistema al mercato.
    ▼
TITANIUM_OS gestisce tutto in tempo reale
```

---

## Il sistema che lavora mentre dormo

Questa è la parte che più dimostra il concetto di Microindustry come entità operativa autonoma.

**Ogni notte, in automatico:**

| Ora | Cosa succede |
|-----|-------------|
| 02:07 | **Story Agent** legge i commit Git delle ultime 24h e genera episodi podcast narrativi. Da codice a storia, in automatico. |
| 03:00 | **Deep Freeze** cripta con AES-256 e archivia ogni file importante. Il backup non dipende dal ricordarsi di farlo. |
| 03:37 | **Night Research** scansiona 13 database scientifici (arXiv, OpenAlex, GitHub, Semantic Scholar, POLITesi...) cercando ricerche rilevanti per i progetti attivi. |
| 04:07 | **Night Push** committa tutto e pusha al repository. Il codice non commitato non esiste. |
| 07:30 | **Daily Brief** genera il report mattutino: milestone attivo, blockers, focus del giorno. La giornata inizia già orientata. |

**Durante il giorno, in automatico:**
- Ogni file aggiunto a MENTE/ → indice RAG aggiornato in <20 secondi
- Ogni milestone verificato → episodio podcast + aggiornamento dataset LLM
- Ogni sessione di lavoro → RIAVVIO_SESSIONE.txt aggiornato per la sessione successiva
- Ogni commit → STATE.json sincronizzato

Il sistema non si ferma quando mi fermo io.

---

## TITANIUM_OS — i nodi attivi

| Nodo | Cosa fa |
|------|---------|
| **MCP Server** | 7 strumenti esposti a Claude Code: stato live, RAG, agenti, aggiornamenti. Claude non legge file — accede ai dati direttamente via protocollo. |
| **RAG v4.0 ibrido** | 800+ documenti in italiano/inglese/tedesco. Ricerca per significato (ChromaDB), per parola esatta (BM25), riordinata da un reranker neurale. Risponde con i tuoi documenti, non con dati generici. |
| **NEXUS Swarm** | Orchestratore multi-agente: una query complessa viene distribuita agli agenti specializzati in parallelo e i risultati vengono aggregati. |
| **ARGUS v2** | Computer use con architettura ibrida: OmniParser locale (YOLO + OCR) per il riconoscimento veloce, Claude Sonnet solo come fallback per i casi ambigui. Costo API ridotto dell'80%. |
| **Dashboard v7.0** | React 19 — sidebar verticale, AgentsView con glassmorphism, mappa drill-down SVG, rete t-SNE 3D interattiva in Three.js. Stato live di ogni nodo e pilastro. |
| **Gmail + Calendar MCP** | Lettura e scrittura diretta da Claude Code. Niente tab browser, niente copia-incolla. |

---

## 8 Agenti AI — ognuno nel suo dominio

Il sistema non usa un modello generalista per tutto. Usa agenti specializzati che condividono la stessa knowledge base RAG ma operano in domini separati.

| Agente | Dominio | Esempio di uso |
|--------|---------|----------------|
| **THEMIS** | Codice, analisi tecnica, GENESIS | "Analizza il bottleneck nel pipeline RAG" |
| **FORGE** | Meccanica, saldatura, CNC, officina | "Gioco ottimale per tiranti M10 Config G?" |
| **TESLA** | Elettronica, PLC Siemens, IoT, sensori | "Compatibilità encoder con drive attuale V32" |
| **LEX** | Brevetti, GDPR, contratti | "Come brevettare il processo MIMS polimeri?" |
| **SIEMENS** | Automazione industriale, S7, HMI | "Struttura programma S7 per asse X V32" |
| **AQUA** | Fluidodinamica, materiali | "Coefficiente espansione polimero a 180°C" |
| **ARIA** | Scheduling, ADHD scaffolding, vita | "Ottimizza il calendario della prossima settimana" |
| **EVA** | WhatsApp, prenotazioni, Vita Natura | "Risposta automatica appuntamento estetica" |

La logica: EVA non sa di codice. THEMIS non sa di prenotazioni estetiche. Ogni agente è affilato nel suo dominio. NEXUS li orchestra quando serve collaborazione.

---

## Chi sono — oltre il CV standard

Il CV tradizionale mostra titoli e datori di lavoro. Non mostra come pensa chi lo ha scritto.

**Competenze tecniche verificate:**

`TIG/MIG titanio` · `CNC 3 assi` · `Saldatura strutturale` · `PLC Siemens S7` · `HMI TP900` · `Robot industriali ESSEGI` · `QC metrologico` · `Python 3.11` · `React 19 + TypeScript` · `Claude API + MCP` · `RAG ChromaDB` · `n8n` · `Flask`

**Competenze personali — le non sostituibili:**

| Tratto | Come si manifesta in pratica |
|--------|------------------------------|
| **Pensiero sistemico** | Non risolvo un problema isolato. Costruisco il sistema che lo elimina per sempre e produce valore collaterale. |
| **Pattern matching rapido** | L'ADHD non è un limite — è un processore parallelo. Connetto segnali che altri non vedono ancora, spesso prima che diventino ovvi. |
| **Engineering hands-on** | Se non posso toccarlo, misurarlo, o vederlo in produzione, non lo considero risolto. |
| **Autonomia radicale** | Non aspetto permessi o validazione. Prototipo, testo, misuro, aggiusto. Il feedback loop è la bussola. |
| **Resilienza da industria** | 15 anni di industria pesante insegnano che i problemi si affrontano, non si gestiscono. La soluzione è sempre concreta. |
| **Documentazione compulsiva** | Ogni decisione tecnica diventa un documento in MENTE/. Ogni documento vale per tutte le sessioni future. Interesse composto sul sapere. |
| **Leva cognitiva** | Un milestone → episodio + reel + LinkedIn + dataset LLM. Il moltiplicatore è il sistema, non l'impegno. |

> *Il CV parla delle aziende per cui ho lavorato.*
> *Il sistema che ho costruito parla di come penso.*

La **MatteoSection** nella Dashboard TITANIUM_OS è un CV interattivo immersivo: skill tree navigabile, timeline narrativa, principi operativi, obiettivi a vista. Non si scarica — si esplora.

---

## I numeri

| Cosa | Valore |
|------|--------|
| V32 — investimento totale | EUR 2.250 |
| V32 — precisione RSS | ±0.019 mm (IT6-IT7) |
| V32 — BEP | 61 ore lavorate = 1.4 mesi @ EUR 45/h |
| V32 — ROI anno 1 | 322% |
| MIMS competitor principale | Alluminio estruso standard (Item, Bosch Rexroth, MayTec) |
| MIMS vantaggio | Polimero composito + connettore brevettato + produzione locale |
| Episodi podcast generati | 36+ (in automatico dai commit) |
| Documenti in RAG | 800+ |
| Automazioni attive | 34+ |
| Agenti AI operativi | 8 |
| Task notturni automatici | 5 |
| Anni di industria | 15+ |
| Target capannone | 15 Luglio 2030 |

---

## Stack

```
Fisico        TIG/MIG titanio · Alu 7075 CNC · Siemens S7+TP900 · Pressa VEVOR 20t
AI            Claude Sonnet 4.6 (orchestrazione) · Haiku 4.5 (content gen)
              OmniParser + YOLO (ARGUS v2) · CrossEncoder/ms-marco (RAG rerank)
Backend       Python 3.11 · Flask · ChromaDB · SentenceTransformer · MCP Anthropic
Frontend      React 19 · TypeScript · Vite · Tailwind v4 · Three.js · Zustand
Automation    n8n (locale) · Task Scheduler Windows · Git hooks
Integraz.     Gmail MCP · Google Calendar MCP · IFTTT
Infra         GitHub · Windows 10 Pro Getac · self-hosted
```

---

## Filosofia operativa

> *Un sistema che gira da solo vale più di 10 abitudini che dipendono dalla volontà.*

**Identifica → Automatizza → Scala.**
Se lo fai 3 volte: script. Se lo fai ogni giorno: nodo nel sistema. Se il nodo produce valore: si scala.

**1 input → N output.**
Un commit → episodio + dataset + STATE aggiornato + changelog. Ogni azione deve produrre più artefatti. Il moltiplicatore è il design del sistema.

**Cattura tutto, filtra dopo.**
Ogni decisione tecnica in MENTE/. Il RAG la rende ricercabile per sempre. Non fidarsi della memoria biologica.

**Libertà sopra profitto.**
Il capannone entro 2030 non è un obiettivo lavorativo. È un obiettivo di sovranità. Tutto il resto serve a quello.

---

[![TITANIUM_OS](https://img.shields.io/badge/TITANIUM__OS-v7.0-10b981?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![V32](https://img.shields.io/badge/V32_CNC-65%25-f59e0b?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![Episodi](https://img.shields.io/badge/Podcast-36+_episodi-a855f7?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![Agenti](https://img.shields.io/badge/Agenti_AI-8_attivi-6366f1?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![RAG](https://img.shields.io/badge/RAG-v4.0_ibrido-0ea5e9?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![ARGUS](https://img.shields.io/badge/ARGUS-v2.0_computer_use-ef4444?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
[![Target](https://img.shields.io/badge/Capannone-2030-64748b?style=flat-square)](https://github.com/Microindustry/TITANIUM_OS)
