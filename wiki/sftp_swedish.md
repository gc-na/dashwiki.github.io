# [Svenska] Debian Almquist Shell (dash) sftp användning: Överföring av filer över SSH

## Översikt
`sftp` (Secure File Transfer Protocol) är ett interaktivt verktyg som används för att överföra filer mellan en lokal och en fjärrserver över SSH. Det erbjuder en säker metod för filöverföring och hantering av filer på fjärrsystem.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
sftp [alternativ] [användare@värd]
```

## Vanliga alternativ
- `-P port`: Anger portnumret för SSH-anslutningen.
- `-o option`: Anger en specifik SSH-alternativ.
- `-b batchfile`: Använder en batchfil för att köra kommandon utan interaktivitet.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `sftp`:

1. Anslut till en fjärrserver:
   ```bash
   sftp användare@exempel.com
   ```

2. Ladda upp en fil till fjärrservern:
   ```bash
   put lokalfil.txt
   ```

3. Ladda ner en fil från fjärrservern:
   ```bash
   get fjärrfil.txt
   ```

4. Lista filer i den aktuella katalogen på fjärrservern:
   ```bash
   ls
   ```

5. Byt katalog på fjärrservern:
   ```bash
   cd /väg/till/katalog
   ```

## Tips
- Använd `-P` alternativet för att specificera en annan port om servern inte använder standardporten 22.
- För att avsluta `sftp` sessionen, skriv `bye` eller `exit`.
- För att överföra flera filer, kan du använda `mput` eller `mget` för att ladda upp eller ladda ner flera filer samtidigt.