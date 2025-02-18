# [Danish] Debian Almquist Shell (dash) mkdir Brug: Opretter nye mapper

## Overview
`mkdir` kommandoen bruges til at oprette nye mapper (eller kataloger) i filsystemet. Det er en grundlæggende kommando, der gør det muligt for brugere at organisere deres filer i strukturerede kataloger.

## Usage
Den grundlæggende syntaks for `mkdir` kommandoen er som følger:

```bash
mkdir [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `mkdir` sammen med korte forklaringer:

- `-p`: Opretter forældremapper, hvis de ikke allerede eksisterer.
- `-v`: Viser en meddelelse for hver oprettet mappe.
- `--help`: Viser hjælp til brug af kommandoen.

## Common Examples
Her er flere praktiske eksempler på, hvordan `mkdir` kan bruges:

1. Opret en enkelt mappe:
   ```bash
   mkdir ny_mappe
   ```

2. Opret flere mapper på én gang:
   ```bash
   mkdir mappe1 mappe2 mappe3
   ```

3. Opret en mappe med forældremapper:
   ```bash
   mkdir -p /sti/til/ny/mappe
   ```

4. Opret en mappe og vis en meddelelse:
   ```bash
   mkdir -v ny_mappe
   ```

## Tips
- Brug `-p` muligheden for at undgå fejl, når du opretter en mappe i en sti, hvor forældremapperne ikke eksisterer.
- Overvej at bruge beskrivende navne til dine mapper for bedre organisering.
- Tjek altid, om mappen allerede eksisterer for at undgå unødvendige fejl.