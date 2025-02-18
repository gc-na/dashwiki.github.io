# [Nederlands] Debian Almquist Shell (dash) sftp gebruik: Bestanden veilig overdragen

## Overzicht
De `sftp` (Secure File Transfer Protocol) opdracht wordt gebruikt om bestanden veilig over te dragen tussen een lokale en een externe computer via SSH (Secure Shell). Het biedt een veilige manier om bestanden te verzenden en ontvangen.

## Gebruik
De basis syntaxis van de `sftp` opdracht is als volgt:

```bash
sftp [opties] [gebruikersnaam@]host
```

## Veelvoorkomende opties
- `-P port`: Specificeert de poort die gebruikt moet worden voor de verbinding.
- `-o option`: Geeft een specifieke SSH-optie op.
- `-b batchfile`: Voert opdrachten uit vanuit een batchbestand.

## Veelvoorkomende voorbeelden

1. Verbinden met een externe server:
   ```bash
   sftp gebruiker@voorbeeld.com
   ```

2. Verbinden met een specifieke poort:
   ```bash
   sftp -P 2222 gebruiker@voorbeeld.com
   ```

3. Bestanden uploaden naar de server:
   ```bash
   put lokaal_bestand.txt
   ```

4. Bestanden downloaden van de server:
   ```bash
   get server_bestand.txt
   ```

5. Een hele map uploaden:
   ```bash
   put -r lokale_map
   ```

## Tips
- Zorg ervoor dat je SSH-toegang hebt tot de server voordat je `sftp` gebruikt.
- Gebruik de `-b` optie om een batchbestand te maken voor geautomatiseerde overdrachten.
- Controleer altijd de bestandsrechten op de server om ervoor te zorgen dat je de juiste toegang hebt.