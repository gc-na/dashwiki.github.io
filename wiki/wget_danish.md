# [Danish] Debian Almquist Shell (dash) wget brug: Hent filer fra internettet

## Oversigt
`wget` er et kommandolinjeværktøj, der bruges til at hente filer fra internettet. Det understøtter HTTP, HTTPS og FTP protokoller og kan bruges til at downloade enkeltfiler eller hele websteder.

## Brug
Den grundlæggende syntaks for `wget`-kommandoen er:

```bash
wget [muligheder] [argumenter]
```

## Almindelige muligheder
- `-O [fil]`: Angiv navnet på den fil, som den hentede data skal gemmes i.
- `-q`: Kør i stille tilstand, uden at vise statusmeddelelser.
- `-c`: Fortsæt en afbrudt download.
- `--limit-rate=[rate]`: Begræns downloadhastigheden til den angivne værdi.
- `-r`: Hent filer rekursivt, hvilket betyder at det også henter filer fra links på den hentede side.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `wget`:

1. Hent en enkelt fil:
   ```bash
   wget https://example.com/fil.txt
   ```

2. Hent en fil og gem den med et specifikt navn:
   ```bash
   wget -O nyfil.txt https://example.com/fil.txt
   ```

3. Hent en fil i stille tilstand:
   ```bash
   wget -q https://example.com/fil.txt
   ```

4. Fortsæt en afbrudt download:
   ```bash
   wget -c https://example.com/fil.txt
   ```

5. Hent et helt websted rekursivt:
   ```bash
   wget -r https://example.com/
   ```

## Tips
- Brug `-q` for at undgå unødvendige meddelelser, når du downloader i scripts.
- Tjek altid URL'en for at sikre, at du downloader fra en pålidelig kilde.
- Overvej at bruge `--limit-rate` for at undgå at overbelaste din internetforbindelse, især ved store downloads.