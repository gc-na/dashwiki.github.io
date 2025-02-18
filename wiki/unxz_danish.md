# [Danish] Debian Almquist Shell (dash) unxz brug: Udpak .xz filer

## Oversigt
`unxz` er et kommandolinjeværktøj, der bruges til at dekomprimere filer, der er komprimeret med XZ-formatet. Det fjerner komprimeringen fra en .xz-fil og gendanner den originale fil.

## Brug
Den grundlæggende syntaks for `unxz`-kommandoen er:

```
unxz [muligheder] [argumenter]
```

## Almindelige muligheder
- `-k`, `--keep`: Behold den originale komprimerede fil efter dekomprimering.
- `-f`, `--force`: Tving dekomprimering, selvom outputfilen allerede eksisterer.
- `-v`, `--verbose`: Vis detaljeret output under dekomprimeringsprocessen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `unxz`:

1. Dekomprimere en enkelt .xz-fil:
   ```bash
   unxz fil.xz
   ```

2. Dekomprimere en .xz-fil og beholde den originale:
   ```bash
   unxz -k fil.xz
   ```

3. Tvinge dekomprimering, hvis outputfilen allerede findes:
   ```bash
   unxz -f fil.xz
   ```

4. Dekomprimere en fil og vise detaljeret output:
   ```bash
   unxz -v fil.xz
   ```

## Tips
- Sørg for at have tilstrækkelig diskplads, da dekomprimering kan kræve ekstra plads til den originale fil.
- Brug `-k`-muligheden, hvis du vil bevare den komprimerede fil til fremtidig brug.
- Tjek filens integritet efter dekomprimering for at sikre, at processen er lykkedes.