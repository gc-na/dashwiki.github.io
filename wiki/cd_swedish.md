# [Svenska] Debian Almquist Shell (dash) cd användning: Navigera i kataloger

## Översikt
`cd` (change directory) är ett kommando som används för att ändra den aktuella arbetskatalogen i terminalen. Genom att använda `cd` kan du navigera mellan olika kataloger på ditt filsystem.

## Användning
Den grundläggande syntaxen för `cd`-kommandot är:

```
cd [alternativ] [argument]
```

## Vanliga alternativ
- `-` : Gå tillbaka till den föregående katalogen.
- `..` : Gå upp en nivå i katalogstrukturen.
- `~` : Gå till användarens hemkatalog.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `cd`-kommandot:

1. Gå till hemkatalogen:
   ```sh
   cd ~
   ```

2. Gå upp en nivå i katalogstrukturen:
   ```sh
   cd ..
   ```

3. Gå till en specifik katalog, till exempel `/var/log`:
   ```sh
   cd /var/log
   ```

4. Gå tillbaka till den föregående katalogen:
   ```sh
   cd -
   ```

5. Gå till en relativ katalog, till exempel `Documents`:
   ```sh
   cd Documents
   ```

## Tips
- Använd `cd -` för snabbt att växla mellan två kataloger.
- Du kan använda tab-tangenten för att autocompleta katalognamn, vilket sparar tid och minskar risken för fel.
- Kom ihåg att katalognamn är skiftlägeskänsliga i Unix-baserade system, så se till att du skriver dem korrekt.