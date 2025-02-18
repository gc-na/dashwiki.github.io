# [Svenska] Debian Almquist Shell (dash) netcat användning: nätverkskommunikation och felsökning

## Översikt
Netcat, ofta kallad "schweizisk armékniv" för nätverksprotokoll, är ett kraftfullt verktyg för att läsa och skriva data över nätverksanslutningar. Det kan användas för att skapa TCP- eller UDP-anslutningar, vilket gör det användbart för både felsökning och dataöverföring.

## Användning
Den grundläggande syntaxen för netcat är:

```
netcat [alternativ] [argument]
```

## Vanliga alternativ
- `-l`: Lyssna på en port för inkommande anslutningar.
- `-p [port]`: Specifiera portnumret som ska användas.
- `-u`: Använd UDP istället för TCP.
- `-v`: Aktivera detaljerad (verbose) utdata.
- `-z`: Skanna portar utan att skicka data (zero-I/O mode).

## Vanliga exempel
Här är några praktiska exempel på hur man använder netcat:

### 1. Skapa en enkel server
För att starta en server som lyssnar på port 1234:
```bash
netcat -l -p 1234
```

### 2. Ansluta till en server
För att ansluta till en server på port 1234:
```bash
netcat [server_ip] 1234
```

### 3. Skicka en fil
För att skicka en fil från en maskin till en annan:
På mottagande maskin:
```bash
netcat -l -p 1234 > mottagen_fil.txt
```
På avsändande maskin:
```bash
netcat [mottagar_ip] 1234 < fil_att_skicka.txt
```

### 4. Portskanning
För att skanna en server för öppna portar:
```bash
netcat -z -v [server_ip] 1-1000
```

## Tips
- Använd `-v` för att få mer information om anslutningar och överföringar.
- Var försiktig med att använda netcat över osäkra nätverk, eftersom data inte är krypterad.
- Netcat kan även användas för att skapa en enkel chattapplikation genom att koppla samman två terminaler.