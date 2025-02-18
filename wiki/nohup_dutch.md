# [Nederlands] Debian Almquist Shell (dash) nohup gebruik: Voorkomt dat een proces wordt beëindigd bij uitloggen

## Overzicht
De `nohup` (no hang up) opdracht in de Debian Almquist Shell (dash) wordt gebruikt om een proces uit te voeren dat niet wordt beëindigd wanneer de gebruiker uitlogt of de terminal sluit. Dit is bijzonder nuttig voor lange taken die je wilt laten draaien zonder dat je ingelogd blijft.

## Gebruik
De basis syntaxis van de `nohup` opdracht is als volgt:

```bash
nohup [opties] [argumenten]
```

## Veelvoorkomende opties
- `&`: Voert het proces op de achtergrond uit.
- `-h`: Toont de helpinformatie voor de `nohup` opdracht.
- `-v`: Geeft de versie-informatie van de `nohup` opdracht weer.

## Veelvoorkomende voorbeelden

1. **Een script op de achtergrond uitvoeren**:
   ```bash
   nohup ./mijn_script.sh &
   ```

2. **Een lange opdracht uitvoeren en de uitvoer naar een bestand sturen**:
   ```bash
   nohup lange_opdracht > uitvoer.log &
   ```

3. **Een Python-script uitvoeren zonder dat het stopt bij uitloggen**:
   ```bash
   nohup python3 mijn_script.py &
   ```

4. **Een opdracht uitvoeren en zowel standaarduitvoer als foutuitvoer naar een bestand sturen**:
   ```bash
   nohup mijn_opdracht > uitvoer.log 2>&1 &
   ```

## Tips
- Gebruik altijd `&` om het proces op de achtergrond te laten draaien, zodat je de terminal kunt blijven gebruiken.
- Controleer de uitvoer van je processen door de logbestanden te bekijken die je hebt opgegeven.
- Wees voorzichtig met het uitvoeren van processen die veel systeembronnen vereisen, aangezien deze op de achtergrond kunnen blijven draaien zonder dat je ze in de gaten houdt.