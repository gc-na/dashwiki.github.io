# [Nederlands] Debian Almquist Shell (dash) chgrp gebruik: Wijzig groepsbezit van bestanden

## Overzicht
De `chgrp`-opdracht wordt gebruikt om de groepsbezit van bestanden en mappen te wijzigen. Dit is handig wanneer je de toegang tot bestanden wilt beheren op basis van groepsrechten.

## Gebruik
De basis syntaxis van de `chgrp`-opdracht is als volgt:

```bash
chgrp [opties] [argumenten]
```

## Veelvoorkomende opties
- `-R`: Wijzig de groepsbezit van bestanden en mappen recursief.
- `-v`: Toon een uitvoer van de wijzigingen die zijn aangebracht.
- `--reference=BESTAND`: Stel de groepsbezit in op dezelfde als die van het opgegeven bestand.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `chgrp`-opdracht:

1. Wijzig de groepsbezit van een enkel bestand:
   ```bash
   chgrp gebruikers bestand.txt
   ```

2. Wijzig de groepsbezit van meerdere bestanden:
   ```bash
   chgrp gebruikers bestand1.txt bestand2.txt bestand3.txt
   ```

3. Wijzig de groepsbezit van een map en al zijn inhoud recursief:
   ```bash
   chgrp -R gebruikers /pad/naar/map
   ```

4. Wijzig de groepsbezit van een bestand naar dat van een referentiebestand:
   ```bash
   chgrp --reference=referentie.txt bestand.txt
   ```

## Tips
- Zorg ervoor dat je de juiste permissies hebt om de groepsbezit van een bestand te wijzigen.
- Gebruik de `-v` optie om te bevestigen welke bestanden zijn gewijzigd, vooral bij het gebruik van de recursieve optie.
- Controleer altijd de huidige groepsbezit met de `ls -l` opdracht voordat je wijzigingen aanbrengt.