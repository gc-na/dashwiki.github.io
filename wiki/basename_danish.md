# [Danish] Debian Almquist Shell (dash) basename brug: Fjerner stien fra filnavne

## Overview
`basename` er et kommando, der bruges til at fjerne stien fra et filnavn og kun returnere selve filnavnet. Dette er nyttigt, når man arbejder med filstier og kun ønsker at fokusere på filnavnet.

## Usage
Den grundlæggende syntaks for `basename` er:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: Behandler alle argumenter og returnerer filnavne for hver enkelt.
- `-s`: Angiver en suffix, der skal fjernes fra filnavnet.

## Common Examples
Her er nogle praktiske eksempler på brugen af `basename`:

1. Fjerne stien fra et filnavn:
   ```bash
   basename /path/to/file.txt
   ```
   Output: `file.txt`

2. Fjerne stien og en suffix fra et filnavn:
   ```bash
   basename /path/to/file.txt .txt
   ```
   Output: `file`

3. Behandle flere filer på én gang:
   ```bash
   basename -a /path/to/file1.txt /path/to/file2.txt
   ```
   Output:
   ```
   file1.txt
   file2.txt
   ```

## Tips
- Brug `basename` i scripts for at gøre filnavne mere læsbare.
- Kombiner `basename` med andre kommandoer som `find` for at håndtere filer effektivt.
- Vær opmærksom på, at `basename` kun fjerner den sidste del af stien, så hvis du har flere mapper med samme navn, kan det føre til forvirring.