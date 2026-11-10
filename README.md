# De Advieskamer

Een AI-adviesraad in één HTML-pagina. Je legt een twijfel of beslissing voor, de voorzitter stelt verduidelijkende vragen en vult een briefing in, kiest 7 adviseurs uit een pool van 20, laat ze om de beurt adviseren en stemmen (optie A/B/C), en sluit af met één scherp besluit.

Live versie (claude.ai artifact): https://claude.ai/artifact/LX2n3MFw4oithDnHeSnekG

## Opbouw

1. **Vraag** – vrije tekst, met keuze van een ingebouwd bedrijfsprofiel (DCMR Milieudienst Rijnmond) en optioneel eigen aanvullende context (lokaal opgeslagen in de browser).
2. **Verduidelijking** – de AI stelt 2–3 vragen.
3. **Briefing** – beslissing, context, doel, opties A/B/C, zorgen, tijdshorizon; aannames gemarkeerd als "(voorstel)".
4. **Adviesraad** – de voorzitter selecteert 7 adviseurs; elk adviseert vanuit zijn eigen denkkader ("school") en stemt.
5. **Besluit** – één keuze met argumenten, voorwaarden, grootste risico, eerste stap en meting. Vervolgvragen en kopieerbaar verslag.

## Adviseurs

Fictieve adviseurs met geïllustreerde avatars. De ondernemersrollen redeneren volgens publiek bekende denkkaders van o.a. Munger, Hormozi, Bezos, Wickman, Taleb, Godin, Cagan, Lencioni, Buffett, Vaynerchuk, Martell en Thiel. De verzuim/arbo- en VTH-rollen (bedrijfsarts, casemanager, preventiespecialist, arbeidsdeskundige, toezichthouder, specialistisch adviseur, vergunningverlener, jurist) leunen op de gezaghebbende Nederlandse kaders (NVAB, Poortwachter, LHSO, Omgevingswet, Awb).

Aanpassen: zie de constanten `POOL`, `LOOKS` en `PROFILES` bovenin het `<script>`-blok in `index.html`.

## AI-aanroep

De pagina gebruikt `claude.use("sample")` – de ingebouwde AI-capability van claude.ai-artifacts. Buiten de artifact-omgeving (bijv. GitHub Pages) is `window.claude` niet aanwezig en toont de pagina een melding dat de AI niet beschikbaar is. Wil je de pagina zelfstandig draaien, vervang dan de functie `ask()` door een aanroep van je eigen backend die een LLM-API aanspreekt (stuur nooit een API-sleutel vanuit de browser mee).

## Licentie

© Sander – eigen gebruik.
