# [Svenska] Debian Almquist Shell (dash) mkdir användning: Skapa kataloger

## Översikt
`mkdir` är ett kommando som används för att skapa nya kataloger i filsystemet. Det är en grundläggande funktion i Unix-liknande operativsystem, inklusive Debian Almquist Shell (dash).

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
mkdir [alternativ] [argument]
```

## Vanliga alternativ
- `-p`: Skapar föräldrakataloger om de inte redan finns.
- `-m`: Sätter behörigheterna för den skapade katalogen.
- `--help`: Visar hjälpinformation om kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mkdir`:

1. Skapa en enkel katalog:
   ```bash
   mkdir min_katalog
   ```

2. Skapa flera kataloger samtidigt:
   ```bash
   mkdir katalog1 katalog2 katalog3
   ```

3. Skapa en katalog med föräldrakataloger:
   ```bash
   mkdir -p förälder/barn
   ```

4. Skapa en katalog med specifika behörigheter:
   ```bash
   mkdir -m 755 skyddad_katalog
   ```

## Tips
- Använd `-p` alternativet för att undvika fel om föräldrakataloger redan finns.
- Kontrollera behörigheterna efter att du har skapat en katalog för att säkerställa att de är korrekta.
- Använd `--help` för att få mer information om tillgängliga alternativ och användning.