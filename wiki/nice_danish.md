# [Dansk] Debian Almquist Shell (dash) nice brug: Juster processens prioritet

## Oversigt
`nice`-kommandoen bruges til at ændre prioriteten af en proces, når den køres. Dette kan være nyttigt, når du ønsker at køre en ressourcekrævende opgave uden at forstyrre andre processer, der kører på systemet.

## Brug
Den grundlæggende syntaks for `nice`-kommandoen er:

```bash
nice [options] [arguments]
```

## Almindelige muligheder
- `-n, --adjustment=N`: Angiv justeringen af prioriteten. Standard er 10, og værdier kan være negative for at øge prioriteten.
- `-h, --help`: Vis hjælp og afslut.
- `--version`: Vis versionsinformation og afslut.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `nice`:

1. Kør et program med standardprioritet:
   ```bash
   nice myscript.sh
   ```

2. Kør et program med en justering på 5:
   ```bash
   nice -n 5 myscript.sh
   ```

3. Kør et program med en negativ justering (-5), hvilket kræver root-rettigheder:
   ```bash
   sudo nice -n -5 myscript.sh
   ```

4. Kør et program i baggrunden med lav prioritet:
   ```bash
   nice -n 19 long_running_task &
   ```

## Tips
- Brug `nice` til at køre tunge opgaver, når du ikke ønsker at påvirke systemets responsivitet.
- Vær opmærksom på, at negative justeringer kræver root-rettigheder, så brug `sudo` om nødvendigt.
- Overvej at kombinere `nice` med `nohup` for at køre opgaver, der skal fortsætte, selv efter du logger ud.