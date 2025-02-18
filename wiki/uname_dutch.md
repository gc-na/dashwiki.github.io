# [Nederlands] Debian Almquist Shell (dash) uname gebruik: Toon systeeminformatie

## Overzicht
De `uname`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om informatie over het systeem weer te geven. Dit omvat details zoals de naam van het besturingssysteem, de kernelversie en andere relevante systeeminformatie.

## Gebruik
De basis syntaxis van de `uname`-opdracht is als volgt:

```bash
uname [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelvoorkomende opties die je kunt gebruiken met de `uname`-opdracht:

- `-a`: Toont alle beschikbare systeeminformatie.
- `-s`: Toont de naam van het besturingssysteem.
- `-n`: Toont de netwerknaam van de host.
- `-r`: Toont de kernelversie.
- `-v`: Toont de versie van de kernel.
- `-m`: Toont het machine-type (bijvoorbeeld x86_64).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `uname`-opdracht:

1. Toon alle systeeminformatie:
   ```bash
   uname -a
   ```

2. Toon alleen de naam van het besturingssysteem:
   ```bash
   uname -s
   ```

3. Toon de kernelversie:
   ```bash
   uname -r
   ```

4. Toon het machine-type:
   ```bash
   uname -m
   ```

## Tips
- Gebruik `uname -a` voor een snelle en uitgebreide weergave van alle systeeminformatie.
- Combineer `uname` met andere commando's in scripts om systeeminformatie dynamisch te gebruiken.
- Controleer regelmatig de kernelversie met `uname -r` om ervoor te zorgen dat je systeem up-to-date is.