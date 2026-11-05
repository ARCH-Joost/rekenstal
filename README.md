# Rekenstal 🐎

Een rustige rekenoefenapp met een paardenthema: elke goede som is een sprong
over een hek.

**Live:** https://arch-joost.github.io/rekenstal/

## Wat er in zit

- Tafels (instelbaar welke), delen met de tafels
- Plus en min tot 100 en tot 1000
- Alles door elkaar
- Een ouderscherm met instellingen, rondes van de afgelopen 7 dagen en de
  lastigste sommen

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
