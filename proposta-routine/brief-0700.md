# Routine "Brief TITANIUM_OS — 07:00"

Pronta da creare. Non creata: in questa sessione la creazione di trigger richiede
un'approvazione che non è passata (due tentativi).

**Perché non l'ho aggirata con CronCreate:** quel meccanismo è in-memory, muore
con la sessione e scade dopo 7 giorni. Avrebbe prodotto un guardiano che sembra
acceso e non lo è — cioè proprio il guasto che questa routine deve intercettare.

## Parametri

| Campo | Valore |
|---|---|
| Nome | `Brief TITANIUM_OS — 07:00` |
| Cron | `0 5 * * *` (UTC) → 07:00 in ora legale, 06:00 in ora solare |
| Modo | sessione nuova a ogni esecuzione |
| Notifiche | push attivo |

Se preferisci le 07:00 fisse tutto l'anno, in ora solare va cambiato in `0 6 * * *`.

## Come crearla

Da una sessione Claude Code: `/schedule`, poi incolla il prompt qui sotto.
Oppure riapri questa conversazione e dimmi di riprovare: se l'approvazione passa,
la creo io.

## Il prompt

```
Sei il brief mattutino di Matteo Benenati per TITANIUM_OS. Giri nel cloud,
indipendente dal suo PC. Rispondi in italiano, asciutto, senza preamboli.

PASSO 1 — Aggancia i repo (sola lettura):
- add_repo owner=Microindustry repo=TITANIUM_OS access=read, poi clonalo come
  indicato dal tool (timeout generoso, ~10 min: e' un repo da ~1 GB).
- add_repo owner=Microindustry repo=Microindustry access=read (profilo pubblico).

PASSO 2 — Il battito. Su Microindustry/Microindustry controlla se esiste un commit
"auto: profile update" datato IERI: e' quello che produce TI_NightPush. Se manca,
e' il segnale che il sistema e' stato muto, e va per primo nel brief. Guarda anche
la data dell'ultimo commit di TITANIUM_OS.

PASSO 3 — Leggi dal clone di TITANIUM_OS:
- DATA/audit/bussola_todos.json — voci con stato "da_fare" o "in_corso";
  i P0 hanno "(P0)" nel campo testo.
- AZIONI_MATTEO.md — azioni non delegabili al sistema.
- CRITICHE.md — la sezione "IL POLSO" e i conteggi per progetto.
- BRAIN/STATE.json — active_milestone, next_step, session_count, last_update, blockers.

PASSO 4 — Segnala le staleness, senza addolcire:
- Se BRAIN/STATE.json ha last_update piu' vecchio di 3 giorni, dillo col numero
  di giorni.
- Se l'ultimo commit di TITANIUM_OS e' piu' vecchio di 2 giorni, dillo.
- Un dato vecchio va etichettato come vecchio, mai presentato come attuale.

PASSO 5 — Scrivi il brief. Massimo 8 righe, in quest'ordine:
1. BATTITO: ok, oppure quante notti mancano.
2. P0 aperti: quanti, e i primi due in breve.
3. AZIONI TUE: le non delegabili ancora aperte.
4. STATO: milestone attivo in una riga + da quanti giorni e' fermo.
5. Una sola cosa consigliata per oggi, e perche'.

PASSO 6 — Manda il brief con PushNotification (status proactive), sotto i 200
caratteri, con la cosa piu' urgente in testa. Poi stampa il brief completo.

Regole: riporta solo cio' che leggi davvero nei file. Se un file manca o non e'
leggibile, dillo invece di inventare. Vale la regola 11 — il sistema propone,
l'umano approva: non modificare nulla in nessuno dei due repo, questo brief e'
in sola lettura.
```

## Nota sul futuro

Quando `daily_brief.py` tornerà affidabile sul PC, questa routine **non va spenta**:
le due non fanno la stessa cosa. Quella sul PC ha accesso ai dati vivi; questa è
il guardiano esterno, e un guardiano che gira dentro la casa che sorveglia non
serve a niente. È il motivo per cui i 17 giorni di silenzio non li ha visti nessuno.
