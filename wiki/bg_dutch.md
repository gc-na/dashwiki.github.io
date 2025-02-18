# [Nederlands] Debian Almquist Shell (dash) bg gebruik: Zet een taak op de achtergrond

## Overzicht
De `bg`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om een taak die momenteel in de voorgrond draait, naar de achtergrond te verplaatsen. Dit stelt gebruikers in staat om andere opdrachten uit te voeren terwijl de achtergrondtaak doorgaat.

## Gebruik
De basis syntaxis van de `bg`-opdracht is als volgt:

```bash
bg [opties] [argumenten]
```

## Veelvoorkomende Opties
- **%job_spec**: Hiermee geef je de specifieke taak aan die je naar de achtergrond wilt verplaatsen. Dit kan een jobnummer of een jobnaam zijn.

## Veelvoorkomende Voorbeelden

1. **Een specifieke taak naar de achtergrond verplaatsen**:
   Als je een taak met jobnummer 1 hebt, kun je deze als volgt naar de achtergrond verplaatsen:
   ```bash
   bg %1
   ```

2. **Een taak die is gepauzeerd opnieuw starten in de achtergrond**:
   Als je een taak hebt gepauzeerd met `Ctrl+Z`, kun je deze opnieuw starten in de achtergrond met:
   ```bash
   bg
   ```

3. **Meerdere taken naar de achtergrond verplaatsen**:
   Je kunt ook meerdere taken naar de achtergrond verplaatsen door hun jobnummers op te geven:
   ```bash
   bg %1 %2
   ```

## Tips
- Zorg ervoor dat je de juiste jobnummers gebruikt; je kunt de actieve taken bekijken met de `jobs`-opdracht.
- Houd er rekening mee dat achtergrondtaken mogelijk niet kunnen communiceren met de terminal zoals voorgrondtaken dat doen.
- Gebruik de `fg`-opdracht om een achtergrondtaak weer naar de voorgrond te brengen als je deze weer wilt bedienen.