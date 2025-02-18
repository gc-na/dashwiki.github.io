# [Danish] Debian Almquist Shell (dash) sftp brug: Overførsel af filer sikkert

## Oversigt
`sftp` (Secure File Transfer Protocol) er en netværksprotokol, der bruges til at overføre filer sikkert mellem en lokal og en fjerncomputer. Det fungerer over SSH (Secure Shell), hvilket giver en krypteret forbindelse, der beskytter data under overførslen.

## Brug
Den grundlæggende syntaks for `sftp`-kommandoen er:

```bash
sftp [muligheder] [bruger@værtsnavn]
```

## Almindelige muligheder
- `-P` : Angiv portnummeret, hvis det er forskelligt fra standardporten (22).
- `-o` : Angiv specifikke SSH-indstillinger, f.eks. `-o StrictHostKeyChecking=no`.
- `-b` : Angiv en batchfil, der indeholder SFTP-kommandoer.

## Almindelige eksempler
1. Opret forbindelse til en fjernserver:
   ```bash
   sftp bruger@eksempel.com
   ```

2. Overfør en fil fra den lokale maskine til fjernserveren:
   ```bash
   sftp bruger@eksempel.com
   put lokal_fil.txt
   ```

3. Download en fil fra fjernserveren til den lokale maskine:
   ```bash
   sftp bruger@eksempel.com
   get fjern_fil.txt
   ```

4. Liste filer i den aktuelle fjernmappe:
   ```bash
   sftp bruger@eksempel.com
   ls
   ```

5. Skift til en anden mappe på fjernserveren:
   ```bash
   sftp bruger@eksempel.com
   cd /sti/til/mappe
   ```

## Tips
- Brug `-P` til at angive en anden port, hvis din server ikke bruger standardporten 22.
- Overvej at bruge en SSH-nøgle til autentificering for at gøre forbindelsen mere sikker og praktisk.
- For batchoperationer kan du bruge `-b` til at automatisere filoverførsler med en liste over kommandoer.