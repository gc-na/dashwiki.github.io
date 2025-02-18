# [Danish] Debian Almquist Shell (dash) cp brug: Kopier filer og mapper

## Oversigt
`cp`-kommandoen bruges til at kopiere filer og mapper fra et sted til et andet i Unix-lignende operativsystemer, herunder Debian Almquist Shell (dash). Det er en grundlæggende og ofte anvendt kommando til filhåndtering.

## Brug
Den grundlæggende syntaks for `cp`-kommandoen er som følger:

```bash
cp [muligheder] [argumenter]
```

## Almindelige muligheder
- `-r`: Kopierer mapper rekursivt.
- `-i`: Spørger om bekræftelse, før der overskrives en eksisterende fil.
- `-u`: Kopierer kun, hvis kildefilen er nyere end destinationsfilen eller hvis destinationsfilen ikke findes.
- `-v`: Viser detaljer om, hvad der bliver kopieret.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `cp`-kommandoen kan bruges:

1. **Kopiere en fil til en anden placering:**
   ```bash
   cp fil.txt /sti/til/destination/
   ```

2. **Kopiere en fil og ændre navnet:**
   ```bash
   cp fil.txt ny_fil.txt
   ```

3. **Kopiere en mappe og dens indhold rekursivt:**
   ```bash
   cp -r mappe/ /sti/til/destination/
   ```

4. **Kopiere en fil med bekræftelse før overskrivning:**
   ```bash
   cp -i fil.txt /sti/til/destination/
   ```

5. **Kopiere kun nyere filer:**
   ```bash
   cp -u fil.txt /sti/til/destination/
   ```

## Tips
- Brug `-v`-muligheden for at få feedback om, hvilke filer der bliver kopieret, især når du arbejder med mange filer.
- Når du kopierer mapper, skal du altid bruge `-r` for at sikre, at alle underliggende filer og mapper også bliver kopieret.
- Vær forsigtig med `-i`-muligheden, da det kan bremse processen, hvis du kopierer mange filer og ofte skal bekræfte overskrivninger.