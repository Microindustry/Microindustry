# Automazioni iPhone — cosa hai, cosa conviene

27/08/2026. Ricognizione in sola lettura sull'account IFTTT. Niente creato.

---

## 1. Il vincolo che decide tutto

```
username     benenatimatteomb
tier         FREE  (is_paid: false)
applet_count 0
applet_limit 2          ← due. In totale.
time_zone    Europe/Rome
```

**Hai due slot IFTTT, e zero applet.** Qualunque cosa progettiamo deve starci
dentro, oppure passi a Pro. Questo cambia completamente la strategia: con due
slot non si costruisce un sistema, si spendono due colpi bene.

## 2. Cosa hai già collegato — 20 servizi

Il lato iOS è tutto connesso, ed è più ricco di quanto pensassi:

| Servizio | Cosa dà |
|---|---|
| `ios_shortcuts` | trigger *"shortcut automation started"* — Comandi Rapidi può accendere IFTTT |
| `do_button` | widget bottone in schermata home |
| `do_note` | widget nota rapida |
| `do_camera` | foto + **scansione QR** (anche QR specifico o con regex) |
| `location` | entra/esce da un'area — geofence |
| `if_notifications` | notifica semplice, ricca, widget |
| `ios_reminders` | crea promemoria, e triggera su nuovo/completato |
| `ios_calendar` · `ios_photos` · `ios_health` · `ios_contacts` | il resto del pacchetto Apple |
| `email` | manda email, **e riceve**: `send_ifttt_an_email_tagged` |
| `email_digest` | digest giornaliero o settimanale |
| `date_and_time` | orari e ricorrenze, lato server |
| `weather` · `feed` (RSS) · `space` · `voip_calls` | il contorno |

**Non collegati, ma disponibili e importanti:**

- **`maker_webhooks`** — `make_web_request`, e i trigger `event` / `json_event`.
  È la colla verso qualunque cosa.
- **`github`** — e ha l'azione **`create_new_issue_for_repository`**.
  È l'anello che mancava: IFTTT può scrivere direttamente nella tua bussola.

Vanno collegati da te con un OAuth: un minuto a testa, ma non posso farlo io.

---

## 3. La cosa controintuitiva: ti serve poco IFTTT

**Comandi Rapidi di Apple fa quasi tutto quello che vuoi, gratis e senza limiti.**
Sa fare richieste HTTP da solo (*Ottieni contenuto di URL*), sa partire da un
tag NFC, da un orario, dall'arrivo in un posto, dall'apertura di un'app, dal
collegamento del caricabatterie.

Quindi la regola è: **Comandi Rapidi è il motore, IFTTT è l'eccezione.**
I due slot si spendono solo dove Comandi Rapidi non arriva — cioè dove serve
che una cosa giri **a telefono spento** (IFTTT gira sul suo server), o dove
serve **non tenere un token sul telefono**.

---

## 4. Slot 1 — la cattura in officina

È l'automazione che ti manca davvero. Le cose che ti vengono in mente mentre
saldi non hanno un posto dove cadere: o le ricordi, o le perdi.

```
TRIGGER   Note widget  (do_note)          ← una nota dalla schermata home
ACTION    GitHub → create_new_issue_for_repository
          repo: Microindustry/TITANIUM_OS
          title: [officina] {{NoteField}}
```

**Perché passare da IFTTT invece che da Comandi Rapidi:** l'autenticazione
GitHub resta su IFTTT. Non ti serve mettere un token con permessi di scrittura
dentro il telefono, che poi va rinnovato — e il tuo token `titanium-scanner` è
già scaduto a maggio senza che nessuno se ne accorgesse.

Ogni idea diventa una issue nel repo. La bussola la vede, il RAG la rilegge, e
al PC la trovi già lì. Questo è il ponte fra l'officina e il sistema.

## 5. Slot 2 — lascialo vuoto

Sul serio. L'unico altro candidato ovvio è il geofence dell'officina, ma
**Comandi Rapidi lo fa nativamente** con *Automazione → Quando arrivo*.
Tieni lo slot libero finché non nasce un bisogno che solo IFTTT copre: sprecarlo
adesso significa non poterlo usare quando servirà.

---

## 6. Quello che va fatto in Comandi Rapidi — gratis e illimitato

### A. Tag NFC sulla V32
Un adesivo NFC da pochi centesimi sul telaio. Avvicini il telefono e parte
l'automazione: registra l'inizio della sessione di lavoro, o apre la nota
giusta. **Automazione → NFC → Scansiona.** Zero slot IFTTT.

Vale anche per la pressa, per il magazzino, per ogni postazione. È il modo più
vicino a "misurare senza doverci pensare" — regola 6.

### B. Cattura a voce, mani sporche
*"Ehi Siri, nota officina"* → il comando detta, e manda il testo dove vuoi:
via email all'indirizzo trigger di IFTTT, oppure direttamente in una nota.
Non tocchi lo schermo, che con le mani unte è il punto.

### C. Arrivo e uscita
**Automazione → Quando arrivo a [officina]**: avvia un timer, apre la bussola,
o ti ricorda le due azioni non delegabili di `AZIONI_MATTEO.md`.

### D. Pulsante Azione / widget
Se hai un iPhone con il pulsante Azione, assegnalo alla cattura. È il gesto più
corto che esista fra un'idea e un posto dove tenerla.

---

## 7. Dove sta il confine, detto chiaro

| Cosa | Chi lo fa |
|---|---|
| Gesti sul telefono (NFC, Siri, arrivo, pulsante) | **Comandi Rapidi** |
| Scrivere su GitHub senza token sul telefono | **IFTTT** (slot 1) |
| Sorvegliare il sistema a PC spento, ogni mattina | **Routine Claude** — non IFTTT |
| Toccare la CNC o il PC di casa | **niente di tutto questo** |

La sentinella del battito **non** è un lavoro da IFTTT: deve leggere GitHub,
confrontare date e ragionare su cosa dirti. È la Routine delle 07:00, che è già
scritta in `proposta-routine/brief-0700.md`.

---

## 8. Cosa non ho potuto fare

- **Creare l'applet.** `create_applet` è una scrittura, e in questa sessione le
  scritture sono bloccate — come per Gmail e per le Routine.
- **Leggere `my_applets`.** Bloccato anche quello. Ma `get_user_info` dice
  `applet_count: 0`, quindi non c'è niente da vedere.
- **Collegare GitHub e Webhooks su IFTTT.** Serve un OAuth dal tuo account.

## 9. I tuoi tre gesti, in ordine

1. Su IFTTT, collega **GitHub** (un minuto, OAuth).
2. Crea l'applet dello slot 1: `Note widget` → `Create a new issue`, repo
   `Microindustry/TITANIUM_OS`, titolo `[officina] {{NoteField}}`.
3. Su iPhone, apri Comandi Rapidi e fai il tag NFC della V32.

Il primo e il terzo si fanno dal telefono, adesso. Il secondo pure.
