# [Svenska] Debian Almquist Shell (dash) id användning: visa användar- och gruppinformation

## Översikt
Kommandot `id` används för att visa användarens identitet, inklusive användarens UID (User ID), GID (Group ID) och de grupper som användaren tillhör. Det är ett enkelt men kraftfullt verktyg för att få information om användarkonton i systemet.

## Användning
Den grundläggande syntaxen för kommandot `id` är:

```
id [alternativ] [argument]
```

## Vanliga alternativ
- `-u`: Visa endast användarens UID.
- `-g`: Visa endast användarens GID.
- `-G`: Visa alla grupper som användaren tillhör.
- `-n`: Visa namn istället för ID för användare eller grupper.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `id`:

1. Visa information om den aktuella användaren:
   ```sh
   id
   ```

2. Visa endast användarens UID:
   ```sh
   id -u
   ```

3. Visa endast användarens GID:
   ```sh
   id -g
   ```

4. Visa alla grupper som den aktuella användaren tillhör:
   ```sh
   id -G
   ```

5. Visa information om en specifik användare (t.ex. "username"):
   ```sh
   id username
   ```

## Tips
- Använd `id -n` tillsammans med `-u` eller `-g` för att få namn istället för numeriska ID:n, vilket kan vara mer läsbart.
- Om du är osäker på vilken användare du är inloggad som, kan du helt enkelt köra `id` utan några alternativ för att få en översikt över din identitet.
- Kommandot `id` kan vara användbart i skript för att kontrollera användar- och gruppbehörigheter innan du utför åtgärder som kräver specifika rättigheter.