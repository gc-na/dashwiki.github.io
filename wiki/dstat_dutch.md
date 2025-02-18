# [Nederlands] Debian Almquist Shell (dash) dstat gebruik: systeemmonitoring in real-time

## Overzicht
De `dstat`-opdracht is een veelzijdig hulpprogramma voor systeemmonitoring dat informatie over systeembronnen in real-time kan weergeven. Het combineert de functionaliteit van verschillende andere tools en biedt een gedetailleerd overzicht van de prestaties van uw systeem.

## Gebruik
De basis syntaxis van de `dstat`-opdracht is als volgt:

```bash
dstat [opties] [argumenten]
```

## Veelvoorkomende opties
Hier zijn enkele veelvoorkomende opties die u kunt gebruiken met `dstat`:

- `-c`: Toon CPU-gebruik.
- `-d`: Toon schijfactiviteit.
- `-n`: Toon netwerkactiviteit.
- `-r`: Toon geheugengebruik.
- `-t`: Toon tijdstempels bij de uitvoer.
- `--help`: Toon hulpinformatie over het gebruik van dstat.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `dstat`:

1. **Basisgebruik**: Toon standaard systeemstatistieken.
   ```bash
   dstat
   ```

2. **CPU- en geheugenmonitoring**: Toon CPU- en geheugenstatistieken.
   ```bash
   dstat -c -r
   ```

3. **Schijf- en netwerkactiviteit**: Toon schijf- en netwerkactiviteit.
   ```bash
   dstat -d -n
   ```

4. **Met tijdstempels**: Toon systeemstatistieken met tijdstempels.
   ```bash
   dstat -t
   ```

5. **Gecombineerde statistieken**: Toon CPU-, schijf- en netwerkstatistieken.
   ```bash
   dstat -c -d -n
   ```

## Tips
- Gebruik `dstat` in combinatie met andere monitoringtools voor een uitgebreider overzicht van uw systeem.
- Experimenteer met verschillende opties om de meest relevante informatie voor uw situatie te verkrijgen.
- Overweeg om `dstat` te gebruiken in een script voor geautomatiseerde monitoring van systeembronnen.