# [Svenska] Debian Almquist Shell (dash) env användning: Hantera miljövariabler

## Översikt
`env`-kommandot används för att visa eller ändra miljövariabler i Unix-liknande operativsystem. Det kan också användas för att köra ett program med en modifierad miljö.

## Användning
Den grundläggande syntaxen för `env`-kommandot är:

```bash
env [alternativ] [argument]
```

## Vanliga alternativ
- `-i`: Starta en ny miljö utan några miljövariabler.
- `-u VARIABEL`: Ta bort den angivna miljövariabeln från miljön.
- `VARIABEL=VÄRDE`: Sätt en miljövariabel till ett specifikt värde innan du kör ett kommando.

## Vanliga exempel
Här är några praktiska exempel på hur `env` kan användas:

1. Visa alla aktuella miljövariabler:
   ```bash
   env
   ```

2. Köra ett kommando med en specifik miljövariabel:
   ```bash
   env MY_VAR=hello bash -c 'echo $MY_VAR'
   ```

3. Ta bort en miljövariabel och köra ett kommando:
   ```bash
   env -u MY_VAR bash -c 'echo $MY_VAR'
   ```

4. Starta en ny miljö utan några miljövariabler:
   ```bash
   env -i bash
   ```

## Tips
- Använd `env` för att testa program i en ren miljö utan att påverkas av befintliga miljövariabler.
- När du sätter miljövariabler, kom ihåg att de endast gäller för det kommando som körs direkt efter `env`.
- Det kan vara bra att använda `env` i skript för att säkerställa att rätt version av ett program körs, särskilt om det finns flera versioner installerade.