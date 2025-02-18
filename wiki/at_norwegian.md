# [Norsk] Debian Almquist Shell (dash) ved at: Planlegg oppgaver for fremtiden

## Oversikt
`at`-kommandoen brukes til å planlegge oppgaver som skal kjøres på et spesifisert tidspunkt i fremtiden. Dette er nyttig for å automatisere oppgaver uten å måtte være til stede for å starte dem manuelt.

## Bruk
Grunnleggende syntaks for `at`-kommandoen er som følger:

```
at [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f` : Angi en fil som inneholder kommandoene som skal kjøres.
- `-m` : Send en e-post når oppgaven er fullført.
- `-q` : Angi køen for oppgaven (f.eks. a, b, c).
- `-l` : List opp alle planlagte oppgaver.
- `-d` : Slett en planlagt oppgave.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `at`-kommandoen kan brukes:

1. **Planlegge en oppgave for å kjøre nå**:
   ```bash
   echo "echo 'Hei, verden!'" | at now
   ```

2. **Planlegge en oppgave for å kjøre om 5 minutter**:
   ```bash
   echo "backup.sh" | at now + 5 minutes
   ```

3. **Planlegge en oppgave for å kjøre på et spesifikt tidspunkt**:
   ```bash
   echo "shutdown now" | at 22:00
   ```

4. **Bruke en fil for å kjøre flere kommandoer**:
   ```bash
   at -f /path/to/script.sh 10:00
   ```

5. **Liste opp alle planlagte oppgaver**:
   ```bash
   at -l
   ```

## Tips
- Sørg for at `atd`-tjenesten kjører på systemet ditt for at planlagte oppgaver skal fungere.
- Bruk `-m` alternativet for å motta varsler når oppgavene er fullført.
- Test oppgavene dine med en kort tidsplan for å sikre at de fungerer som forventet før du planlegger dem for lengre tid fremover.