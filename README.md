# Rekenstal 🐎

Een rustige rekenoefenapp met een paardenthema: elke goede som is een sprong
over een hek.

**Live:** https://arch-joost.github.io/rekenstal/

## Wat er in zit

- Tafels (instelbaar welke), delen met de tafels
- Plus en min tot 100 en tot 1000
- Klokkijken: een wijzerklok aflezen, tijd in woorden ("vijf over half acht")
  omzetten naar digitaal, en een 24-uurstijd (14:45) omzetten naar de
  wijzerklok. Instelbaar: hele en halve uren, kwartieren of per 5 minuten.
- Alles door elkaar (de rekenonderwerpen, zonder klokkijken)
- Een ouderscherm met instellingen, rondes van de afgelopen 7 dagen en de
  lastigste sommen

## Tip en uitleg bij een fout

Elke som krijgt één passende aanpak, zodat ze niet tussen methodes hoeft te
wisselen:

| Som | Aanpak |
|---|---|
| plus/min, getal eindigt op 8 of 9 (47 + 29) | compenseren: 47 + 30 − 1 |
| min, getallen dicht bij elkaar (83 − 78) | aanvullen: spring van 78 naar 83 |
| plus zonder tientaloverschrijding (43 + 25) | splitsen: tientallen en eenheden apart |
| overige plus/min | rijgen, via het tiental of honderdtal |
| ronde honderdtallen (300 + 400) | rekenen met honderdtallen: 3 + 4 |
| tafels | wisselen, verdubbelen, halveren (5× = helft van 10×), steunsom (7× = 5× + 2×) |
| delen | omkeren naar een keersom, met een steunsom |
| klok | wijzers aflezen, woorden naar cijfers, min 12 |

- **Na de 1e fout:** een tip met de naam van de aanpak en de eerste stap, en
  waar het kan een getallenlijn met de sprongen en een **?** op de plek van
  het antwoord.
- **Na de 2e fout:** het antwoord met de volledige uitwerking in stappen en
  de complete getallenlijn. De cijfertoetsen verdwijnen dan even, zodat
  alleen **Verder** overblijft.

In het ouderscherm kun je tip en uitleg samen uitzetten.

## Ontwerpprincipes

Deze zijn bewust gekozen (voor concentratie). Niet aan tornen zonder overleg:

- Eén som tegelijk, geen timer of tijdsdruk.
- Korte rondes (standaard 8 sommen); de voortgang is zichtbaar als hekken.
- Bij een fout eerst een tip; na de 2e poging wordt het antwoord getoond en
  komt de som later in de ronde terug.
- Na elke ronde een verplichte beweegpauze van 30 seconden; na 3 rondes op een
  dag: "genoeg voor vandaag".
- Voortgang staat in `localStorage` onder de key `rekenstal-v1`. Houd dat
  formaat compatibel, anders raakt ze haar rozetten kwijt.

## Techniek

Eén statisch bestand, `index.html`: vanilla JS, geen build en geen
afhankelijkheden (alleen het lettertype Andika van Google Fonts). Gehost via
GitHub Pages vanaf `main`, root.

Lokaal testen: open `index.html` in een browser.
