# [Danish] Debian Almquist Shell (dash) rmdir brug: Slet tomme mapper

## Oversigt
`rmdir`-kommandoen bruges til at fjerne tomme mapper i Unix-lignende operativsystemer. Hvis mappen indeholder filer eller undermapper, vil kommandoen ikke kunne udføre sletningen.

## Brug
Den grundlæggende syntaks for `rmdir`-kommandoen er:

```
rmdir [muligheder] [argumenter]
```

## Almindelige muligheder
- `--ignore-fail-on-non-empty`: Ignorerer fejl, hvis mappen ikke er tom.
- `--verbose`: Viser detaljer om, hvad der bliver slettet.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `rmdir`:

1. Slet en tom mappe:
   ```bash
   rmdir /sti/til/tom/mappe
   ```

2. Slet flere tomme mapper på én gang:
   ```bash
   rmdir /sti/til/mappe1 /sti/til/mappe2
   ```

3. Brug `--verbose` for at se, hvad der bliver slettet:
   ```bash
   rmdir --verbose /sti/til/tom/mappe
   ```

4. Ignorer fejl ved ikke-tomme mapper:
   ```bash
   rmdir --ignore-fail-on-non-empty /sti/til/ikke-tom/mappe
   ```

## Tips
- Sørg for, at mappen er tom, før du bruger `rmdir`, ellers vil kommandoen fejle.
- Brug `rmdir` med forsigtighed, da det ikke kan gendanne slettede mapper.
- Overvej at bruge `rm -r` til at slette mapper, der indeholder filer, men vær opmærksom på, at dette vil slette alt indholdet.