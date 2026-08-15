# Blinqx Verzekering & Hypotheek — Brochures 2026

Statische HTML-brochures, klaar voor GitHub Pages.

## Inhoud

| Bestand | Brochure | Pagina's |
| --- | --- | --- |
| `index.html` | Tabbladen-overzicht met printknop | — |
| `productoverzicht.html` | Productoverzicht | |
| `eblinqx-hypotheek.html` | eBlinqx Hypotheek | |
| `eblinqx-verzekering.html` | eBlinqx Verzekering | |
| `eblinqx-volmacht.html` | eBlinqx Volmacht | |
| `eblinqx-connect-crm.html` | eBlinqx Connect CRM | |
| `eblinqx-beurs.html` | eBlinqx Beurs | |
| `eblinqx-makelaardij.html` | eBlinqx Makelaardij | |

## Gebruik

Open `index.html` — elke brochure zit in een eigen tabblad, met een knop om die
brochure te printen of los te openen. De losse bestanden zijn ook direct te openen.

## Publiceren op GitHub Pages

1. Zet de inhoud van deze map in een repository (of in `/docs`).
2. Settings → Pages → Source: de branch en map kiezen.
3. De brochures staan op `https://<gebruiker>.github.io/<repo>/`.

## Printen naar PDF

Elke brochure is opgemaakt op A4. Print met marges op "geen" en achtergronden aan;
elke pagina komt op één vel.

## Afhankelijkheden

Geen build, geen npm. `ds-styles.css` (typografie en kleurtokens) en
`doc-page.js` (paginaopmaak en print) staan naast de HTML-bestanden,
beeldmateriaal in `assets/`.
