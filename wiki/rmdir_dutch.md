# [Nederlands] Debian Almquist Shell (dash) rmdir gebruik: Verwijder lege mappen

## Overzicht
De `rmdir` opdracht wordt gebruikt om lege mappen te verwijderen. Als de map niet leeg is, zal de opdracht falen en een foutmelding geven.

## Gebruik
De basis syntaxis van de `rmdir` opdracht is als volgt:

```
rmdir [opties] [argumenten]
```

## Veelvoorkomende Opties
- `--ignore-fail-on-non-empty`: Negeert fouten als de map niet leeg is.
- `--parents`: Verwijdert ook lege bovenliggende mappen indien mogelijk.

## Veelvoorkomende Voorbeelden

1. **Verwijder een lege map**:
   ```bash
   rmdir mijnmap
   ```

2. **Verwijder meerdere lege mappen**:
   ```bash
   rmdir map1 map2 map3
   ```

3. **Verwijder een lege bovenliggende map**:
   ```bash
   rmdir --parents map1/map2
   ```

4. **Negeer fouten bij niet-lege mappen**:
   ```bash
   rmdir --ignore-fail-on-non-empty nietlege_map
   ```

## Tips
- Zorg ervoor dat de map leeg is voordat je `rmdir` gebruikt, anders krijg je een foutmelding.
- Gebruik de `--parents` optie om ook lege bovenliggende mappen te verwijderen, wat handig kan zijn om een hele structuur in één keer op te ruimen.
- Controleer altijd de inhoud van een map met `ls` voordat je deze verwijdert, om onbedoeld verlies van gegevens te voorkomen.