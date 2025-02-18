# [Svenska] Debian Almquist Shell (dash) netstat användning: Visa nätverksanslutningar

## Översikt
Kommandot `netstat` används för att visa nätverksanslutningar, routingtabeller och olika nätverksprotokollstatistik. Det är ett kraftfullt verktyg för att övervaka nätverksaktivitet och felsöka nätverksproblem.

## Användning
Den grundläggande syntaxen för `netstat` är:

```bash
netstat [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar alla anslutningar och lyssnande portar.
- `-t`: Visar TCP-anslutningar.
- `-u`: Visar UDP-anslutningar.
- `-n`: Visar adresser och portnummer i numerisk form istället för att försöka lösa dem till namn.
- `-l`: Visar endast lyssnande portar.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `netstat`:

1. Visa alla aktiva anslutningar:
   ```bash
   netstat -a
   ```

2. Visa endast TCP-anslutningar:
   ```bash
   netstat -t
   ```

3. Visa endast UDP-anslutningar:
   ```bash
   netstat -u
   ```

4. Visa lyssnande portar:
   ```bash
   netstat -l
   ```

5. Visa anslutningar med numeriska adresser:
   ```bash
   netstat -n
   ```

## Tips
- Använd `netstat -tuln` för att snabbt få en översikt över alla lyssnande TCP- och UDP-portar med numeriska adresser.
- Kombinera alternativ för att få mer specifik information, till exempel `netstat -at` för att se alla aktiva TCP-anslutningar.
- Tänk på att `netstat` kan kräva root-privilegier för att visa vissa typer av information, så använd `sudo` om det behövs.