# Michela & Filippo — Sito del matrimonio

Sito Jekyll autonomo basato sul tema Alembic. Non richiede il tema come gem né
plugin personalizzati, quindi si compila sia in locale sia su GitHub Pages così com'è.

URL finale (una volta pubblicato): https://filippo-santoliquido.github.io/wedding/

## Cosa modificare
- **Contenuti**: tutto il sito è una pagina sola, `index.md`. Ogni sezione è un
  titolo `## Titolo {#ancora}` seguito dal testo in Markdown. Sostituisci tutto ciò
  che è tra « virgolette ». La riga `feature_image:` in cima al file è la foto grande
  di apertura; le fasce fotografiche tra una sezione e l'altra si impostano con
  `{% include band.html image="/assets/images/NOME.jpg" %}`.
- **Menu / titolo / URL**: `_config.yml` (il blocco in alto).
- **Colore d'accento**: `assets/styles.scss` → `$accentColour: #306090;` (cambia il codice colore).
- **Foto di intestazione**: metti le tue immagini in `assets/images/` e punta lì `feature_image:`.
- **RSVP**: `rsvp.md` rimanda a un Modulo Google — sostituisci `YOUR-FORM-ID` con il link del tuo modulo.

## Anteprima in locale
```bash
bundle install
bundle exec jekyll serve
# apri http://localhost:4000/wedding/
```

## Pubblicazione (GitHub Pages, sito di progetto)
1. Crea un NUOVO repository sul tuo account chiamato `wedding` (tienilo separato dal
   repository del tuo sito accademico `filippo-santoliquido.github.io`).
2. Carica questa cartella nel repository (vedi i comandi git).
3. Repository → **Settings → Pages** → *Build and deployment* → Source: **Deploy from a
   branch** → Branch: **main** / **/(root)** → Save.
4. Attendi circa 1 minuto: il sito comparirà su https://filippo-santoliquido.github.io/wedding/

Se in futuro passi a un dominio personalizzato, imposta `baseurl: ""` in `_config.yml`.
