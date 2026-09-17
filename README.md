# Møllely hjemmeside

Statisk site for Møllely ApS, Lyngevej 265, 3540 Lynge. Hostet på GitHub Pages fra main.

## Sider
- `index.html`: kort forside med kort til de tre områder
- `havefesten.html`: fest- og lokationsudlejning
- `graeskar.html`: pluk selv-græskar og fortælling
- `shelter.html`: shelterovernatning med bookingkalender

Designet er låst i `DESIGN.md`. Billeder ligger som data-URI'er i filerne, originaler og gradede versioner i `~/Møllely-billeder/`.

## Booking (manuel indtil videre)
- Bookinger kommer pr. SMS/telefon til 21 60 09 84. Der er ingen backend endnu.
- Optagne shelterdatoer ligger i `shelter.html` i blokken `<script type="application/json" id="shelter-state">`, format `"2026-10-17"`.
- **Regel: stedet kan kun bruges til én ting ad gangen.** Er der booket havefest på en dato, blokeres samme dato i shelterkalenderen (og omvendt ved behov). Alle bookinger, uanset type, skal derfor ind i shelter-state.
- Planen er fuld automatisering med Supabase (fælles tilgængelighedstabel på tværs af fest og shelter, dobbeltbooking-sikring, push-besked via ntfy). Afventer Supabase-konto.
