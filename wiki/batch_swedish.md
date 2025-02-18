# [Svenska] Debian Almquist Shell (dash) batch användning: kör kommandon i bakgrunden

## Översikt
`batch`-kommandot används för att schemalägga kommandon som ska köras vid en senare tidpunkt, när systemet är mindre belastat. Det är särskilt användbart för att köra resurskrävande uppgifter utan att påverka användarens interaktion med systemet.

## Användning
Den grundläggande syntaxen för `batch`-kommandot är:

```bash
batch [options] [arguments]
```

## Vanliga alternativ
- `-f`: Anger en fil som innehåller kommandon att köra.
- `-h`: Visar hjälpinformation om kommandot.
- `-q`: Tystar utdata; inga meddelanden skrivs till terminalen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `batch`:

1. **Köra ett enkelt kommando**:
   För att köra ett kommando som `echo` vid en senare tidpunkt, skriv:
   ```bash
   echo "Detta körs senare" | batch
   ```

2. **Köra flera kommandon**:
   Du kan också köra flera kommandon genom att använda en semikolon:
   ```bash
   (echo "Första kommandot"; echo "Andra kommandot") | batch
   ```

3. **Använda en fil med kommandon**:
   Om du har en fil som heter `kommandon.txt` med kommandon, kan du köra dem med:
   ```bash
   batch < kommandon.txt
   ```

## Tips
- Kontrollera systemets belastning innan du schemalägger tunga uppgifter för att säkerställa att de körs effektivt.
- Använd `at`-kommandot om du vill schemalägga kommandon för en specifik tid istället för att vänta på låg belastning.
- Håll dina kommandon i en fil för enklare hantering och återanvändning.