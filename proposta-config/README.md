# settings.json — permessi per le scritture

Scritto il 27/08/2026. **Valido** (`jq` OK), **non attivo** nella sessione mobile.

## Perché non si è attivato

Il watcher della configurazione di Claude Code sorveglia solo le cartelle che
avevano già un file di settings **all'avvio della sessione**. In questo container
`~/.claude/settings.json` non esisteva: il file è stato creato correttamente ma
non viene riletto finché la configurazione non si ricarica.

Ricaricarla richiede un'azione da interfaccia — `/permissions`, oppure riavviare
la sessione — e non è una cosa che posso fare io.

## Dove va

```
~/.claude/settings.json          → PC:      C:\Users\teo\.claude\settings.json
```

È una configurazione **utente**, non di progetto: vale per tutte le sessioni,
non solo per questo repo. Per questo non l'ho messa in `.claude/` del profilo
pubblico, dove non c'entra niente.

## Cosa fa

**Sblocca** (`permissions.allow`) gli strumenti Gmail e claude-code-remote, così
etichettare, archiviare e creare routine non chiede approvazione ogni volta.

**Blocca** (`permissions.deny`, che ha precedenza sull'allow) le operazioni che
non devono mai partire da sole:

```
trash_message · trash_thread · delete_label
mark_message_spam · mark_thread_spam
send_message · reply · forward
```

Cioè: posso **organizzare** la posta, non posso **cancellarla** né **scrivere a
qualcuno al posto tuo**. È la regola 11 messa nella configurazione invece che
solo nelle intenzioni — se un giorno sbaglio, il file mi ferma.

**`autoMode.allow`** aggiunge tre regole al classificatore di sicurezza della
modalità auto, mantenendo i default (`$defaults`): etichette e archiviazione
sulla tua casella, aggancio in scrittura dei tuoi repo quando lo chiedi, e
gestione delle tue routine. È quello che serve per sbloccare l'accesso in
scrittura a TITANIUM_OS, che l'allowlist da sola non supera.

## Come attivarlo

**Sul PC:** copia il file in `C:\Users\teo\.claude\settings.json` e riavvia
Claude Code. Da lì in poi vale ovunque, anche nelle sessioni cloud che parti tu.

**Qui:** apri `/permissions` una volta — ricarica la configurazione — oppure
avvia una sessione nuova. Il file è già scritto nel container, ma il container
è effimero: se la sessione scade, sparisce. Questa copia nel repo è la versione
che sopravvive.
