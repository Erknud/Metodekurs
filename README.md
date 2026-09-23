# Kodebok: Medieundersøkelsen 2026 – befolkningsutvalget (undervisningsversjon)

Et lite utvalg variabler fra Medieundersøkelsen 2026 (Nordiske Mediedager), kun befolkningsutvalget (n = 1061). Respondentene har fått nye, tilfeldige id-er og kan ikke kobles til originaldataene.

«Vet ikke» og «Ønsker ikke å svare» er satt som manglende verdi (`NA`).

Filer: `mu26_befolkning.rds` (for R) og `mu26_befolkning.csv`.

## Bakgrunn

| Variabel | Beskrivelse | Verdier |
|---|---|---|
| `id` | Respondent-id | 1–1061 |
| `kjonn` | Kjønn | Mann, Kvinne |
| `aldersgruppe` | Alder i grupper | 18-24, 25-34, 35-44, 45-54, 55-64, 65+ |
| `landsdel` | Landsdel | Oslo og Akershus, Sør-Østlandet, Agder og Rogaland, Vestlandet, Trøndelag, Nord-Norge |
| `utdanning` | Høyeste fullførte utdanning | Grunnskole/videregående, Universitet/høyskole 1-4 år, Universitet/høyskole 5+ år |

## Politikk

| Variabel | Spørsmål | Verdier |
|---|---|---|
| `venstre_hoyre` | Hvor vil du plassere deg selv på en skala fra venstre til høyre i politikken? | 0 = Helt til venstre … 5 = I midten … 10 = Helt til høyre |
| `parti` | Dersom det var stortingsvalg i morgen, hvilket parti ville du da stemme på? | Partinavn eller «Annet parti» (blankt, ville ikke stemt og vet ikke = `NA`) |

## Nyheter

| Variabel | Spørsmål | Verdier |
|---|---|---|
| `tillit_nyheter` | I hvilken grad har du tiltro til nyhetsmediene generelt? | 1 = Ingen tiltro, 2 = Mindre tiltro, 3 = Noe tiltro, 4 = Stor tiltro |
| `unngar_nyheter` | Har du i løpet av det siste året aktivt forsøkt å unngå nyheter og/eller enkelte tema i nyhetene? | Nei, aldri; Ja, men sjelden; Ja, noen ganger; Ja, store deler av tiden |

## Kunstig intelligens (KI)

| Variabel | Spørsmål | Verdier |
|---|---|---|
| `ki_bruk` | Bruker du noen KI-verktøy i dag? Hvis ja, hvor ofte? | 0 = Aldri, 1 = Sjeldnere enn månedlig, 2 = Noen ganger i måneden, 3 = Ukentlig, 4 = Daglig, 5 = Flere ganger daglig |
| `bruker_chatgpt` | Bruker du ChatGPT regelmessig? | 0 = Nei, 1 = Ja |
| `ki_konsekvenser` | Alt i alt, tror du utviklingen av KI vil ha positive eller negative konsekvenser for samfunnet de neste fem årene? | 1 = Svært negative, 2 = Ganske negative, 3 = Verken eller, 4 = Ganske positive, 5 = Svært positive |
| `ki_eller_journalist` | «Så lenge informasjonen er korrekt, spiller det liten rolle for meg om en nyhetssak er skrevet av en journalist eller generert ved hjelp av KI» | 1 = Helt uenig, 2 = Delvis uenig, 3 = Verken eller, 4 = Delvis enig, 5 = Helt enig |
| `tillit_ki_redaksjoner` | I hvilken grad har du tillit til at norske redaksjoner som bruker KI i nyhetsformidling sikrer at informasjonen som publiseres er korrekt? | 1 = Ikke i det hele tatt, 2 = I ganske liten grad, 3 = I noen grad, 4 = I ganske stor grad, 5 = I svært stor grad |

## Eksperiment: KI som kilde

Respondentene ble tilfeldig fordelt på fem versjoner av følgende scenario, der bare kilden (KILDE) varierte:

> «En venn du vanligvis stoler på har delt et viralt bilde i sosiale medier som angivelig viser en kjent offentlig person begå en kriminell handling. Vennen har undersøkt om bildet er ekte ved å spørre (KILDE), som svarte at det fremstår som ekte og ikke manipulert.»

Kilden var enten en forsker på desinformasjon, OpenAIs KI-tjeneste ChatGPT, Googles KI-tjeneste Gemini, VGs KI-tjeneste heiVG eller Elon Musks KI-tjeneste Grok.

| Variabel | Beskrivelse | Verdier |
|---|---|---|
| `eksp_kilde` | Kilden respondenten fikk i sin versjon av spørsmålet | Forsker (en forsker på desinformasjon), ChatGPT, Gemini, heiVG (VGs KI-tjeneste), Grok |
| `tillit_bilde` | I hvor stor grad ville du hatt tillit til at bildet faktisk er ekte i et slikt tilfelle? | 1 = Ikke i det hele tatt, 2 = I ganske liten grad, 3 = I noen grad, 4 = I ganske stor grad, 5 = I svært stor grad |
