# [Svenska] Debian Almquist Shell (dash) iotop användning: övervaka disk I/O-användning

## Översikt
Kommandot `iotop` används för att övervaka och visa disk I/O-användning av processer i realtid. Det ger en översikt över vilka processer som använder mest diskresurser, vilket kan vara användbart för att identifiera flaskhalsar och optimera systemprestanda.

## Användning
Den grundläggande syntaxen för `iotop` är:

```bash
iotop [alternativ] [argument]
```

## Vanliga alternativ
- `-o`, `--only`: Visa endast processer som använder I/O.
- `-b`, `--batch`: Kör i batch-läge, vilket är användbart för att logga utdata till en fil.
- `-d`, `--delay`: Ange fördröjning mellan uppdateringar i sekunder (standard är 1 sekund).
- `-p`, `--pid`: Visa endast processer med angivet process-ID.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `iotop`:

1. Visa alla processer som använder I/O:
   ```bash
   iotop
   ```

2. Visa endast processer som använder I/O:
   ```bash
   iotop -o
   ```

3. Kör `iotop` i batch-läge med en fördröjning på 2 sekunder:
   ```bash
   iotop -b -d 2
   ```

4. Visa I/O-användning för en specifik process med PID 1234:
   ```bash
   iotop -p 1234
   ```

## Tips
- Använd `iotop` med `sudo` för att få fullständig information om alla processer, eftersom vissa processer kan vara dolda för vanliga användare.
- Tänk på att `iotop` kan påverka systemets prestanda något, så använd det sparsamt på produktionssystem.
- Kombinera `iotop` med andra verktyg som `htop` för en mer omfattande systemövervakning.