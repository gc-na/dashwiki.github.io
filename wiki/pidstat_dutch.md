# [Nederlands] Debian Almquist Shell (dash) pidstat gebruik: Monitoren van processtatistieken

## Overzicht
Het `pidstat` commando is een hulpmiddel dat wordt gebruikt om de prestaties van processen in een Linux-systeem te monitoren. Het geeft gedetailleerde informatie over de CPU-gebruik, geheugen, en andere statistieken van actieve processen.

## Gebruik
De basis syntaxis van het `pidstat` commando is als volgt:

```bash
pidstat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toon de helpinformatie en beschikbare opties.
- `-r`: Toon geheugenstatistieken.
- `-u`: Toon CPU-gebruik.
- `-p <PID>`: Specificeer de proces-ID om te monitoren.
- `-t`: Toon statistieken voor threads.

## Veelvoorkomende Voorbeelden

1. **Basis CPU-gebruik weergeven:**
   ```bash
   pidstat
   ```

2. **CPU-gebruik van een specifiek proces (bijvoorbeeld PID 1234):**
   ```bash
   pidstat -p 1234
   ```

3. **Geheugenstatistieken weergeven:**
   ```bash
   pidstat -r
   ```

4. **Statistieken voor alle processen elke 2 seconden weergeven:**
   ```bash
   pidstat 2
   ```

5. **Statistieken voor threads van een specifiek proces:**
   ```bash
   pidstat -t -p 1234
   ```

## Tips
- Gebruik `pidstat` in combinatie met andere monitoringtools zoals `top` of `htop` voor een uitgebreider overzicht van systeembronnen.
- Experimenteer met verschillende opties om de meest relevante informatie voor uw situatie te verkrijgen.
- Overweeg om `pidstat` te automatiseren in scripts voor regelmatige monitoring van systeemprocessen.