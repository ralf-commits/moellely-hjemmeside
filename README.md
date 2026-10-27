# Møllely hjemmeside

Statisk site for Møllely ApS, Lyngevej 265, 3540 Lynge. Hostet på GitHub Pages fra main.

## Sider
- `index.html`: kort forside med kort til de tre områder
- `havefesten.html`: fest- og lokationsudlejning
- `graeskar.html`: pluk selv-græskar og fortælling
- `shelter.html`: shelterovernatning med bookingkalender

Designet er låst i `DESIGN.md`. Billeder ligger som data-URI'er direkte i HTML-filerne; de behandlede kildebilleder ligger i `billeder/` (fuld opløsning, færdig-gradede, EXIF fjernet).

## Arbejdsgang
- HTML-filerne er kilden. Ret direkte i dem og push; GitHub Pages deployer automatisk inden for et par minutter.
- Siderne deler header, CSS og footer som kopier i hver fil. Ændres noget fælles, skal det ændres i alle fire filer.
- Nyt billede på en side: skalér ned (max 1400 px, jpeg-kvalitet ~72), base64-encod og indsæt som `data:image/jpeg;base64,...` i `src`. Kildebilledet lægges i `billeder/`.
- Nye fotos fra Ralfs fotobibliotek kan kun hentes fra hans Mac (Fotos-adgang). Fra cloud: bed Ralf vedhæfte billedet i chatten i stedet.

## Booking (manuel indtil videre)
- Bookinger kommer pr. SMS/telefon til 21 60 09 84. Der er ingen backend endnu.
- Optagne shelterdatoer ligger i `shelter.html` i blokken `<script type="application/json" id="shelter-state">`, format `"2026-10-17"`.
- **Regel: stedet kan kun bruges til én ting ad gangen.** Er der booket havefest på en dato, blokeres samme dato i shelterkalenderen (og omvendt ved behov). Alle bookinger, uanset type, skal derfor ind i shelter-state.
- Planen er fuld automatisering med Supabase (fælles tilgængelighedstabel på tværs af fest og shelter, dobbeltbooking-sikring, push-besked via ntfy). Afventer Supabase-konto.
