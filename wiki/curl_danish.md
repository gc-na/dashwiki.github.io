# [Danish] Debian Almquist Shell (dash) curl brug: Hent data fra en URL

## Oversigt
`curl` er et kommandolinjeværktøj, der bruges til at overføre data til eller fra en server ved hjælp af forskellige protokoller, herunder HTTP, HTTPS, FTP og mange flere. Det er et nyttigt værktøj til at hente indhold fra internettet eller sende data til en server.

## Brug
Den grundlæggende syntaks for `curl`-kommandoen er som følger:

```bash
curl [muligheder] [argumenter]
```

## Almindelige muligheder
- `-O`: Gem outputtet med det samme navn som filen på serveren.
- `-L`: Følg omdirigeringer, hvis URL'en omdirigerer til en anden adresse.
- `-d`: Send data som en POST-anmodning.
- `-H`: Angiv en brugerdefineret header.
- `-u`: Angiv brugernavn og adgangskode til autentificering.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `curl`:

1. Hente en webside:
   ```bash
   curl http://example.com
   ```

2. Gemme outputtet som en fil:
   ```bash
   curl -O http://example.com/file.txt
   ```

3. Følge omdirigeringer:
   ```bash
   curl -L http://short.url
   ```

4. Udføre en POST-anmodning med data:
   ```bash
   curl -d "param1=value1&param2=value2" http://example.com/submit
   ```

5. Tilføje en brugerdefineret header:
   ```bash
   curl -H "Authorization: Bearer token" http://example.com/protected
   ```

## Tips
- Brug `-v` for at få detaljeret output om anmodningen og svaret, hvilket kan være nyttigt til fejlfinding.
- For at gemme output i en specifik fil, kan du bruge `-o` efterfulgt af filnavnet:
  ```bash
  curl -o myfile.txt http://example.com
  ```
- Vær opmærksom på, at `curl` ikke automatisk følger HTTPS-certifikatfejl. Brug `-k` for at ignorere disse fejl, men vær forsigtig, da det kan udgøre en sikkerhedsrisiko.