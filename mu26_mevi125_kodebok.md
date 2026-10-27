# Kodebok: Medieundersøkelsen 2026 og MEVI125-undersøkelsen 2026

Denne filen brukes i gruppeoppgaven (Del 2) i MEVI125. Den inneholder to utvalg som har svart på de samme spørsmålene:

- **Befolkningen:** et utvalg av den norske befolkningen fra Medieundersøkelsen 2026 (Nordiske Mediedager), n = 1061. Respondentene har fått nye, tilfeldige id-er og kan ikke kobles til originaldataene.
- **MEVI125:** MEVI125-studentene, som svarte på de samme spørsmålene på Lab 1 Spørreundersøkelser 27.10.2026, n = 70. Undersøkelsen er anonym.

Fram til 28.10.2026 inneholder filen bare befolkningsutvalget. Da legges svarene fra MEVI125-studentene til i den samme filen.

Les inn filen i R:

```r
d <- readRDS(url("https://raw.githubusercontent.com/Erknud/Metodekurs/main/mu26_mevi125.rds"))
```

«Vet ikke» og «Ønsker ikke å svare» er satt som manglende verdi (`NA`). I MEVI125-utvalget er også noen få verdier satt som `NA` av hensyn til anonymiteten.

## Bakgrunn og utvalg

| Variabel | Spørsmål / beskrivelse | Verdier |
|---|---|---|
| `id` | Respondent-id | 1–1061 (befolkningen), 1062–1131 (MEVI125) |
| `utvalg` | Hvilket utvalg personen tilhører | Befolkningen, MEVI125 |
| `aldersgruppe` | Alder i grupper | 18-24, 25-34, 35-44, 45-54, 55-64, 65+ |
| `kjonn` | Kjønn | Mann, Kvinne |

## Bruk av KI

| Variabel | Spørsmål / beskrivelse | Verdier |
|---|---|---|
| `ki_bruk` | Bruker du noen KI-verktøy i dag? Hvis ja, hvor ofte? | 0 = Nei, aldri, 1 = Ja, men sjeldnere, 2 = Ja, noen ganger i måneden, 3 = Ja, ukentlig, 4 = Ja, daglig, 5 = Ja, flere ganger daglig |

Spørsmålet «Hvilke av følgende KI-verktøy bruker du regelmessig?» ble bare stilt til dem som bruker KI (`ki_bruk` større enn 0). Hvert verktøy har sin egen variabel:

| Variabel | Verktøy |
|---|---|
| `bruker_chatgpt` | ChatGPT |
| `bruker_gemini` | Gemini |
| `bruker_copilot` | Copilot |
| `bruker_claude` | Claude |
| `bruker_perplexity` | Perplexity |
| `bruker_grok` | Grok (på X) |
| `bruker_snapchat` | Snapchat My AI |
| `bruker_chaton` | Chat On |
| `bruker_mistral` | LeChat / Mistral |
| `bruker_andre` | Andre verktøy |

Verdier for alle verktøyvariablene: 1 = Ja (krysset av for verktøyet), 0 = Nei (krysset ikke av, eller bruker ikke KI). Andelen gjelder altså alle i utvalget, også dem som ikke bruker KI. Vil du se andelen blant dem som bruker KI, kan du filtrere på `ki_bruk > 0`.

## Tillit og syn på KI

| Variabel | Spørsmål | Verdier |
|---|---|---|
| `tillit_nyheter` | I hvilken grad har du tiltro til nyhetsmediene generelt? | 1 = Ingen tiltro, 2 = Mindre tiltro, 3 = Noe tiltro, 4 = Stor tiltro |
| `tillit_ki_redaksjoner` | I hvilken grad har du tillit til at norske redaksjoner som bruker KI i nyhetsformidling sikrer at informasjonen som publiseres er korrekt? | 1 = Ikke i det hele tatt, 2 = I ganske liten grad, 3 = I noen grad, 4 = I ganske stor grad, 5 = I svært stor grad |
| `ki_konsekvenser` | Alt i alt, tror du utviklingen av kunstig intelligens vil hovedsakelig ha positive eller negative konsekvenser for samfunnet de neste fem årene? | 1 = Svært negative, 2 = Ganske negative, 3 = Verken eller, 4 = Ganske positive, 5 = Svært positive |
