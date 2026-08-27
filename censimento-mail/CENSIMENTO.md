# Censimento — benenatimatteo.mb@gmail.com

Rilevato il 27/08/2026. **Sola lettura: nulla è stato modificato, spostato,
etichettato o cancellato.**

---

## Metodo, e i suoi limiti

L'API di Gmail **non dà i totali per mittente**: il campo `resultCountEstimate`
torna sempre `201`, è un tappo fisso. Quindi i conteggi esatti per indirizzo non
sono ottenibili da qui.

Quello che è ottenibile, ed è sufficiente per scrivere i filtri:

- **Totali esatti per etichetta**, dall'API delle label.
- **Distribuzione dei mittenti**, da 200 thread campionati su quattro finestre
  temporali che coprono da maggio 2025 a oggi.

Il campione prende i 50 thread più recenti di ciascuna finestra: è denso al bordo
della finestra, non uniforme su tutto il periodo. Va letto come *"chi scrive in
quel periodo"*, non come *"quanti in totale"*.

---

## 1. I totali esatti

| | |
|---|---|
| Thread in inbox | **27.257** |
| Non letti | **25.921** (95,1%) |
| Non letti in tutto l'account | 27.100 |
| Thread inviati, da sempre | 710 |
| Bozze mai partite | **60** |
| Stellate | 53 |

**Etichette.** Otto su tredici sono a zero messaggi — create e mai usate:
`Notes`, `instagram`, `google`, `ikeA`, `pubblicità`, `likenid`, `opel adam`,
`Bollette` (2 messaggi). Quelle popolate sono quasi interamente non lette:

| Etichetta | Messaggi | Non letti |
|---|---|---|
| ricerca lavoro | 639 | 632 |
| hype | 318 | 314 |
| amason | 137 | **137 (100%)** |
| ila | 19 | 0 |

Etichettare senza decidere non alleggerisce: il messaggio resta lì, solo colorato.

---

## 2. Il flusso è crollato — e questo cambia la strategia

Densità stimata al bordo di ciascuna finestra:

| Periodo | Thread/giorno |
|---|---|
| maggio 2025 | **~16,7** |
| dicembre 2025 | ~5,6 |
| maggio 2026 | ~12,5 *(gonfiato, vedi §4)* |
| agosto 2026 | **~4,5** |

**Il tuo problema non è il flusso in ingresso.** Oggi arrivano 4-5 thread al
giorno: niente. I 27.000 sono **stock storico**, accumulato quando ne arrivavano
tre volte tanti.

Conseguenza operativa: i filtri da soli non risolvono nulla di percepibile.
Servono per non ricostruire il problema, ma il peso che senti oggi è quello
vecchio, e si toglie con un'archiviazione di massa, non con una regola.

---

## 3. Le famiglie di rumore

Ricorrono in **tutte e quattro** le finestre — sono la spina dorsale dei 27.000:

**Commercio e promozioni**
`aliexpress.com` (5 indirizzi diversi: `ae-ai-interest01`, `aeug-new-item-alert14`,
`aeug-interest28`, `ae-best-care-market00`, `promotion`) · `ryanairemail.it` ·
`n.myprotein.com` · `email.subito.it` · `reply.ebay.it` · `zumub.com` ·
`instant-gaming.com` · `giardineria.com` · `kasanova.com` · `photosi.com` ·
`vivaticket.com` · `tisvapo.it` · `sony-europe.com` · `emails.tomtom.com` ·
`gopro.com` · `samsung.com` · `playstation.com` · `mcdonalds.it`

**Social e raccomandazioni**
`pinterest.com` (4 sottodomini) · `service.tiktok.com` · `mail.instagram.com` ·
`facebookmail.com` · `em.linkedin.com` + `newsletters-noreply@linkedin.com` ·
`nextdoor.com` · `crunchyroll.com` · `mydramawave.com`

**Strumenti e servizi**
`ifttt.com` · `n8n.io` · `ngrok.com` · `ollama.com` · `thinkific.com` ·
`descript.com` · `airtable.com` · `notion.so` · `tradingview.com` ·
`shapr3d.com` · `printables.com` · `freeletics.com`

**Lavoro (annunci automatici)**
`jobalerts-noreply@linkedin.com` · `randstad.it` · `adecco.com` · `orienta.net`

---

## 4. Il rumore che ti sei generato da solo

Nella finestra di maggio 2026, **15 thread su 50 — il 30%** — sono
`notifications@github.com` indirizzati a `TITANIUM_OS@noreply.github.com`:
notifiche di CI del tuo stesso repo.

È il motivo per cui quella finestra sembra tre volte più densa delle altre.
Non è posta: è il tuo sistema che si scrive addosso. Si spegne dalle impostazioni
di notifica di GitHub, non con un filtro Gmail — e vale la pena farlo prima,
perché un filtro le nasconderebbe lasciandole contare.

---

## 5. Le uniche mail scritte da persone

Su 200 thread campionati, le mail da un essere umano che si rivolge a te sono
**quattro**, tutte nella finestra di maggio-giugno 2026:

- `Simona.DiLiberti@gigroup.com` — thread di **5 messaggi**, con **due tue
  risposte** e allegati. L'unico scambio vero e completo del campione.
- `c.cernuto@gruppodifazio.it`
- `abbiategrasso.technical@randstad.it` (in bcc)
- `benenatimatteo1995@gmail.com` — **tu stesso**, da un altro account, tre thread
  con allegati pesanti (11,7 MB · 4,6 MB · 447 KB). Trasferimento file, non posta.

Nelle finestre 2025: **zero**.

La corrispondenza umana di questa casella è, di fatto, **lavoro**. Ed è la
categoria che un'archiviazione di massa rischia di seppellire per prima —
va protetta esplicitamente, non per esclusione.

---

## 6. Le mail che contano e che stanno annegando

Dal campione, ciò che va assolutamente estratto prima di qualunque pulizia:

| Mittente | Cosa | Nel campione |
|---|---|---|
| `noreply@a2aenergia.it` · `smile@a2aenergia.it` | bollette luce/gas | ago 2026, mag 2026, dic 2025 |
| `noreply@gruppocap.it` | utenze acqua (allegato 1,2 MB) | dic 2025 |
| `account-security-noreply@accountprotection.microsoft.com` | sicurezza account | ago 2026, marcata IMPORTANT |
| `invoice+statements@mail.anthropic.com` | fatture | mag 2026 |
| `failed-payments@mail.anthropic.com` | **pagamento fallito** | mag 2026, IMPORTANT, 3 messaggi |
| `info.it@ing.com` | banca | mag 2026 |
| `noreply@github.com` | sicurezza/account (non le CI) | ago 2026 |

Il caso `failed-payments` è la misura esatta del costo del rumore: un pagamento
fallito, marcato importante, tre solleciti nello stesso thread, in una casella
dove non guardi. Non è un'ipotesi di danno — è successo.

---

## 7. Proposta operativa

Non applicata. Da decidere insieme.

### Fase 0 — spegnere la sorgente propria
Notifiche CI di GitHub: disattivarle su GitHub. Toglie ~30% del flusso nei
periodi di lavoro intenso e non nasconde niente.

### Fase 1 — proteggere prima di filtrare
Creare l'etichetta `TIENE` e applicarla, **prima di ogni altra cosa**, a:
utenze (a2aenergia, gruppocap), banca (ing), sicurezza account (Microsoft,
Google, GitHub), fatture e pagamenti (Anthropic), e a ogni thread che contiene
un tuo messaggio inviato — quest'ultimo criterio da solo salva tutte le
conversazioni vere, perché una conversazione vera è una a cui hai risposto.

### Fase 2 — fermare l'emorragia
Filtri Gmail sulle famiglie del §3: saltano l'inbox, vanno in un'etichetta
`RUMORE`, restano cercabili. Non cancellare: archiviare. Con 4-5 thread al
giorno il guadagno percepito è modesto, ma impedisce di ricostruire lo stock.

### Fase 3 — lo stock
27.000 thread non si leggono, mai. Archiviazione di massa per data — tutto
ciò che è più vecchio di X e non ha `TIENE` esce dall'inbox e resta
nell'archivio. Reversibile, cercabile, niente va perso.

### Fase 4 — le 60 bozze
Guardarle una per una. È l'unico posto del campione dove potrebbe esserci
qualcosa di **tuo** rimasto in sospeso.

### Fase 5 — il triage quotidiano
Solo dopo. Su 4-5 thread al giorno filtrati, un riepilogo mattutino ha senso;
su 27.000 non ne aveva.

---

## 8. Cosa non ho fatto

- Non ho aperto il **corpo** di nessuna mail. Solo mittenti, date, etichette.
- Non ho contato i totali per mittente: l'API non li espone (§Metodo).
- Non ho toccato l'etichetta `ricerca lavoro` (639 messaggi). È l'unica area
  con corrispondenza umana reale: qualunque regola su quella decidila tu.
- Non ho creato filtri, etichette, archiviazioni. Vale la regola 11.
