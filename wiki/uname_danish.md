# [Danish] Debian Almquist Shell (dash) uname brug: Få systeminformation

## Overview
`uname` er et kommandolinjeværktøj, der bruges til at vise systeminformation om den kørende kerne og operativsystemet. Det kan give oplysninger som systemets navn, version og hardwarearkitektur.

## Usage
Den grundlæggende syntaks for `uname`-kommandoen er som følger:

```bash
uname [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `uname` med korte forklaringer:

- `-a`: Viser alle tilgængelige oplysninger om systemet.
- `-s`: Viser systemets navn.
- `-n`: Viser netværksnavnet på værten.
- `-r`: Viser kerneversionen.
- `-m`: Viser maskinens hardwarearkitektur.

## Common Examples
Her er nogle praktiske eksempler på brugen af `uname`:

1. For at vise alle systemoplysninger:
    ```bash
    uname -a
    ```

2. For kun at vise systemets navn:
    ```bash
    uname -s
    ```

3. For at få netværksnavnet på værten:
    ```bash
    uname -n
    ```

4. For at se kerneversionen:
    ```bash
    uname -r
    ```

5. For at finde ud af hardwarearkitekturen:
    ```bash
    uname -m
    ```

## Tips
- Brug `uname -a` for at få en hurtig oversigt over alle relevante systemoplysninger.
- Kombinér `uname` med andre kommandoer i scripts for at tilpasse systemovervågning.
- Vær opmærksom på, at nogle muligheder kan variere afhængigt af systemets konfiguration og version.