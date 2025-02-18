# [Danish] Debian Almquist Shell (dash) chmod brug: Ændrer filrettigheder

## Oversigt
`chmod`-kommandoen bruges til at ændre fil- og mappetilladelser i Unix-lignende operativsystemer. Den giver brugerne mulighed for at kontrollere, hvem der kan læse, skrive eller udføre en fil.

## Brug
Den grundlæggende syntaks for `chmod`-kommandoen er:

```bash
chmod [muligheder] [argumenter]
```

## Almindelige muligheder
- `-R`: Ændrer tilladelser rekursivt for alle filer og undermapper i en mappe.
- `u`: Refererer til ejeren af filen (user).
- `g`: Refererer til gruppen af ejeren (group).
- `o`: Refererer til andre brugere (others).
- `r`: Giver læsetilladelse (read).
- `w`: Giver skrivetilladelse (write).
- `x`: Giver udførelsestilladelse (execute).
- `+`: Tilføjer en tilladelse.
- `-`: Fjerner en tilladelse.
- `=`: Sætter tilladelsen til en bestemt værdi.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `chmod`:

1. **Giv ejeren læse- og skrivetilladelse:**
   ```bash
   chmod u+rw fil.txt
   ```

2. **Fjern udførelsestilladelse for andre:**
   ```bash
   chmod o-x fil.txt
   ```

3. **Giv alle brugere læse- og udførelsestilladelse:**
   ```bash
   chmod a+rx fil.txt
   ```

4. **Ændre tilladelser rekursivt for en mappe:**
   ```bash
   chmod -R u+rwX mappe/
   ```

5. **Sæt specifikke tilladelser (læs, skriv, udfør) for ejer, gruppe og andre:**
   ```bash
   chmod 755 fil.txt
   ```

## Tips
- Brug `chmod -R` med forsigtighed, da det ændrer tilladelser for alle filer og mapper inden for den angivne mappe.
- Tjek filrettighederne efter ændringer ved at bruge `ls -l` for at sikre, at de er indstillet korrekt.
- Overvej at bruge numeriske tilladelser (f.eks. 755) for hurtigere og mere præcise ændringer.