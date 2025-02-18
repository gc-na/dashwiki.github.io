# [Danish] Debian Almquist Shell (dash) zip brug: Komprimér filer

## Overview
`zip` er et kommandolinjeværktøj, der bruges til at komprimere filer og mapper til et enkelt zip-arkiv. Dette gør det lettere at opbevare og overføre flere filer som én enhed.

## Usage
Den grundlæggende syntaks for `zip`-kommandoen er som følger:

```bash
zip [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `zip` med korte forklaringer:

- `-r`: Rekursivt komprimere mapper og deres indhold.
- `-e`: Krypter zip-arkivet med en adgangskode.
- `-9`: Brug den højeste komprimeringsgrad.
- `-d`: Slet filer fra zip-arkivet.
- `-l`: Liste indholdet af zip-arkivet.

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `zip`:

1. **Komprimere en enkelt fil:**
   ```bash
   zip myarchive.zip myfile.txt
   ```

2. **Komprimere flere filer:**
   ```bash
   zip myarchive.zip file1.txt file2.txt file3.txt
   ```

3. **Rekursivt komprimere en mappe:**
   ```bash
   zip -r myarchive.zip myfolder/
   ```

4. **Kryptere zip-arkivet:**
   ```bash
   zip -e myarchive.zip myfile.txt
   ```

5. **Slette en fil fra et zip-arkiv:**
   ```bash
   zip -d myarchive.zip myfile.txt
   ```

## Tips
- Overvej at bruge `-9` for at opnå den bedste komprimering, især hvis du har meget data.
- Brug `-e` til at beskytte følsomme filer med en adgangskode.
- For at se indholdet af et zip-arkiv uden at udpakke det, kan du bruge `unzip -l myarchive.zip`.