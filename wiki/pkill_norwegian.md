# [Norsk] Debian Almquist Shell (dash) pkill bruk: Avslutt prosesser basert på navn

## Oversikt
`pkill`-kommandoen brukes til å avslutte prosesser basert på prosessnavn eller andre kriterier. Dette gjør det enkelt å stoppe flere prosesser samtidig uten å måtte spesifisere prosess-ID-er (PID).

## Bruk
Grunnleggende syntaks for `pkill`-kommandoen er som følger:

```
pkill [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`: Matcher prosessnavn med hele kommandolinjen.
- `-n`: Dreper den nyeste prosessen som matcher.
- `-o`: Dreper den eldste prosessen som matcher.
- `-signal`: Angir signalet som skal sendes til prosessen (standard er SIGTERM).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `pkill`:

### Avslutt en prosess ved navn
For å avslutte alle prosesser med navnet "firefox":
```bash
pkill firefox
```

### Avslutt prosesser med et spesifikt signal
For å sende SIGKILL til alle prosesser med navnet "myapp":
```bash
pkill -9 myapp
```

### Avslutt prosessen basert på hele kommandolinjen
For å avslutte prosesser der kommandolinjen inneholder "python script.py":
```bash
pkill -f "python script.py"
```

### Avslutt den nyeste prosessen
For å avslutte den nyeste prosessen med navnet "node":
```bash
pkill -n node
```

## Tips
- Vær forsiktig når du bruker `pkill`, spesielt med kraftige signaler som SIGKILL, da dette kan føre til tap av data.
- Bruk `pgrep`-kommandoen først for å se hvilke prosesser som vil bli påvirket av `pkill`.
- Du kan kombinere `pkill` med andre verktøy som `grep` for mer spesifikke søk.