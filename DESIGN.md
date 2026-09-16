# Møllely designguide

Låst efter "bud 2" (godkendt september 2026). Alt nyt på siden og i markedsføring følger den her.

## Positionering
**Den store havefest. Lidt ude på landet. Tæt på.**
Vi konkurrerer ikke med godsbryllupper. Vi er den store, fede havefest. Græskar og sankt hans er de årlige events, brandet bygger på.

## Farver
| Rolle | Hex |
|---|---|
| Baggrund (creme) | `#F6F1E3` |
| Kort (lys creme) | `#FDFBF4` |
| Tekst (mørkegrøn) | `#22301B` |
| Dæmpet tekst | `#5A6350` |
| Streger/kanter | `#E3DCC8` |
| Accent (græskar-orange) | `#C95B1F` |
| Mørkegrønt kort | `#24391F` |
| Lys grøn tekst på mørk | `#C9D3BD` |

Orange er ENESTE accentfarve: knapper, labels, punchlines, understregninger. Mørkegrønne kort bruges som variation (max ét pr. side).

## Typografi
- **Karla 800** til alle overskrifter, letter-spacing -0.02em. Store størrelser, korte linjer.
- **Karla 400/700** til brødtekst.
- **Young Serif** kun til Møllely-ordmærket i topbaren.

## Tone
- Korte sætninger. Punchlines frem for forklaringer: "Jeres fest. Vores plæne."
- Selvironisk og jordnær, aldrig fin.
- ALDRIG tankestreger (– eller —). Brug punktum, komma eller kolon.
- Priser siges direkte: "300 kr. pr. nat."

## Komponenter
- Sticky lys topbar med orange "Book"-knap.
- Kort: 20px hjørner, billede øverst (16:9, wide-kort 21:8), derunder ORANGE LABEL, fed overskrift, én til to linjers tekst, evt. link med orange understregning.
- Korte sider: hero + kort + kontaktstribe. Aldrig lange rul.

## Billeder
- Ægte fotos fra gården, varmt lys, ingen opstilling. Skudt på telefon er fint.
- Altid: EXIF/GPS-data fjernes, og billeder komprimeres (max 1400px, jpeg ~72) før de lægges på siden.
- Ønskeliste: havefest i aftensol (hero), shelteret, teltene indefra dækket op.

## Sider
`index.html` (kort forside), `havefesten.html`, `graeskar.html`, `shelter.html` (med bookingkalender).
Shelterkalenderens optagne datoer ligger i `shelter.html` i blokken `<script type="application/json" id="shelter-state">`, format `"2026-10-17"`.
