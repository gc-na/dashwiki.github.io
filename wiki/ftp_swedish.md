# [Svenska] Debian Almquist Shell (dash) ftp användning: Överföra filer via FTP

## Översikt
Kommandot `ftp` används för att överföra filer mellan datorer via File Transfer Protocol (FTP). Det möjliggör både nedladdning och uppladdning av filer till och från en FTP-server.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
ftp [alternativ] [argument]
```

## Vanliga alternativ
- `-i`: Slå av interaktiv läge, vilket innebär att du inte kommer att bli tillfrågad om att bekräfta varje filöverföring.
- `-n`: Anslut utan att automatiskt logga in.
- `-v`: Aktivera detaljerad utdata, vilket visar mer information om överföringsprocessen.
- `-p`: Använd passiv överföring, vilket kan vara användbart om du har brandväggar som blockerar aktiva anslutningar.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `ftp`:

1. Ansluta till en FTP-server:
   ```bash
   ftp ftp.example.com
   ```

2. Logga in med ett användarnamn:
   ```bash
   ftp -n ftp.example.com
   user myusername mypassword
   ```

3. Ladda ner en fil från servern:
   ```bash
   get filnamn.txt
   ```

4. Ladda upp en fil till servern:
   ```bash
   put lokalfil.txt
   ```

5. Lista filer i den aktuella katalogen på servern:
   ```bash
   ls
   ```

## Tips
- Kontrollera alltid att du har rätt behörigheter för att ladda upp eller ladda ner filer.
- Använd `-i` alternativet för att snabba upp överföringar om du hanterar många filer.
- Om du har problem med anslutningen, prova att använda `-p` för passiv överföring.
- Tänk på att FTP inte krypterar data, så undvik att överföra känslig information utan att använda en säker metod som SFTP.