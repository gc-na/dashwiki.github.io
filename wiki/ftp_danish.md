# [Danish] Debian Almquist Shell (dash) ftp brug: Overførsel af filer via FTP

## Oversigt
`ftp`-kommandoen bruges til at overføre filer mellem en lokal computer og en fjernserver ved hjælp af File Transfer Protocol (FTP). Det giver brugerne mulighed for at oprette forbindelse til en FTP-server, navigere i filsystemet og overføre filer frem og tilbage.

## Brug
Den grundlæggende syntaks for `ftp`-kommandoen er:

```bash
ftp [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`: Slukker for interaktiv mode, så filoverførsler sker uden bekræftelse.
- `-v`: Aktiverer detaljeret output, så du kan se, hvad der sker under overførslen.
- `-n`: Forhindrer automatisk login til FTP-serveren, hvilket kræver, at brugeren indtaster loginoplysninger manuelt.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `ftp`-kommandoen:

1. Opret forbindelse til en FTP-server:
   ```bash
   ftp ftp.example.com
   ```

2. Log ind med brugernavn og adgangskode:
   ```bash
   ftp> user myusername mypassword
   ```

3. Skift til en bestemt mappe på serveren:
   ```bash
   ftp> cd /path/to/directory
   ```

4. Download en fil fra serveren:
   ```bash
   ftp> get filename.txt
   ```

5. Upload en fil til serveren:
   ```bash
   ftp> put localfile.txt
   ```

6. Afslut FTP-sessionen:
   ```bash
   ftp> bye
   ```

## Tips
- Brug `-i` muligheden for at undgå bekræftelser ved store filoverførsler.
- Tjek altid, at du har de nødvendige tilladelser til at uploade eller downloade filer fra serveren.
- Overvej at bruge SFTP (Secure FTP) for en mere sikker filoverførsel, da `ftp` ikke krypterer data.