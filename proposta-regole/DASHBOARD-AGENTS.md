# AGENTS.md — DASHBOARD

> Va salvato come `DASHBOARD/AGENTS.md`.
> Vale **solo dentro `DASHBOARD/`**. Per tutto il resto — le 12 regole, i fatti,
> le regole codice — vince `/AGENTS.md` alla radice, che questo file **non ripete
> e non contraddice**.
>
> Sostituisce `DASHBOARD/.cursorrules`. Vedi `MIGRAZIONE.md` §3 per il motivo:
> quel file conteneva numeri non verificati presentati come "THE TRUTH".

---

## STACK

- Framework: React + Vite (TypeScript)
- Styling: Tailwind CSS, mobile first
- Icone: Lucide React
- Tono: industriale, minimalista, ad alto contrasto

## STANDARD DI CODICE

1. **Iper-componentizzazione.** Nessun file enorme. Oltre le 100 righe, proponi
   di spezzare il componente.
2. **Type safety.** Interfacce TypeScript per le props. Mai `any`.
3. **Componenti funzionali.**
4. **Peso visivo.** Il design deve sembrare costruito, non disegnato: fondi
   `zinc-950`, bordi `zinc-800`.

## PALETTE E ICONE

Non decidere a gusto: la palette e la lingua delle icone sono già state fissate
contando l'uso reale su 68 file nella sessione #70. La fonte è
`BRAIN/REGOLE_GRAFICHE.md` — leggila prima di introdurre un colore nuovo.

In sintesi: base `slate`, accenti `emerald / cyan / amber / indigo / rose` + `red`.
Ritirati: `zinc` come accento, `green`, `sky`, `yellow`, `violet`, `pink`.
Le icone `lucide` sono la lingua dell'**interfaccia**; le emoji stanno solo nel
**contenuto**. Applicazione additiva: non ridipingere ciò che già funziona.

## DATI — da dove vengono

La dashboard non inventa numeri e non li scrive in chiaro nel codice. Legge:

| Vista | Fonte |
|-------|-------|
| Stato sistema | `BRAIN/STATE.json` |
| Bussola (da fare / fatto) | `GET /api/bussola/todos`, rigenerato dal night_audit |
| Critiche | `CRITICHE.md` |
| Regole servite in UI | `BRAIN/RULES.md` (derivato) |

**Se un dato non arriva da una di queste fonti, non va mostrato come dato.**
Uno stato vuoto onesto vale più di un numero segnaposto: un numero finto in una
dashboard diventa vero il giorno dopo, quando qualcuno lo cita.

## COMPORTAMENTO

- Conciso. Il codice, non la lezione.
- "Fix" significa la soluzione robusta e duratura, non la pezza.
- Verifica che le icone `lucide-react` siano importate correttamente prima di chiudere.
- Vale la regola 11: **il sistema propone, l'umano approva.**
