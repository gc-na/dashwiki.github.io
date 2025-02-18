# [Danish] Debian Almquist Shell (dash) diff brug: Sammenlign filer

## Oversigt
`diff`-kommandoen bruges til at sammenligne indholdet af to filer linje for linje. Den viser forskellene mellem filerne, hvilket gør det lettere at identificere ændringer.

## Brug
Den grundlæggende syntaks for `diff`-kommandoen er som følger:

```bash
diff [muligheder] [argumenter]
```

## Almindelige muligheder
- `-u`: Viser output i "unified" format, som er mere læsbart.
- `-i`: Ignorerer forskelle i store og små bogstaver.
- `-w`: Ignorerer alle hvide tegn, hvilket gør det lettere at sammenligne indhold.
- `-r`: Sammenligner mapper rekursivt.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `diff`:

1. Sammenlign to tekstfiler:
   ```bash
   diff fil1.txt fil2.txt
   ```

2. Brug unified format til at vise forskelle:
   ```bash
   diff -u fil1.txt fil2.txt
   ```

3. Ignorer forskelle i store og små bogstaver:
   ```bash
   diff -i fil1.txt fil2.txt
   ```

4. Sammenlign to mapper rekursivt:
   ```bash
   diff -r mappe1/ mappe2/
   ```

## Tips
- Brug `-u`-muligheden for at få et mere læsbart output, især når du arbejder med patches.
- Kombiner `diff` med `grep` for at filtrere specifikke linjer, hvis du kun er interesseret i bestemte ændringer.
- Gem output fra `diff` til en fil ved at omdirigere output:
  ```bash
  diff fil1.txt fil2.txt > forskelle.txt
  ```