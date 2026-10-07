# Repair Café Gorinchem

Website van Repair Café Gorinchem — elke 1e zaterdag van de maand, 10:00–12:00 uur, in Buurtkamer Stalkaarsen (Dr. Hiemstralaan 77, Gorinchem).

## Opbouw

Eén statische pagina: [`index.html`](index.html).

- **Styling:** Tailwind CSS via CDN, met eigen kleuren `brand` (indigo `#2D2E82`) en `amberWood` (oranje `#ED6A42`), naar de huisstijl van repaircafe.org
- **Iconen:** Font Awesome 6
- **Lettertype:** Roboto (Google Fonts)
- **JavaScript:** berekent automatisch de eerstvolgende drie bijeenkomsten (1e zaterdag van de maand), plus het mobiele menu, de zoektool "Wat kun je meenemen?", het event-schema voor Google en het versturen van de formulieren

## Lokaal bekijken

Open `index.html` in je browser. Er is geen build-stap nodig.

## Formulieren

Het vrijwilligers- en contactformulier versturen via [FormSubmit](https://formsubmit.co) (gratis, geen account) naar `repaircafegorinchem@outlook.com`. Bij de allereerste inzending stuurt FormSubmit een activatiemail naar dat adres; pas na het klikken op "Activate Form" komen inzendingen binnen. Een onzichtbaar honeypot-veld (`_honey`) houdt simpele spambots tegen.

## Toegankelijkheid

De site is getest tegen WCAG 2.2 niveau AA met [axe-core](https://github.com/dequelabs/axe-core) (desktop, mobiel met open menu, alle meldingen van zoektool en formulieren, 320px breed) plus handmatige toetsenbordtest. Aandachtspunten bij wijzigingen:

- Oranje (`amberWood-500`) knoppen altijd met donkere tekst (`text-brand-950`/`text-slate-950`); wit op oranje haalt het contrast niet.
- Decoratieve iconen krijgen `aria-hidden="true"`; koppen in volgorde (h1 → h2 → h3).
- Links die in een nieuw venster openen krijgen `<span class="sr-only"> (opent in een nieuw venster)</span>`.
