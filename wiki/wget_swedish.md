# [Svenska] Debian Almquist Shell (dash) wget användning: Ladda ner filer från webben

## Översikt
`wget` är ett kraftfullt kommandoradsverktyg som används för att ladda ner filer från webben. Det stödjer olika protokoll som HTTP, HTTPS och FTP, vilket gör det till ett mångsidigt verktyg för att hämta data från internet.

## Användning
Den grundläggande syntaxen för `wget` är:

```bash
wget [alternativ] [argument]
```

## Vanliga alternativ
- `-O [filnamn]`: Spara den nedladdade filen med det angivna filnamnet.
- `-c`: Fortsätt en avbruten nedladdning.
- `-q`: Tyst läge, ingen utdata visas.
- `--limit-rate=[hastighet]`: Begränsa nedladdningshastigheten.
- `-r`: Ladda ner filer rekursivt.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `wget`:

1. Ladda ner en fil från en URL:
   ```bash
   wget https://example.com/fil.zip
   ```

2. Spara filen med ett specifikt namn:
   ```bash
   wget -O nyfil.zip https://example.com/fil.zip
   ```

3. Fortsätt en avbruten nedladdning:
   ```bash
   wget -c https://example.com/fil.zip
   ```

4. Ladda ner en hel webbplats rekursivt:
   ```bash
   wget -r https://example.com
   ```

5. Begränsa nedladdningshastigheten:
   ```bash
   wget --limit-rate=200k https://example.com/fil.zip
   ```

## Tips
- Använd `-q` för att undvika att få mycket utdata om du bara vill ladda ner filer utan att se statusmeddelanden.
- Kontrollera alltid att du har rätt att ladda ner filer från en webbplats för att undvika eventuella juridiska problem.
- För stora filer, överväg att använda `-c` för att kunna återuppta nedladdningen om den avbryts.