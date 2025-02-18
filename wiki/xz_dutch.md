# [Nederlands] Debian Almquist Shell (dash) xz: Bestanden comprimeren en decomprimeren

## Overzicht
De `xz` opdracht wordt gebruikt om bestanden te comprimeren en decomprimeren met behulp van het LZMA-algoritme. Het biedt een hoge compressieverhouding en is ideaal voor het verkleinen van bestandsgrootte, wat opslagruimte bespaart en de overdracht van bestanden versnelt.

## Gebruik
De basis syntaxis van de `xz` opdracht is als volgt:

```bash
xz [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`, `--decompress`: Decomprimeer een bestand.
- `-k`, `--keep`: Houd het originele bestand na compressie of decompressie.
- `-f`, `--force`: Dwingt de opdracht om bestaande bestanden te overschrijven.
- `-z`, `--compress`: Comprimeer een bestand (standaard gedrag).
- `-9`: Gebruik de hoogste compressiegraad.

## Veelvoorkomende Voorbeelden
- Comprimeer een bestand:
    ```bash
    xz bestand.txt
    ```
- Decompressie van een bestand:
    ```bash
    xz -d bestand.txt.xz
    ```
- Comprimeer een bestand en behoud het origineel:
    ```bash
    xz -k bestand.txt
    ```
- Dwing compressie, zelfs als het bestand al bestaat:
    ```bash
    xz -f bestand.txt
    ```
- Comprimeer met de hoogste compressiegraad:
    ```bash
    xz -9 bestand.txt
    ```

## Tips
- Gebruik de `-k` optie als je het originele bestand wilt behouden voor toekomstig gebruik.
- Experimenteer met verschillende compressieniveaus om een balans te vinden tussen snelheid en bestandsgrootte.
- Controleer de grootte van de gecomprimeerde bestanden om te zien of de compressie de moeite waard is voor jouw specifieke bestanden.