# [Svenska] Debian Almquist Shell (dash) logout användning: Avsluta en session

## Översikt
Kommandot `logout` används för att avsluta en användarsession i en skalmiljö. Det är särskilt användbart när du arbetar i en terminal och vill logga ut från den aktuella sessionen.

## Användning
Den grundläggande syntaxen för kommandot är:

```
logout [options] [arguments]
```

## Vanliga alternativ
`logout` har inga specifika alternativ, men det kan användas i olika sammanhang beroende på vilken typ av skal du arbetar i.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `logout`:

1. **Avsluta en interaktiv session:**
   Om du är inloggad i en terminal och vill logga ut, skriver du helt enkelt:
   ```sh
   logout
   ```

2. **Avsluta en session i en sub-shell:**
   Om du har startat en sub-shell med ett kommando som `sh`, kan du logga ut från den med:
   ```sh
   sh
   logout
   ```

3. **Avsluta en SSH-session:**
   När du är inloggad på en fjärrserver via SSH kan du logga ut genom att skriva:
   ```sh
   logout
   ```

## Tips
- Använd `exit` istället för `logout` om du vill avsluta en session i ett skript eller en sub-shell, eftersom `exit` är mer allmänt tillämpligt.
- Se till att spara ditt arbete innan du loggar ut, eftersom alla öppna program och sessioner stängs.
- Om du arbetar med flera terminalfönster, kom ihåg att `logout` endast stänger den aktuella terminalsessionen.