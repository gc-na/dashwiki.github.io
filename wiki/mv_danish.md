# [Danish] Debian Almquist Shell (dash) mv Brug: Flyt eller omdøb filer og mapper

## Oversigt
`mv`-kommandoen bruges til at flytte eller omdøbe filer og mapper i Unix-lignende operativsystemer, herunder Debian Almquist Shell (dash). Den giver brugerne mulighed for at ændre placeringen af en fil eller mappe eller ændre dens navn.

## Brug
Den grundlæggende syntaks for `mv`-kommandoen er som følger:

```bash
mv [muligheder] [kildesti] [destinationssti]
```

## Almindelige muligheder
- `-i`: Spørg om bekræftelse, før en eksisterende destination overskrives.
- `-u`: Flyt kun, hvis kildestien er nyere end destinationsstien eller hvis destinationsstien ikke eksisterer.
- `-v`: Vis detaljer om, hvad der bliver flyttet eller omdøbt.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `mv`-kommandoen kan bruges:

1. **Flyt en fil til en ny placering:**
   ```bash
   mv fil.txt /sti/til/ny/mappe/
   ```

2. **Omdøb en fil:**
   ```bash
   mv gammel_fil.txt ny_fil.txt
   ```

3. **Flyt flere filer til en mappe:**
   ```bash
   mv fil1.txt fil2.txt /sti/til/mappe/
   ```

4. **Brug af -i mulighed for at undgå overskrivning:**
   ```bash
   mv -i fil.txt /sti/til/ny/mappe/
   ```

5. **Brug af -u mulighed for kun at flytte nyere filer:**
   ```bash
   mv -u fil.txt /sti/til/ny/mappe/
   ```

## Tips
- Brug `-v` muligheden for at få feedback om, hvad der bliver flyttet; det kan være nyttigt til fejlfinding.
- Vær forsigtig med at bruge `mv` uden bekræftelse, da det kan overskrive eksisterende filer uden advarsel.
- Overvej at bruge `-i` muligheden, hvis du arbejder med vigtige filer, for at undgå utilsigtet tab af data.