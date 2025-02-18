# [Norsk] Debian Almquist Shell (dash) jobs bruk: viser bakgrunnsjobber

## Oversikt
`jobs`-kommandoen brukes i Debian Almquist Shell (dash) for å vise statusen til bakgrunnsjobber som kjører i den nåværende terminalsesjonen. Den gir informasjon om jobber som er startet i bakgrunnen, samt deres tilstand, noe som er nyttig for å administrere prosesser.

## Bruk
Den grunnleggende syntaksen for `jobs`-kommandoen er som følger:

```bash
jobs [alternativer] [argumenter]
```

## Vanlige alternativer
- `-l`: Viser prosess-ID (PID) for hver jobb i tillegg til jobbenes status.
- `-n`: Viser bare jobber som har endret status siden sist `jobs` ble kjørt.
- `-p`: Viser kun prosess-IDene til jobbene.

## Vanlige eksempler
Her er noen praktiske eksempler på bruk av `jobs`-kommandoen:

1. Vise alle bakgrunnsjobber:
   ```bash
   jobs
   ```

2. Vise bakgrunnsjobber med prosess-ID:
   ```bash
   jobs -l
   ```

3. Vise kun jobber som har endret status:
   ```bash
   jobs -n
   ```

4. Vise prosess-IDene til jobbene:
   ```bash
   jobs -p
   ```

## Tips
- Bruk `bg`-kommandoen for å fortsette en stoppet jobb i bakgrunnen etter å ha sjekket status med `jobs`.
- Kombiner `jobs` med `fg` for å bringe en bakgrunnsjobb til forgrunnen.
- Husk at `jobs` kun viser jobber som er startet i den nåværende terminalsesjonen; hvis du åpner en ny terminal, vil ikke `jobs` vise jobber fra den gamle.