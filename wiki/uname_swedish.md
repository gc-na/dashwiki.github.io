# [Svenska] Debian Almquist Shell (dash) uname användning: Visa systeminformation

## Översikt
`uname` är ett kommando som används för att visa systeminformation om den aktuella maskinen och operativsystemet. Det kan ge detaljer som kärnversion, systemnamn och mer.

## Användning
Den grundläggande syntaxen för kommandot är:

```
uname [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar all tillgänglig systeminformation.
- `-s`: Visar systemnamnet.
- `-n`: Visar nätverksvärdnamnet.
- `-r`: Visar kärnversionen.
- `-v`: Visar versionsinformationen för kärnan.
- `-m`: Visar maskinens arkitektur.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `uname`:

1. Visa all systeminformation:
   ```sh
   uname -a
   ```

2. Visa endast systemnamnet:
   ```sh
   uname -s
   ```

3. Visa kärnversionen:
   ```sh
   uname -r
   ```

4. Visa maskinens arkitektur:
   ```sh
   uname -m
   ```

## Tips
- Använd `uname -a` för att få en snabb överblick över hela systemkonfigurationen.
- Kombinera `uname` med andra kommandon för att få mer detaljerad information om systemet.
- Kom ihåg att vissa alternativ kan variera beroende på systemets konfiguration och version av operativsystemet.