# [Danish] Debian Almquist Shell (dash) dirname brug: Hent stinavne

## Oversigt
`dirname` er et kommandolinjeværktøj, der bruges til at udtrække stinavnet fra en given filsti. Det returnerer den del af stien, der fører til filen, hvilket kan være nyttigt i scripts og automatisering.

## Brug
Den grundlæggende syntaks for `dirname` er som følger:

```bash
dirname [options] [arguments]
```

## Almindelige muligheder
- `-z`, `--zero`: Adskil output med nul-tegn i stedet for nye linjer. Dette er nyttigt, når man arbejder med filnavne, der indeholder nye linjer.
- `--help`: Vis en hjælpemenu med oplysninger om brugen af kommandoen.
- `--version`: Vis versionsoplysninger for `dirname`.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `dirname` kan bruges:

1. **Hent stinavnet fra en filsti**:
   ```bash
   dirname /home/bruger/dokumenter/fil.txt
   ```
   Outputtet vil være:
   ```
   /home/bruger/dokumenter
   ```

2. **Hent stinavnet fra en relativ filsti**:
   ```bash
   dirname ./projekter/kode/script.sh
   ```
   Outputtet vil være:
   ```
   ./projekter/kode
   ```

3. **Brug af dirname i et script**:
   ```bash
   FIL="/home/bruger/dokumenter/fil.txt"
   STI=$(dirname "$FIL")
   echo "Stien er: $STI"
   ```
   Outputtet vil være:
   ```
   Stien er: /home/bruger/dokumenter
   ```

4. **Hent stinavnet fra flere filstier**:
   ```bash
   dirname /var/log/syslog /etc/hosts
   ```
   Outputtet vil være:
   ```
   /var/log
   /etc
   ```

## Tips
- Brug `dirname` i kombination med andre kommandoer som `basename` for at manipulere filstier effektivt.
- Vær opmærksom på, at `dirname` fjerner den sidste del af stien, så hvis du kun har en fil uden sti, vil outputtet være en tom streng.
- Når du arbejder med scripts, kan det være nyttigt at bruge `dirname` til at få stien til det script, der kører, ved at bruge `$0` variablen.