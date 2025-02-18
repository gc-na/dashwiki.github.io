# [Svenska] Debian Almquist Shell (dash) mv Användning: Flytta eller döpa om filer och kataloger

## Översikt
Kommandot `mv` används för att flytta eller döpa om filer och kataloger i Unix-liknande operativsystem, inklusive Debian Almquist Shell (dash). Det är ett grundläggande verktyg för filhantering.

## Användning
Den grundläggande syntaxen för kommandot är:

```
mv [alternativ] [källfil] [mål]
```

## Vanliga alternativ
- `-i`: Fråga innan en befintlig fil skrivs över.
- `-u`: Flytta endast om källfilen är nyare än målfilerna eller om målfilerna inte finns.
- `-v`: Visa detaljerad information om vad som flyttas.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mv`:

1. Flytta en fil till en annan katalog:
   ```bash
   mv fil.txt /väg/till/destination/
   ```

2. Döpa om en fil:
   ```bash
   mv gammal_namn.txt nytt_namn.txt
   ```

3. Flytta flera filer till en katalog:
   ```bash
   mv fil1.txt fil2.txt /väg/till/destination/
   ```

4. Använda alternativet `-i` för att undvika oavsiktlig överskrivning:
   ```bash
   mv -i fil.txt /väg/till/destination/
   ```

## Tips
- Använd alltid alternativet `-i` om du är osäker på om en fil redan finns i målkatalogen för att förhindra oavsiktlig förlust av data.
- Kontrollera alltid filnamn och sökvägar noggrant innan du kör kommandot för att undvika misstag.
- Du kan använda `tab` för att autocompleta fil- och katalognamn, vilket kan spara tid och minska risken för fel.