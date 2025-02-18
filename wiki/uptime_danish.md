# [Danish] Debian Almquist Shell (dash) uptime brug: Viser systemets driftstid

## Overview
`uptime`-kommandoen viser, hvor længe systemet har været aktivt, samt antallet af brugere, der er logget ind, og systemets gennemsnitlige belastning over de seneste 1, 5 og 15 minutter. Dette er nyttigt for at få en hurtig oversigt over systemets tilstand.

## Usage
Den grundlæggende syntaks for `uptime`-kommandoen er:

```sh
uptime [options]
```

## Common Options
- **-p**: Viser en menneskelig læsbar version af systemets driftstid.
- **-s**: Viser tidspunktet for systemets sidste opstart.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du bruger `uptime`:

1. **Vis driftstid og belastning**:
   ```sh
   uptime
   ```

2. **Vis driftstid i menneskelig læsbar form**:
   ```sh
   uptime -p
   ```

3. **Vis tidspunkt for sidste opstart**:
   ```sh
   uptime -s
   ```

## Tips
- Brug `uptime` regelmæssigt for at overvåge systemets sundhed og ydeevne.
- Kombiner `uptime` med andre systemovervågningsværktøjer for at få en mere omfattende forståelse af systemets tilstand.
- Hvis du bemærker en høj belastning, kan det være en god idé at undersøge, hvilke processer der bruger ressourcer.