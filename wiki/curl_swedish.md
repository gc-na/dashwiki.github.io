# [Svenska] Debian Almquist Shell (dash) curl användning: Hämta data från URL:er

## Översikt
`curl` är ett kommandoradsverktyg som används för att överföra data till eller från en server, med hjälp av olika protokoll som HTTP, HTTPS, FTP och mer. Det är ett kraftfullt verktyg för att hämta webbsidor, filer eller för att skicka data till en server.

## Användning
Den grundläggande syntaxen för `curl` är:

```bash
curl [alternativ] [argument]
```

## Vanliga alternativ
- `-O`: Spara filen med samma namn som den har på servern.
- `-L`: Följ omdirigeringar.
- `-d`: Skicka data med POST-förfrågningar.
- `-H`: Ange en HTTP-header.
- `-u`: Ange användarnamn och lösenord för autentisering.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `curl`:

1. Hämta en webbsida:
   ```bash
   curl https://www.example.com
   ```

2. Spara en fil med samma namn som på servern:
   ```bash
   curl -O https://www.example.com/file.zip
   ```

3. Följ omdirigeringar:
   ```bash
   curl -L https://bit.ly/example
   ```

4. Skicka data med en POST-förfrågan:
   ```bash
   curl -d "param1=value1&param2=value2" -X POST https://www.example.com/api
   ```

5. Ange en HTTP-header:
   ```bash
   curl -H "Authorization: Bearer token" https://www.example.com/protected
   ```

## Tips
- Använd `-v` för att få mer detaljerad information om förfrågan och svaret, vilket kan vara användbart för felsökning.
- Om du ofta använder samma alternativ, överväg att skapa en alias i din shell-konfiguration för att förenkla kommandot.
- Var försiktig med att skicka känslig information över HTTP; använd alltid HTTPS när det är möjligt för att skydda dina data.