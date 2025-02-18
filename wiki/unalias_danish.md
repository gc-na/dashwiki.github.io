# [Danish] Debian Almquist Shell (dash) unalias: Fjerner aliaser

## Overview
`unalias` kommandoen bruges til at fjerne aliaser, der er blevet oprettet i den nuværende shell-session. Aliaser er genveje til længere kommandoer, og `unalias` giver dig mulighed for at rydde op i dem, hvis du ikke længere har brug for dem.

## Usage
Den grundlæggende syntaks for `unalias` kommandoen er:

```sh
unalias [options] [arguments]
```

## Common Options
- `-a`: Fjerner alle aliaser i den nuværende session.
- `-m`: Fjerner aliaser, der matcher et givet mønster.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge `unalias`:

1. **Fjerne et specifikt alias:**
   Hvis du har oprettet et alias kaldet `ll`, kan du fjerne det med følgende kommando:
   ```sh
   unalias ll
   ```

2. **Fjerne alle aliaser:**
   For at fjerne alle aliaser, kan du bruge:
   ```sh
   unalias -a
   ```

3. **Fjerne aliaser, der matcher et mønster:**
   Hvis du vil fjerne alle aliaser, der starter med `g`, kan du gøre det med:
   ```sh
   unalias g*
   ```

## Tips
- Husk at aliaser kun gælder for den nuværende session. Hvis du genstarter din shell, vil de oprindelige aliaser være tilgængelige igen.
- Du kan bruge `alias` kommandoen til at se en liste over alle nuværende aliaser, før du fjerner dem.
- Overvej at tilføje nyttige aliaser til din shell-konfigurationsfil, så de automatisk oprettes, når du starter en ny session.