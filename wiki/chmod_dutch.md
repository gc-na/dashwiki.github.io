# [Nederlands] Debian Almquist Shell (dash) chmod gebruik: Bestanden en mappen machtigingen beheren

## Overzicht
De `chmod`-opdracht wordt gebruikt om de bestandspermissies van bestanden en mappen in een Unix-achtige omgeving te wijzigen. Hiermee kun je bepalen wie toegang heeft tot een bestand en welke acties ze kunnen uitvoeren, zoals lezen, schrijven of uitvoeren.

## Gebruik
De basis syntaxis van de `chmod`-opdracht is als volgt:

```bash
chmod [opties] [argumenten]
```

## Veelvoorkomende opties
- `-R`: Wijzig de permissies recursief voor alle bestanden en submappen in de opgegeven map.
- `-v`: Toon een uitvoer voor elke wijziging die is aangebracht.
- `-c`: Toon alleen de bestanden waarvan de permissies zijn gewijzigd.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `chmod`:

1. **Geef de eigenaar lees-, schrijf- en uitvoerrechten:**
   ```bash
   chmod 700 bestand.txt
   ```

2. **Geef de eigenaar lees- en uitvoerrechten, en de groep alleen leesrechten:**
   ```bash
   chmod 740 bestand.txt
   ```

3. **Geef iedereen leesrechten:**
   ```bash
   chmod a+r bestand.txt
   ```

4. **Verander de permissies van een map en al zijn inhoud recursief:**
   ```bash
   chmod -R 755 /pad/naar/map
   ```

5. **Toon welke bestanden zijn gewijzigd:**
   ```bash
   chmod -cv 644 bestand.txt
   ```

## Tips
- Wees voorzichtig met het geven van uitvoerrechten (`x`) aan bestanden, vooral als ze scripts zijn, om veiligheidsrisico's te vermijden.
- Gebruik de `-R` optie met zorg, omdat het alle bestanden en submappen in de opgegeven map beïnvloedt.
- Controleer altijd de huidige permissies met `ls -l` voordat je wijzigingen aanbrengt, zodat je weet wat je wijzigt.