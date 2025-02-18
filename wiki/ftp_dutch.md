# [Nederlands] Debian Almquist Shell (dash) ftp gebruik: Bestanden overdragen via het FTP-protocol

## Overzicht
Het `ftp`-commando wordt gebruikt om bestanden over te dragen via het File Transfer Protocol (FTP). Hiermee kunnen gebruikers verbinding maken met FTP-servers om bestanden te uploaden of te downloaden.

## Gebruik
De basis syntaxis van het `ftp`-commando is als volgt:

```bash
ftp [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-v`: Verbose modus, toont meer details over de verbinding.
- `-n`: Voorkomt dat ftp automatisch inlogt bij de server.
- `-p`: Gebruik passieve modus voor de verbinding.
- `-g`: Schakel globbing uit (wildcard-ondersteuning).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van het `ftp`-commando:

1. Verbinden met een FTP-server:
   ```bash
   ftp ftp.example.com
   ```

2. Verbinden zonder automatisch inloggen:
   ```bash
   ftp -n ftp.example.com
   ```

3. Bestanden downloaden van de server:
   ```bash
   get bestand.txt
   ```

4. Bestanden uploaden naar de server:
   ```bash
   put lokaal_bestand.txt
   ```

5. Een lijst van bestanden op de server weergeven:
   ```bash
   ls
   ```

## Tips
- Gebruik de `-v` optie om meer informatie te krijgen over de verbinding, wat nuttig kan zijn voor het oplossen van problemen.
- Zorg ervoor dat je de juiste inloggegevens hebt voordat je verbinding maakt met de server.
- Overweeg om een veilige variant van FTP, zoals SFTP, te gebruiken voor gevoelige gegevensoverdracht.