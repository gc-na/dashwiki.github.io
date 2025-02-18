# [Svenska] Debian Almquist Shell (dash) who: visa inloggade användare

## Översikt
Kommandot `who` används för att visa en lista över användare som för närvarande är inloggade på systemet. Det ger information om användarnamn, terminal, inloggningstid och mer.

## Användning
Den grundläggande syntaxen för kommandot är:

```
who [alternativ] [argument]
```

## Vanliga alternativ
- `-b`: Visar den senaste systemstarten.
- `-q`: Visar en snabb översikt av inloggade användare.
- `-r`: Visar den aktuella runleveln för systemet.
- `--help`: Visar hjälpinformation för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `who`:

1. Visa alla inloggade användare:
   ```bash
   who
   ```

2. Visa den senaste systemstarten:
   ```bash
   who -b
   ```

3. Visa en snabb översikt av inloggade användare:
   ```bash
   who -q
   ```

4. Visa aktuell runlevel:
   ```bash
   who -r
   ```

## Tips
- Använd `who` regelbundet för att övervaka aktiva användare på systemet.
- Kombinera `who` med andra kommandon, som `grep`, för att filtrera resultaten.
- Tänk på att `who` endast visar användare som är inloggade via terminaler, så användare som är inloggade via grafiska gränssnitt kanske inte visas.