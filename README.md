# Blinqx Verzekering & Hypotheek — Brochures 2026

Statische HTML-brochures, klaar voor GitHub Pages. In deze versie zijn de wijzigingen
uit `Blinqx-VH-wijzigingen-was-wordt-v2.xlsx` doorgevoerd (zie `WIJZIGINGEN.md`).

## Inhoud

| Bestand | Brochure | Pagina's |
| --- | --- | --- |
| `index.html` | Overzichtspagina: gegroepeerde lijst, zoeken, print/PDF, deeplinks | — |
| `productoverzicht.html` | Productoverzicht | 38 |
| `eblinqx-vh-compleet.html` | eBlinqx V&H Compleet | 12 |
| `eblinqx-hypotheek.html` | eBlinqx Hypotheek | 11 |
| `eblinqx-hypotheek-advies.html` | eBlinqx Hypotheek Advies (product) | 13 |
| `eblinqx-advies-bemiddeling-start.html` | eBlinqx Hypotheek Advies & Bemiddeling Start | 12 |
| `eblinqx-verzekering.html` | eBlinqx Verzekering Provinciaal | 11 |
| `eblinqx-volmacht.html` | eBlinqx Verzekering Volmacht | 11 |
| `eblinqx-beurs.html` | eBlinqx Verzekering Beurs | 11 |
| `eblinqx-connect-crm.html` | eBlinqx CRM | 11 |
| `eblinqx-makelaardij.html` | eBlinqx Makelaardij | 13 |
| `vcn-partner.html` | VCN Partner (met VCN Hypotheken) | 13 |
| `blinqx-banking-insurance-partners.html` | Blinqx Banking, Insurance & Partners | 13 |
| `eblinqx-schadeverzekeringen.html` | Schadeverzekeringen verkopen (thema) | 6 |
| `mijnhuiszaken.html` | MijnHuiszaken (partnerformule) | 6 |

> **Naamgeving.** Deze set volgt het lagenmodel nog niet volledig. eBlinqx Hypotheek Advies
> is een product binnen de proposities eBlinqx Hypotheek en eBlinqx V&H Compleet, eBlinqx Connect
> is de applicatie (voorheen Faster Forward Elements) en niet het CRM, en Volmacht en Beurs zijn
> varianten van eBlinqx Verzekering — geen zelfstandige proposities. De namen zijn in deze versie
> rechtgezet; de bestandsstructuur is behouden en aangevuld met V&H Compleet, Advies & Bemiddeling
> Start, VCN Partner en de partnerbrochure.

## Gebruik

Open `index.html`. Links staan de brochures gegroepeerd (Overzicht, Hypotheek, Verzekering,
Compleet & CRM, Partners), met zoekveld en paginatelling. Bovenaan de viewer: vorige/volgende,
**Link** (kopieert een deeplink), **Los openen** en **Print / PDF**.

- **Deeplinks:** elke brochure heeft een eigen adres, bijv. `…/blinqx-brochures/#vcn-partner`.
  De terugknop van de browser werkt tussen brochures.
- **Printen** opent de brochure in een nieuw venster en start daar het printvenster. Dat werkt
  ook als de overzichtspagina in een iframe staat (bijv. Google Sites). Sta pop-ups toe.
- **Sneltoetsen:** `/` zoeken, `[` en `]` vorige/volgende, pijltjes in de lijst.
- Op mobiel zit de lijst achter de knop **Brochures**. Brochures schalen op smalle schermen
  automatisch mee (alleen op scherm; printen blijft A4 op ware grootte).

Nieuwe brochure toevoegen: bestand in de root zetten en één regel toevoegen aan `GROUPS`
bovenin het script van `index.html` (bestandsnaam zonder `.html`, soort, titel, pagina's).

De losse bestanden zijn ook direct te openen.

## Publiceren op GitHub Pages

1. Nieuwe repository aanmaken en de inhoud van deze map in de root zetten (of in `/docs`):
   ```bash
   git init
   git add .
   git commit -m "Blinqx V&H brochures 2026"
   git branch -M main
   git remote add origin https://github.com/<gebruiker>/<repo>.git
   git push -u origin main
   ```
2. Settings → Pages → Source: branch `main`, map `/` (of `/docs`).
3. De brochures staan op `https://<gebruiker>.github.io/<repo>/`. Het bestand `.nojekyll` staat
   er al in, zodat Jekyll de bestanden niet verwerkt.

## Insluiten in Google Sites

1. Google Sites → **Invoegen → Insluiten → tabblad *Code insluiten***.
2. Plak:
   ```html
   <iframe src="https://jeroen-o.github.io/blinqx-brochures/" style="width:100%;height:900px;border:0" allow="clipboard-write"></iframe>
   ```
   Eén brochure direct tonen: zet `#bestandsnaam` achter de URL, bijv. `…/blinqx-brochures/#vcn-partner`.
3. Klik **Volgende → Invoegen** en sleep het insluitblok op de pagina zo groot mogelijk
   (volle breedte, flinke hoogte). Brochures schalen automatisch mee met de breedte van het blok.
4. Publiceer de site opnieuw.

Plak niet de inhoud van `index.html` zelf in Google Sites: die verwijst naar bestanden die
alleen op GitHub Pages staan en werkt daar dus niet. Printen opent een nieuw venster (pop-ups
toestaan). Ingevulde “Namens”-gegevens worden in een ingesloten pagina mogelijk niet onthouden.

## Printen naar PDF

Elke brochure is opgemaakt op A4. Print met marges op "geen" en achtergronden aan;
elke pagina komt op één vel.

## Afhankelijkheden

Geen build, geen npm. Alle afbeeldingen zitten in de HTML-bestanden zelf, dus
er kan geen beeld ontbreken door een verkeerd pad. Naast de brochures staan
alleen `ds-styles.css` (typografie en kleurtokens) en `doc-page.js`
(paginaopmaak en print) — die twee moeten mee in de repository. De map
`assets/` is optioneel en alleen voor hergebruik van het beeldmateriaal.

## Namens Blinqx V & H invullen

Onderaan elke brochure staat een balk **Namens Blinqx V & H**. De velden staan
voorgevuld met de gegevens van Jeroen Oversteegen. Vul naam, functie,
e-mailadres, mobiel, vast nummer en adres in en klik Opslaan: de gegevens verschijnen op de
achterkant van *alle* brochures (ze worden in de browser bewaard). "Standaard"
zet Jeroen Oversteegen terug. De balk print niet mee en verdwijnt met "Verberg".

De ingevulde gegevens staan in localStorage op het eigen apparaat. Op een gedeeld
apparaat ziet de volgende gebruiker dus de gegevens van de vorige. Vul hier
uitsluitend gegevens van eigen medewerkers in — geen klant- of eindgebruikergegevens.

## Nog te verifiëren

Deze punten uit de Excel zijn bewust **niet** in de brochures verwerkt en vragen een besluit:

- **Structuur.** Zeven productbrochures worden in het lagenmodel vier propositiebrochures
  (eBlinqx Hypotheek · Verzekering · V&H Compleet · CRM). Die herstructurering is niet uitgevoerd;
  alleen de naamgeving is rechtgezet. eBlinqx V&H Compleet heeft nu wel een eigen brochure (12 pagina's).
- **Certificering.** ISO 27001 en ISAE 3402 staan als bevestigd in de Excel en zijn daarom
  blijven staan. Niet publiceren zonder schriftelijke bevestiging van compliance.
- **Tijdlijn.** De jaartallen van MyTP, Adviesbox/Finly en de platformlancering wijken af van de
  website. De jaartallen zijn ongemoeid gelaten; de kop luidt nu "tot en met 2024", zodat er geen
  gat na 2024 wordt gesuggereerd. 2025 en 2026 aanvullen zodra de mijlpalen bekend zijn.
- **Cijfers zonder bron** zijn afgezwakt naar niet-numerieke formuleringen (retentie, woningzoekers,
  publicatiekanalen, besparingsbedrag, tijdwinst). Met bron en peildatum kunnen ze terug.
- **Gebruikersaantal.** 100.000+ is vervangen door 600+ collega's en 10+ vestigingen. Het
  gebruikersaantal per afbakening moet nog worden vastgesteld.
- **Openstaand ter bevestiging:** definitieve naam FinRust, aantal en positionering van de
  check-ups, aantal aangesloten geldverstrekkers (FinData), publicatiebereik RenteAdministratie.nl,
  toestemming voor naamsvermelding bij klantcitaten, positie van Makelaardij en eBlinqx Fiscaal,
  en de standaard contactpersoon op de achterkant.
