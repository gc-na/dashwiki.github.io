# [Danish] Debian Almquist Shell (dash) whoami brug: Identificer den aktuelle bruger

## Oversigt
`whoami`-kommandoen bruges til at vise navnet på den nuværende bruger, der er logget ind på systemet. Det er en simpel, men nyttig kommando, når du har brug for at bekræfte, hvilken bruger du arbejder som.

## Brug
Den grundlæggende syntaks for `whoami`-kommandoen er:

```
whoami [options] [arguments]
```

## Almindelige muligheder
Der er ikke mange muligheder for `whoami`, men her er nogle af de mest almindelige:

- **--help**: Viser hjælp og information om brugen af kommandoen.
- **--version**: Viser versionen af `whoami`-kommandoen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `whoami`:

1. For at vise det nuværende brugernavn:
   ```bash
   whoami
   ```

2. For at få hjælp til `whoami`-kommandoen:
   ```bash
   whoami --help
   ```

3. For at se versionen af `whoami`:
   ```bash
   whoami --version
   ```

## Tips
- Brug `whoami` i scripts for at sikre, at du kender den bruger, der kører scriptet.
- Kombiner `whoami` med andre kommandoer for at tilpasse output, f.eks. ved at bruge det i en betingelse i et script.
- Husk, at `whoami` kun viser det nuværende brugernavn og ikke yderligere oplysninger om brugeren.