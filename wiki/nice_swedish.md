# [Svenska] Debian Almquist Shell (dash) nice användning: Justera processprioritet

## Översikt
Kommandot `nice` används för att starta ett program med en modifierad prioritet. Det gör att användare kan styra hur mycket CPU-resurser ett program får i förhållande till andra processer. Genom att använda `nice` kan man förhindra att ett program tar över systemresurserna, vilket är särskilt användbart när man kör resurskrävande uppgifter.

## Användning
Den grundläggande syntaxen för `nice` är:

```bash
nice [alternativ] [kommando] [argument]
```

## Vanliga alternativ
- `-n, --adjustment <värde>`: Anger hur mycket prioriteten ska justeras. Värdet kan vara mellan -20 (högre prioritet) och 19 (lägre prioritet).
- `-h, --help`: Visar hjälpinformation om kommandot.
- `--version`: Visar versionsinformation för `nice`.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `nice`:

1. Starta ett program med standardprioritet:
   ```bash
   nice my_program
   ```

2. Starta ett program med lägre prioritet (19):
   ```bash
   nice -n 19 my_program
   ```

3. Starta ett program med högre prioritet (-10):
   ```bash
   nice -n -10 my_program
   ```

4. Använd `nice` för att köra en långvarig process i bakgrunden:
   ```bash
   nice -n 15 long_running_task &
   ```

## Tips
- Använd `nice` när du kör tunga skript eller program som inte är tidskritiska för att undvika att påverka systemets responsivitet.
- Kom ihåg att endast användare med tillräckliga rättigheter kan öka prioriteten för processer (använda negativa värden).
- Kontrollera prioriteten för en körande process med kommandot `ps` för att se hur `nice` påverkar den.