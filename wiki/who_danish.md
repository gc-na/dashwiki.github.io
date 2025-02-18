# [Danish] Debian Almquist Shell (dash) who: viser brugere der er logget ind

## Oversigt
`who`-kommandoen bruges til at vise en liste over brugere, der i øjeblikket er logget ind på systemet. Den giver information om, hvilke brugere der er aktive, samt deres login-tid og terminal.

## Brug
Den grundlæggende syntaks for `who`-kommandoen er:

```bash
who [options] [arguments]
```

## Almindelige muligheder
- `-b`: Viser tidspunktet for den seneste systemopstart.
- `-q`: Viser en kort oversigt over brugerne og antallet af loggede ind brugere.
- `-H`: Viser overskrifter for kolonnerne i outputtet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `who`-kommandoen:

1. Vise alle loggede ind brugere:
   ```bash
   who
   ```

2. Vise tidspunktet for den seneste systemopstart:
   ```bash
   who -b
   ```

3. Vise en kort oversigt over loggede ind brugere:
   ```bash
   who -q
   ```

4. Vise brugere med kolonneoverskrifter:
   ```bash
   who -H
   ```

## Tips
- Brug `who` regelmæssigt for at holde øje med, hvilke brugere der er logget ind på systemet.
- Kombiner `who` med andre kommandoer som `grep` for at filtrere resultaterne, f.eks. for at finde en specifik bruger:
  ```bash
  who | grep brugernavn
  ```
- Husk, at `who` kun viser brugere, der er logget ind via terminaler; det viser ikke brugere, der er logget ind via grafiske brugergrænseflader.