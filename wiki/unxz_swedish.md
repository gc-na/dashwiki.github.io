# [Svenska] Debian Almquist Shell (dash) unxz användning: Avpacka .xz-filer

## Översikt
Kommandot `unxz` används för att avpacka filer som är komprimerade med XZ-algoritmen. Det tar en eller flera .xz-filer som argument och skapar motsvarande okomprimerade filer.

## Användning
Den grundläggande syntaxen för `unxz` är:

```
unxz [alternativ] [argument]
```

## Vanliga alternativ
- `-k`, `--keep`: Behåll den ursprungliga komprimerade filen efter avpackning.
- `-f`, `--force`: Tvinga avpackning även om det finns en fil med samma namn.
- `-v`, `--verbose`: Visa detaljerad information om avpackningsprocessen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `unxz`:

1. Avpacka en fil:
   ```bash
   unxz fil.xz
   ```

2. Avpacka en fil och behåll den komprimerade versionen:
   ```bash
   unxz -k fil.xz
   ```

3. Tvinga avpackning av en fil även om en okomprimerad fil redan finns:
   ```bash
   unxz -f fil.xz
   ```

4. Visa detaljerad information under avpackning:
   ```bash
   unxz -v fil.xz
   ```

## Tips
- Kontrollera alltid att du har tillräckligt med diskutrymme innan du avpackar stora filer.
- Använd `-k` alternativet om du vill behålla den komprimerade filen för säkerhets skull.
- För att avpacka flera filer samtidigt kan du ange dem alla i kommandot:
  ```bash
  unxz fil1.xz fil2.xz fil3.xz
  ```