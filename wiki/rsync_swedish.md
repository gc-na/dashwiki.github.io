# [Svenska] Debian Almquist Shell (dash) rsync användning: Synkronisera filer och kataloger

## Översikt
Rsync är ett kraftfullt verktyg för att synkronisera filer och kataloger mellan olika platser, antingen lokalt eller över nätverket. Det är effektivt och kan spara bandbredd genom att endast överföra ändrade delar av filer.

## Användning
Den grundläggande syntaxen för rsync är:

```bash
rsync [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Arkivläge; kopierar filer och kataloger rekursivt och bevarar nästan alla attribut.
- `-v`: Verbos; visar detaljerad information om vad som kopieras.
- `-z`: Komprimera; komprimerar data under överföring för att spara bandbredd.
- `-r`: Rekursiv; kopierar kataloger rekursivt.
- `--delete`: Tar bort filer i destinationen som inte finns i källan.

## Vanliga exempel
Här är några praktiska exempel på hur man använder rsync:

1. **Kopiera en lokal katalog till en annan lokal katalog:**
   ```bash
   rsync -av /path/to/source/ /path/to/destination/
   ```

2. **Synkronisera en lokal katalog till en fjärrserver:**
   ```bash
   rsync -av /path/to/local/ user@remote:/path/to/remote/
   ```

3. **Kopiera filer och komprimera dem under överföring:**
   ```bash
   rsync -avz /path/to/source/ user@remote:/path/to/remote/
   ```

4. **Synkronisera och ta bort filer som inte finns i källan:**
   ```bash
   rsync -av --delete /path/to/source/ /path/to/destination/
   ```

## Tips
- Använd `-n` eller `--dry-run` för att simulera en rsync-operation utan att faktiskt kopiera några filer. Detta är användbart för att se vad som skulle hända.
- Se till att avsluta källsökvägen med en snedstreck (`/`) om du vill kopiera innehållet i katalogen snarare än själva katalogen.
- Kontrollera alltid att du har rätt behörigheter för både källan och destinationen för att undvika problem under överföringen.