# [Svenska] Debian Almquist Shell (dash) cp användning: Kopiera filer och kataloger

## Översikt
Kommandot `cp` används för att kopiera filer och kataloger i Unix-liknande operativsystem, inklusive Debian. Det gör det möjligt att skapa en exakt kopia av en fil eller en katalog på en annan plats.

## Användning
Den grundläggande syntaxen för kommandot `cp` är:

```bash
cp [alternativ] [argument]
```

## Vanliga alternativ
- `-r`: Kopiera kataloger rekursivt.
- `-i`: Fråga innan en skrivning sker om målfilen redan finns.
- `-u`: Kopiera endast om källfilen är nyare än målfilen eller om målfilen inte finns.
- `-v`: Visa detaljerad information om vad som kopieras.

## Vanliga exempel
Kopiera en fil:

```bash
cp fil.txt /destination/mapp/
```

Kopiera en katalog rekursivt:

```bash
cp -r mapp1/ /destination/mapp2/
```

Kopiera en fil med bekräftelse om den redan finns:

```bash
cp -i fil.txt /destination/mapp/
```

Kopiera en fil och visa vad som kopieras:

```bash
cp -v fil.txt /destination/mapp/
```

## Tips
- Använd `-i` alternativet för att undvika oavsiktlig överskrivning av filer.
- Kontrollera alltid sökvägarna noggrant för att säkerställa att du kopierar till rätt plats.
- För stora kataloger kan det vara bra att använda `-u` för att spara tid genom att endast kopiera nya eller ändrade filer.