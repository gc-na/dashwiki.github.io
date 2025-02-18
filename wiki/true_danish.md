# [Danish] Debian Almquist Shell (dash) true brug: [returner altid succes]

## Oversigt
`true` er en simpel kommando i Debian Almquist Shell (dash), der altid returnerer en successtatus (exit status 0). Den bruges ofte i scripts og kommandolinjer, hvor en succesfuld afslutning er nødvendig, men hvor der ikke er nogen specifik handling, der skal udføres.

## Brug
Den grundlæggende syntaks for `true` er:

```bash
true [options] [arguments]
```

## Almindelige muligheder
`true` har ingen specifikke muligheder, da dens eneste funktion er at returnere en successtatus. 

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `true` kan anvendes:

1. **Brug i en if-sætning:**
   ```bash
   if true; then
       echo "Dette vil altid blive vist."
   fi
   ```

2. **Som en placeholder i scripts:**
   ```bash
   while true; do
       true
   done
   ```

3. **I en kommandokæde:**
   ```bash
   true && echo "Kommandoen lykkedes."
   ```

4. **I en while-løkke til at køre en kommando kontinuerligt:**
   ```bash
   while true; do
       echo "Kører..."
       sleep 1
   done
   ```

## Tips
- Brug `true` i scripts, hvor du har brug for en kommando, der altid lykkes, for at undgå fejl.
- Det kan være nyttigt at bruge `true` i kombination med andre kommandoer i kommandokæder for at sikre, at efterfølgende kommandoer kun køres, hvis den forrige lykkedes.
- Overvej at bruge `false` i modsætning til `true`, når du ønsker at simulere en fejlsituation i dine tests.