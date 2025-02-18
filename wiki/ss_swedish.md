# [Svenska] Debian Almquist Shell (dash) ss användning: Visa nätverksanslutningar

## Översikt
Kommandot `ss` används för att visa information om nätverksanslutningar, inklusive TCP, UDP och andra protokoll. Det är ett kraftfullt verktyg för att övervaka och felsöka nätverksanslutningar på systemet.

## Användning
Den grundläggande syntaxen för kommandot `ss` är:

```bash
ss [alternativ] [argument]
```

## Vanliga alternativ
- `-t`: Visa endast TCP-anslutningar.
- `-u`: Visa endast UDP-anslutningar.
- `-l`: Visa endast lyssnande anslutningar.
- `-p`: Visa processinformation som är kopplad till anslutningarna.
- `-n`: Visa numeriska adresser istället för att försöka lösa dem till namn.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `ss`:

1. Visa alla aktiva TCP-anslutningar:
   ```bash
   ss -t
   ```

2. Visa alla lyssnande UDP-anslutningar:
   ```bash
   ss -u -l
   ```

3. Visa alla anslutningar med processinformation:
   ```bash
   ss -p
   ```

4. Visa alla anslutningar och använd numeriska adresser:
   ```bash
   ss -n
   ```

5. Visa både TCP- och UDP-anslutningar:
   ```bash
   ss -t -u
   ```

## Tips
- Använd `ss -ltn` för att snabbt se vilka portar som lyssnar på TCP-anslutningar.
- Kombinera alternativ för att få mer specifik information, till exempel `ss -tunlp` för att se både TCP och UDP med processinformation.
- För att få en översikt över alla anslutningar kan du helt enkelt köra `ss` utan några alternativ.