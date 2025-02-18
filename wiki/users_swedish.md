# [Svenska] Debian Almquist Shell (dash) användare: Visa användarinformation

## Översikt
Kommandot `users` används för att visa namnen på de användare som för närvarande är inloggade på systemet. Det ger en snabb översikt över aktiva användarsessioner.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
users [alternativ]
```

## Vanliga alternativ
- `-n`: Visa endast användarnamn utan att inkludera extra information.
- `-r`: Visa endast användare som är inloggade på systemet.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `users`:

1. Visa alla inloggade användare:
   ```bash
   users
   ```

2. Visa inloggade användare utan extra information:
   ```bash
   users -n
   ```

3. Visa endast användare som är inloggade:
   ```bash
   users -r
   ```

## Tips
- Använd `users` i kombination med andra kommandon som `who` eller `w` för att få mer detaljerad information om användarsessioner.
- Kommandot är snabbt och effektivt för att få en översikt över aktiva användare, särskilt på servrar med flera användare.