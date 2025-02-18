# [Nederlands] Debian Almquist Shell (dash) jobs gebruik: Beheer achtergrondprocessen

## Overzicht
De `jobs`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om een lijst van actieve achtergrondprocessen te tonen die zijn gestart vanuit de huidige shell-sessie. Dit is handig voor het beheren van taken die op de achtergrond draaien, zodat je hun status kunt controleren en ze eventueel kunt hervatten of beëindigen.

## Gebruik
De basis syntaxis van de `jobs`-opdracht is als volgt:

```bash
jobs [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Toont de proces-ID (PID) van de achtergrondprocessen.
- `-n`: Toont alleen de jobs die recentelijk zijn gewijzigd.
- `-p`: Toont alleen de proces-ID's van de jobs.

## Veelvoorkomende voorbeelden

1. **Basis gebruik**: Toont een lijst van alle achtergrondprocessen.
    ```bash
    jobs
    ```

2. **Met proces-ID's**: Toont de achtergrondprocessen met hun respectieve PID's.
    ```bash
    jobs -l
    ```

3. **Recent gewijzigde jobs**: Toont alleen de jobs die recent zijn gewijzigd.
    ```bash
    jobs -n
    ```

4. **Alleen PID's**: Toont alleen de proces-ID's van de achtergrondprocessen.
    ```bash
    jobs -p
    ```

## Tips
- Zorg ervoor dat je regelmatig de `jobs`-opdracht gebruikt om een overzicht te krijgen van actieve achtergrondprocessen, vooral als je meerdere taken tegelijk uitvoert.
- Gebruik de `fg`-opdracht om een achtergrondtaak naar de voorgrond te brengen, en de `bg`-opdracht om een stopgezette taak opnieuw op de achtergrond te starten.
- Houd er rekening mee dat de status van de jobs alleen zichtbaar is binnen de shell-sessie waarin ze zijn gestart.