# [Nederlands] Debian Almquist Shell (dash) wget gebruik: Een tool voor het downloaden van bestanden

## Overzicht
De `wget`-opdracht is een krachtige tool die wordt gebruikt om bestanden van het internet te downloaden. Het ondersteunt verschillende protocollen, waaronder HTTP, HTTPS en FTP, en kan worden gebruikt om zowel enkele bestanden als hele websites te downloaden.

## Gebruik
De basis syntaxis van de `wget`-opdracht is als volgt:

```bash
wget [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties die je kunt gebruiken met `wget`:

- `-O [bestandsnaam]`: Hiermee kun je de naam van het gedownloade bestand specificeren.
- `-q`: Voert de opdracht uit in stille modus, zonder output naar de terminal.
- `-c`: Hervat een onderbroken download.
- `-r`: Download bestanden recursief, wat handig is voor het downloaden van hele websites.
- `--limit-rate=[snelheid]`: Beperk de downloadsnelheid tot een bepaalde waarde.

## Veelvoorkomende Voorbeelden

Hier zijn enkele praktische voorbeelden van het gebruik van `wget`:

1. Een enkel bestand downloaden:
   ```bash
   wget https://example.com/bestand.zip
   ```

2. Een bestand downloaden met een specifieke naam:
   ```bash
   wget -O nieuwe_naam.zip https://example.com/bestand.zip
   ```

3. Een onderbroken download hervatten:
   ```bash
   wget -c https://example.com/bestand.zip
   ```

4. Een hele website downloaden:
   ```bash
   wget -r https://example.com
   ```

5. De downloadsnelheid beperken:
   ```bash
   wget --limit-rate=200k https://example.com/bestand.zip
   ```

## Tips
- Gebruik de `-q` optie als je de output wilt minimaliseren, vooral bij automatische scripts.
- Combineer de `-c` optie met `-r` om een onderbroken recursieve download te hervatten.
- Controleer altijd de rechten en de gebruiksvoorwaarden van de website voordat je bestanden downloadt.