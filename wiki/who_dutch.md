# [Nederlands] Debian Almquist Shell (dash) who: toon ingelogde gebruikers

## Overzicht
De `who` opdracht in de Debian Almquist Shell (dash) toont een lijst van gebruikers die momenteel zijn ingelogd op het systeem. Het geeft informatie zoals de gebruikersnaam, terminal, inlogtijd en soms het IP-adres of de hostnaam van waaruit de gebruiker is ingelogd.

## Gebruik
De basis syntaxis van de `who` opdracht is als volgt:

```bash
who [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-b`: Toont de tijd van de laatste systeemopstart.
- `-H`: Toont de kolomnamen bovenaan de uitvoer.
- `-q`: Toont alleen de gebruikersnamen en het aantal ingelogde gebruikers.
- `--help`: Geeft een korte uitleg over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `who` opdracht:

1. **Basisgebruik**: Toon alle ingelogde gebruikers.
   ```bash
   who
   ```

2. **Toon de tijd van de laatste systeemopstart**:
   ```bash
   who -b
   ```

3. **Toon alleen de gebruikersnamen en het aantal ingelogde gebruikers**:
   ```bash
   who -q
   ```

4. **Toon de uitvoer met kolomnamen**:
   ```bash
   who -H
   ```

## Tips
- Gebruik `who` samen met andere opdrachten zoals `grep` om specifieke gebruikers te filteren.
- Combineer `who` met `wc -l` om het totale aantal ingelogde gebruikers te tellen:
  ```bash
  who | wc -l
  ```
- Houd er rekening mee dat `who` alleen informatie toont over gebruikers die daadwerkelijk zijn ingelogd, dus het kan nuttig zijn voor systeembeheer en monitoring.