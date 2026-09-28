# V32 — FLUSSO

Flusso di coscienza del progetto. **Append-only**: si aggiunge in fondo, non si riscrive sopra.
L'ultimo blocco in fondo è sempre lo stato più aggiornato.

Formato di ogni blocco:

```
## [data] — titolo
FONTE: foto | misurato | datasheet | dichiarato
...testo...
```

Regola: se una cosa non è verificata, si scrive `dichiarato` e resta un debito aperto.
Niente numeri inventati. Se non si sa, si scrive "non so".

---

## [2026-09-03] — Apertura flusso
FONTE: dichiarato

Punto di partenza reale, dichiarato da Matteo, non ancora verificato:

- V32 = fresatrice CNC 3 assi, corpo unico, acciaio saldato TIG
- Stato: telaio in piedi
- Config G = gusset + rinforzi colonne Z + U
- Componentistica: scelta, fisicamente disponibile, **mai censita**

Cosa NON si sa (buchi dichiarati aperti oggi):

| Sottosistema | Stato conoscenza |
|---|---|
| CONTROLLO / PLC | zero |
| DRIVER | zero |
| MANDRINO | zero |
| ELETTRICO / quadro | zero |
| Assi X/Y/Z — corse, guide, viti | zero |
| BOM | inesistente |

Numeri esistenti ma **non dimostrati**: BEP 61 ore, tariffa target 45 EUR/h.
Vanno ricalcolati da zero quando la BOM sarà reale.

Metodo deciso: si parte dai PEZZI fisici (foto) → si capisce come si montano →
si aggiornano gli assi → si rifanno i calcoli → poi VULCAN, MIMS, NINA.

Prossimo blocco: censimento pezzi da foto.

---
