# File modificati — riepilogo completo

Questi sono TUTTI i file cambiati rispetto allo zip che avevi caricato.
Copiali sopra il repo mantenendo la struttura delle cartelle.

## ⚠️ Un file va CANCELLATO a mano
```bash
rm assets/button.js
```
Era un residuo del tema originale: nascondeva il primo pulsante della pagina
sopra i 640px di larghezza, facendo sparire "Conferma la presenza" su desktop.

## I 6 file modificati

| File | Cosa cambia |
|---|---|
| `_config.yml` | data del countdown corretta: 2027-03-29T11:15 (Pasquetta) |
| `index.md` | mappe con coordinate esatte, punti focali delle foto, testo hero con classi, due punti focali hero |
| `_includes/band.html` | supporto al parametro `position` per il punto focale di ogni fascia |
| `_includes/site-feature.html` | passa i punti focali della hero al CSS come variabili |
| `_includes/site-before-end.html` | tolto il richiamo a button.js, resta il countdown |
| `_sass/_onepage-extra.scss` | fasce più alte, hero a proporzioni fisse, testo nero in alto |

## Come applicare
```bash
# dalla cartella del repo
rm assets/button.js
bundle exec jekyll serve      # apri http://localhost:4000/wedding/
git add -A
git commit -m "Fix foto, countdown, mappe, bottone RSVP e testo hero"
git push
```

## Le manopole da regolare

**Punto focale della hero** — in cima a `index.md`:
```yaml
feature_position: "center 55%"          # desktop
feature_position_mobile: "center 50%"   # telefono
```
Percentuale bassa = si vede la parte alta della foto; alta = la parte bassa.

**Punto focale delle fasce** — nel corpo di `index.md`:
```liquid
{% include band.html image="/assets/images/foto.jpg" position="center 40%" %}
```

**Altezza della scritta sulla hero** — in `_sass/_onepage-extra.scss`,
cerca `►► MANOPOLA`: è il valore `top` (4% telefono, 5% desktop).

## Segnaposto ancora da riempire
- link della cartella Google Drive per le foto (`index.md`, sezione Foto)
- link del modulo Google per gli RSVP (`index.md`, sezione RSVP, in 2 punti)
- scadenza per le conferme
- testo dei regali e le risposte delle FAQ
