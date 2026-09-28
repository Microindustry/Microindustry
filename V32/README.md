# V32 — Workspace progetto

Fresatrice CNC 3 assi. Corpo unico, acciaio saldato TIG. Config G.

Questo non è un archivio di documentazione. È il **flusso di lavoro attivo**:
si scrive mentre si costruisce, e ogni affermazione porta la sua fonte.

## Come si legge

| File | Cosa contiene |
|---|---|
| `FLUSSO.md` | **Inizia da qui.** Append-only: l'ultimo blocco in fondo è lo stato attuale |
| `PEZZI.md` | Censimento componenti — lettura umana |
| `bom.json` | Distinta strutturata — sorgente di verità |
| `bom.csv` | Stessa distinta per Excel |
| `foto/` | Foto originali dei componenti |

File che nasceranno quando ci sarà materia (non prima):
`ASSI.md` · `CALCOLI.md` · `ROADMAP.md`

## La regola

Ogni riga porta `fonte`:

| fonte | significato |
|---|---|
| `foto` | letto dall'etichetta del componente reale |
| `misurato` | misurato fisicamente |
| `datasheet` | da scheda tecnica produttore |
| `dichiarato` | detto a voce, **non verificato** — è un debito, non un dato |

Una macchina non si costruisce sulle intenzioni. Si costruisce sui pezzi che hai in mano.

## Sequenza di lavoro

```
PEZZI  →  ASSEMBLAGGIO  →  ASSI  →  CALCOLI  →  VULCAN / MIMS / NINA
  ↑
 qui
```
