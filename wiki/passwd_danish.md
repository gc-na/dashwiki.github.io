# [Danish] Debian Almquist Shell (dash) passwd brug: Ændre brugeradgangskoder

## Overview
`passwd`-kommandoen bruges til at ændre adgangskoden for en bruger i systemet. Det er en vigtig del af systemadministration, da det hjælper med at sikre, at kun autoriserede brugere har adgang til deres konti.

## Usage
Den grundlæggende syntaks for `passwd`-kommandoen er:

```bash
passwd [options] [arguments]
```

## Common Options
- `-d`: Slet adgangskoden for brugeren, hvilket gør kontoen uden adgangskode.
- `-e`: Tving brugeren til at ændre deres adgangskode ved næste login.
- `-l`: Lås brugerkontoen ved at tilføje et "!" foran adgangskoden.
- `-u`: Lås op for en brugerkonto ved at fjerne "!" fra adgangskoden.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du bruger `passwd`-kommandoen:

1. Ændre din egen adgangskode:
   ```bash
   passwd
   ```

2. Ændre en anden brugers adgangskode (kræver root-rettigheder):
   ```bash
   sudo passwd brugernavn
   ```

3. Tving en bruger til at ændre adgangskoden ved næste login:
   ```bash
   sudo passwd -e brugernavn
   ```

4. Lås en brugerkonto:
   ```bash
   sudo passwd -l brugernavn
   ```

5. Lås op for en brugerkonto:
   ```bash
   sudo passwd -u brugernavn
   ```

## Tips
- Sørg for at vælge en stærk adgangskode, der kombinerer bogstaver, tal og specialtegn.
- Brug `passwd -e` for at sikre, at brugere ændrer deres adgangskode regelmæssigt.
- Vær opmærksom på, at ændringer i adgangskoder kan påvirke automatiserede scripts og tjenester, der bruger disse konti.