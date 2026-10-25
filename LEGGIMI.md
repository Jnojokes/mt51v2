# Anteprima del sito di Mauro Testatonda

Questa cartella è il sito pronto per Vercel: una pagina statica (HTML, immagini, nessuna build).
È un'**anteprima riservata**: Google non la indicizza (`robots.txt`, meta `noindex` e header
`X-Robots-Tag`). Chi ha il link la vede.

## Metterla online (GitHub → Vercel)

1. **GitHub**: in alto a destra **+ → New repository**. Nome consigliato `maurotestatonda-anteprima`,
   visibilità **Private**, senza README. Crea.
2. Nella pagina del repository vuoto clicca **uploading an existing file**, trascina **tutto il
   contenuto** di questa cartella (non la cartella stessa: `index.html` deve stare alla radice),
   poi **Commit changes**.
3. **Vercel** (vercel.com, accesso con GitHub): **Add New… → Project**, scegli il repository
   (se non compare: **Adjust GitHub App Permissions** e autorizza quel repository).
4. Impostazioni: **Framework Preset: Other**, Build Command vuoto, Output Directory vuoto
   (la radice). **Deploy**.
5. Dopo un minuto hai l'indirizzo `https://<nome-progetto>.vercel.app`.

Da qui in poi ogni file caricato o modificato su GitHub ripubblica il sito da solo.

## Dopo il primo deploy

- **Anteprima sui social e su WhatsApp**: l'immagine `og.jpg` funziona meglio con l'indirizzo
  completo. Mandami l'URL di Vercel e rigenero `index.html` con il link assoluto.
- **Dominio** (es. maurotestatonda.it): Vercel → Project → Settings → Domains.

## Prima di aprirlo a tutti

- Consenso scritto di Mauro per le immagini AI che lo ritraggono.
- Privacy policy pubblicata (nel footer c'è ancora «in arrivo»).
- Invio del modulo: oggi prepara il messaggio e lo fa partire dall'email o da WhatsApp di chi scrive.
  Il sito non salva nessun dato. Per un invio diretto serve un servizio esterno (lo configuriamo insieme).
- Per renderlo indicizzabile: togliere `<meta name="robots" ...>` da `index.html`, cambiare
  `robots.txt` in `Allow: /`, togliere l'header `X-Robots-Tag` da `vercel.json`, aggiungere sitemap.

## Cosa c'è dentro

| File | A cosa serve |
|---|---|
| `index.html` | la pagina (GSAP e Lenis caricati da CDN) |
| `img/` | le immagini WebP |
| `mauro-testatonda.vcf` | il biglietto da visita del tasto «Salva il contatto» |
| `og.jpg`, `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | anteprima social e icone |
| `404.html` | la pagina «Il palco è vuoto» |
| `vercel.json`, `robots.txt` | header (noindex, cache, vCard) e blocco motori di ricerca |
