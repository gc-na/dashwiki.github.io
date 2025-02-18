# [Svenska] Debian Almquist Shell (dash) nohup användning: Kör kommandon oavsett inloggning

## Översikt
Kommandot `nohup` (no hang up) används för att köra ett kommando så att det fortsätter att köras även om användaren loggar ut från systemet. Det är särskilt användbart för långvariga processer som man vill ska fortsätta i bakgrunden.

## Användning
Den grundläggande syntaxen för `nohup` är:

```
nohup [alternativ] [argument]
```

## Vanliga alternativ
- `&` - Kör kommandot i bakgrunden.
- `-h` - Visa hjälpmeddelande.
- `-v` - Visa versionsinformation.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `nohup`:

1. Kör ett skript i bakgrunden:
   ```bash
   nohup ./mitt_skript.sh &
   ```

2. Kör en långvarig process och skriv ut loggar till en fil:
   ```bash
   nohup python mitt_program.py > logg.txt 2>&1 &
   ```

3. Använd `nohup` för att köra en kommandorad som inte ska avbrytas:
   ```bash
   nohup tar -czf backup.tar.gz /min/katalog & 
   ```

## Tips
- Använd `&` för att köra kommandot i bakgrunden så att du kan fortsätta använda terminalen.
- Kontrollera loggfilen som `nohup` skapar (vanligtvis `nohup.out`) för att se utdata och felmeddelanden.
- Tänk på att stänga av processer som körs i bakgrunden om de inte längre behövs, för att spara systemresurser.