# [Norsk] Debian Almquist Shell (dash) bg bruken: Fortsetter kjørende prosesser i bakgrunnen

## Oversikt
`bg`-kommandoen brukes i Debian Almquist Shell (dash) for å fortsette en stoppet prosess i bakgrunnen. Dette er nyttig når du ønsker å frigjøre terminalen mens du lar prosessen kjøre videre.

## Bruk
Den grunnleggende syntaksen for `bg`-kommandoen er som følger:

```bash
bg [job_id]
```

## Vanlige alternativer
- `job_id`: Identifikatoren for jobben du ønsker å fortsette i bakgrunnen. Hvis du ikke spesifiserer en jobbid, vil `bg` fortsette den siste stoppede jobben.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `bg`-kommandoen:

1. **Fortsett den siste stoppede jobben i bakgrunnen**:
   ```bash
   bg
   ```

2. **Fortsett en spesifikk jobb i bakgrunnen**:
   Anta at du har stoppet en jobb med jobbid 1:
   ```bash
   bg %1
   ```

3. **Kombinere med `jobs`-kommandoen**:
   Først kan du se på stoppede jobber:
   ```bash
   jobs
   ```
   Deretter kan du fortsette en spesifikk jobb:
   ```bash
   bg %2
   ```

## Tips
- Bruk `jobs`-kommandoen for å se en liste over alle aktive og stoppede jobber før du bruker `bg`.
- Husk at prosesser som kjører i bakgrunnen kan generere utdata. Vurder å bruke omdirigering for å unngå rot i terminalen.
- Du kan bruke `fg`-kommandoen for å bringe en bakgrunnsprosess tilbake til forgrunnen hvis du trenger å interagere med den.