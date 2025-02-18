# [Danish] Debian Almquist Shell (dash) wc brug: Tæller linjer, ord og tegn i filer

## Oversigt
`wc` (word count) er et kommandolinjeværktøj, der bruges til at tælle antallet af linjer, ord og tegn i en eller flere filer. Det er nyttigt til hurtigt at få indsigt i indholdet af tekstfiler.

## Brug
Den grundlæggende syntaks for `wc`-kommandoen er:

```bash
wc [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Tæller kun linjer.
- `-w`: Tæller kun ord.
- `-c`: Tæller kun tegn.
- `-m`: Tæller kun tegn (inklusive multibyte-tegn).
- `-L`: Viser længden af den længste linje.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `wc` kan bruges:

1. Tæl linjer, ord og tegn i en fil:
   ```bash
   wc filnavn.txt
   ```

2. Tæl kun linjer i en fil:
   ```bash
   wc -l filnavn.txt
   ```

3. Tæl kun ord i en fil:
   ```bash
   wc -w filnavn.txt
   ```

4. Tæl kun tegn i en fil:
   ```bash
   wc -c filnavn.txt
   ```

5. Tæl linjer i flere filer:
   ```bash
   wc fil1.txt fil2.txt
   ```

## Tips
- Brug `wc` i kombination med andre kommandoer ved hjælp af en pipe (`|`) for at analysere output fra en anden kommando. For eksempel:
  ```bash
  ls | wc -l
  ```
  Dette tæller antallet af filer i den aktuelle mappe.
  
- Hvis du arbejder med store filer, kan det være nyttigt at bruge `-l` eller `-w` for at få hurtigere resultater, da disse tællinger generelt er hurtigere end at tælle tegn.