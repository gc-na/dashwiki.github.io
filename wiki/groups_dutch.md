# [Nederlands] Debian Almquist Shell (dash) groepen gebruik: Groepen van gebruikers weergeven

## Overzicht
De `groups` opdracht in de Debian Almquist Shell (dash) toont de groepen waartoe een gebruiker behoort. Dit kan nuttig zijn voor systeembeheerders en gebruikers die hun toegangsrechten willen controleren.

## Gebruik
De basis syntaxis van de `groups` opdracht is als volgt:

```bash
groups [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`, `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `-v`, `--version`: Toont de versie van de `groups` opdracht.

## Veelvoorkomende Voorbeelden

1. **Toon de groepen van de huidige gebruiker:**

   ```bash
   groups
   ```

2. **Toon de groepen van een specifieke gebruiker:**

   ```bash
   groups gebruikersnaam
   ```

3. **Gebruik de helpoptie om informatie te krijgen:**

   ```bash
   groups --help
   ```

4. **Controleer de versie van de `groups` opdracht:**

   ```bash
   groups --version
   ```

## Tips
- Gebruik `groups` zonder argumenten om snel te controleren tot welke groepen je zelf behoort.
- Voor systeembeheerders is het handig om de groepen van andere gebruikers te controleren om toegangsrechten te beheren.
- Combineer de `groups` opdracht met andere commando's zoals `id` voor meer gedetailleerde informatie over gebruikers en hun rechten.