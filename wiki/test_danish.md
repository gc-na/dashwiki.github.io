# [Danish] Debian Almquist Shell (dash) test brug: Kontroller betingelser

## Oversigt
`test`-kommandoen bruges i dash til at evaluere betingelser og returnere en statuskode baseret på resultatet. Den kan bruges til at kontrollere filers eksistens, sammenligne værdier og evaluere logiske udtryk.

## Brug
Den grundlæggende syntaks for `test`-kommandoen er:

```bash
test [options] [arguments]
```

## Almindelige muligheder
- `-e`: Tjekker om en fil eksisterer.
- `-f`: Tjekker om en fil er en regulær fil.
- `-d`: Tjekker om en fil er en mappe.
- `-z`: Tjekker om længden af en streng er nul.
- `=`: Sammenligner to strenge for lighed.
- `-lt`: Tjekker om det første tal er mindre end det andet.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `test`:

1. Tjek om en fil eksisterer:
   ```bash
   test -e /path/to/file && echo "Filen findes"
   ```

2. Tjek om en fil er en regulær fil:
   ```bash
   test -f /path/to/file && echo "Det er en regulær fil"
   ```

3. Tjek om en mappe eksisterer:
   ```bash
   test -d /path/to/directory && echo "Det er en mappe"
   ```

4. Tjek om en streng er tom:
   ```bash
   str="Hello"
   test -z "$str" && echo "Strengen er tom" || echo "Strengen er ikke tom"
   ```

5. Sammenlign to tal:
   ```bash
   a=5
   b=10
   test $a -lt $b && echo "$a er mindre end $b"
   ```

## Tips
- Brug `&&` og `||` til at kæde flere kommandoer sammen baseret på resultatet af `test`.
- For mere komplekse betingelser kan du kombinere flere `test`-udtryk med `-a` (og) og `-o` (eller).
- Det er ofte en god idé at bruge `[` og `]` som en synonym for `test`, da det kan gøre syntaksen mere læsbar. For eksempel: `[ -e /path/to/file ]`.