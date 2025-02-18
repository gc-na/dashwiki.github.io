# [Danish] Debian Almquist Shell (dash) cmp brug: Sammenlign to filer byte for byte

## Overview
`cmp`-kommandoen bruges til at sammenligne to filer byte for byte. Den identificerer den første forskel mellem filerne og kan være nyttig til at finde ud af, om to filer er identiske eller ej.

## Usage
Den grundlæggende syntaks for `cmp`-kommandoen er:

```bash
cmp [options] [arguments]
```

## Common Options
- `-l`: Vis byte-positionerne for forskelle.
- `-s`: Tjekker kun, om filerne er forskellige, uden at vise output.
- `-i OFFSET`: Angiv en offset for at starte sammenligningen fra en bestemt byte.
- `-n N`: Sammenlign kun de første N bytes af filerne.

## Common Examples
Her er nogle praktiske eksempler på brugen af `cmp`:

1. Sammenlign to filer og vis forskellen:
   ```bash
   cmp fil1.txt fil2.txt
   ```

2. Tjek om to filer er ens uden at vise output:
   ```bash
   cmp -s fil1.txt fil2.txt
   ```

3. Vis byte-positionerne for forskelle mellem to filer:
   ```bash
   cmp -l fil1.txt fil2.txt
   ```

4. Sammenlign kun de første 100 bytes af to filer:
   ```bash
   cmp -n 100 fil1.txt fil2.txt
   ```

## Tips
- Brug `cmp` i scripts til at automatisere kontrol af filintegritet.
- Kombiner `cmp` med `&&` for at udføre handlinger baseret på sammenligningsresultater.
- Overvej at bruge `diff`-kommandoen, hvis du ønsker en mere detaljeret sammenligning af tekstfiler.