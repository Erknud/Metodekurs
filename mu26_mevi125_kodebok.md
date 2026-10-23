# Kodebok: Medieundersøkelsen 2026 og MEVI125-undersøkelsen 2026

Denne filen brukes i gruppeoppgaven (Del 2) i MEVI125. Den inneholder to utvalg som har svart på de samme spørsmålene:

- **Befolkningen:** et utvalg av den norske befolkningen fra Medieundersøkelsen 2026 (Nordiske Mediedager), n = 1061. Respondentene har fått nye, tilfeldige id-er og kan ikke kobles til originaldataene.
- **MEVI125:** MEVI125-studentene, som svarte på de samme spørsmålene på Lab 1 Spørreundersøkelser 27.10.2026. Undersøkelsen er anonym.

Fram til 28.10.2026 inneholder filen bare befolkningsutvalget. Da legges svarene fra MEVI125-studentene til i den samme filen.

Les inn filen i R:

```r
d <- readRDS(url("https://raw.githubusercontent.com/Erknud/Metodekurs/main/mu26_mevi125.rds"))
```

«Vet ikke» og «Ønsker ikke å svare» er satt som manglende verdi (`NA`).

## Variabler

| Variabel | Spørsmål / beskrivelse | Verdier |
|---|---|---|
| `id` | Respondent-id | 1–1061 (befolkningen), fra 1062 (MEVI125) |
| `utvalg` | Hvilket utvalg personen tilhører | Befolkningen, MEVI125 |
| `aldersgruppe` | Alder i grupper | 18-24, 25-34, 35-44, 45-54, 55-64, 65+ |
| `bruker_chatgpt` | Bruker du ChatGPT regelmessig? | 0 = Nei, 1 = Ja |
| `ki_bruk` | Bruker du noen KI-verktøy i dag? Hvis ja, hvor ofte? | 0 = Aldri, 1 = Sjeldnere enn månedlig, 2 = Noen ganger i måneden, 3 = Ukentlig, 4 = Daglig, 5 = Flere ganger daglig |
| `tillit_nyheter` | I hvilken grad har du tiltro til nyhetsmediene generelt? | 1 = Ingen tiltro, 2 = Mindre tiltro, 3 = Noe tiltro, 4 = Stor tiltro |
| `tillit_ki_redaksjoner` | I hvilken grad har du tillit til at norske redaksjoner som bruker KI i nyhetsformidling sikrer at informasjonen som publiseres er korrekt? | 1 = Ikke i det hele tatt, 2 = I ganske liten grad, 3 = I noen grad, 4 = I ganske stor grad, 5 = I svært stor grad |
| `ki_konsekvenser` | Alt i alt, tror du utviklingen av KI vil ha positive eller negative konsekvenser for samfunnet de neste fem årene? | 1 = Svært negative, 2 = Ganske negative, 3 = Verken eller, 4 = Ganske positive, 5 = Svært positive |
