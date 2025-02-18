# [Danish] Debian Almquist Shell (dash) head brug: Vis de første linjer i en fil

## Overview
`head`-kommandoen bruges til at vise de første linjer af en fil. Det er nyttigt, når du hurtigt vil se indholdet af en fil uden at åbne den helt.

## Usage
Den grundlæggende syntaks for `head`-kommandoen er:

```bash
head [options] [arguments]
```

## Common Options
- `-n [antal]`: Angiver hvor mange linjer der skal vises. Standard er 10 linjer.
- `-c [antal]`: Viser et bestemt antal byte i stedet for linjer.
- `-q`: Undertrykker filnavne, når der vises indhold fra flere filer.
- `-v`: Viser filnavne, selv når der kun er én fil.

## Common Examples
Her er nogle praktiske eksempler på brug af `head`:

1. Vis de første 10 linjer af en fil:
   ```bash
   head filnavn.txt
   ```

2. Vis de første 5 linjer af en fil:
   ```bash
   head -n 5 filnavn.txt
   ```

3. Vis de første 20 byte af en fil:
   ```bash
   head -c 20 filnavn.txt
   ```

4. Vis de første 10 linjer fra flere filer:
   ```bash
   head fil1.txt fil2.txt
   ```

5. Vis de første 10 linjer og inkluder filnavnet:
   ```bash
   head -v filnavn.txt
   ```

## Tips
- Brug `head` i kombination med `tail` for at få et hurtigt overblik over en fil.
- Hvis du arbejder med store logfiler, kan `head` hjælpe dig med at få et hurtigt indblik i de nyeste optegnelser.
- Overvej at bruge `-n` optionen for at tilpasse antallet af linjer, du ønsker at se, så du kun får den information, du har brug for.