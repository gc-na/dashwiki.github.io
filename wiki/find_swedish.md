# [Svenska] Debian Almquist Shell (dash) find användning: Hitta filnamn

## Översikt
`find`-kommandot används för att söka efter filer och kataloger i ett filsystem baserat på olika kriterier som namn, typ, storlek och mer. Det är ett kraftfullt verktyg för att navigera och hantera filer i Unix-liknande operativsystem.

## Användning
Den grundläggande syntaxen för `find`-kommandot är:

```bash
find [alternativ] [argument]
```

## Vanliga alternativ
- `-name`: Sök efter filer med ett specifikt namn.
- `-type`: Filtyp (t.ex. `f` för filer, `d` för kataloger).
- `-size`: Sök efter filer baserat på storlek (t.ex. `+100M` för större än 100 MB).
- `-mtime`: Sök efter filer baserat på ändringsdatum (t.ex. `-mtime -7` för filer ändrade de senaste 7 dagarna).
- `-exec`: Utför ett kommando på de filer som hittas.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `find`-kommandot:

1. Sök efter en fil med ett specifikt namn:
   ```bash
   find /sökväg/till/katalog -name "filnamn.txt"
   ```

2. Sök efter alla kataloger:
   ```bash
   find /sökväg/till/katalog -type d
   ```

3. Sök efter filer större än 100 MB:
   ```bash
   find /sökväg/till/katalog -type f -size +100M
   ```

4. Sök efter filer som ändrades under de senaste 7 dagarna:
   ```bash
   find /sökväg/till/katalog -mtime -7
   ```

5. Ta bort alla `.tmp`-filer:
   ```bash
   find /sökväg/till/katalog -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Använd `-print` för att visa resultatet av din sökning om det inte skrivs ut automatiskt.
- Kombinera alternativ för mer specifika sökningar, till exempel `find /sökväg -type f -name "*.log" -mtime -30` för att hitta loggfiler som ändrades de senaste 30 dagarna.
- Var försiktig med `-exec` alternativet, särskilt med kommandon som `rm`, för att undvika oavsiktlig radering av filer.