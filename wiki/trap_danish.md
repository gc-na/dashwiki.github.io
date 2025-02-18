# [Danish] Debian Almquist Shell (dash) trap brug: Håndtering af signaler

## Overview
`trap`-kommandoen i dash bruges til at fange og håndtere signaler og hændelser i et shell-script. Dette giver brugeren mulighed for at definere, hvordan scriptet skal reagere, når det modtager specifikke signaler, såsom at stoppe eller afslutte programmet.

## Usage
Den grundlæggende syntaks for `trap`-kommandoen er:

```sh
trap [handling] [signal]
```

Her angiver `[handling]` den handling, der skal udføres, når signalet modtages, og `[signal]` er det specifikke signal, du ønsker at fange.

## Common Options
- `EXIT`: Fanger signalet, når scriptet afsluttes.
- `INT`: Fanger afbrydelsessignalet (Ctrl+C).
- `TERM`: Fanger terminering af processen.
- `HUP`: Fanger signalet, når terminalen lukkes.

## Common Examples

### Eksempel 1: Fange Ctrl+C
Dette eksempel viser, hvordan man fanger Ctrl+C og udfører en oprydningshandling.

```sh
trap 'echo "Scriptet blev afbrudt"; exit' INT
while true; do
    echo "Kører..."
    sleep 1
done
```

### Eksempel 2: Oprydning ved afslutning
Her fanges EXIT-signalet for at udføre en oprydning, når scriptet afsluttes.

```sh
trap 'echo "Udfører oprydning..."; rm -f temp.txt' EXIT
echo "Kører script..."
touch temp.txt
```

### Eksempel 3: Fange terminering
I dette eksempel fanges TERM-signalet for at udføre en specifik handling.

```sh
trap 'echo "Modtaget TERM-signal"; exit' TERM
while true; do
    echo "Kører..."
    sleep 1
done
```

## Tips
- Brug `trap` til at sikre, at vigtige oprydningshandlinger altid udføres, selvom scriptet afbrydes.
- Test dine signalhåndteringsrutiner grundigt for at sikre, at de fungerer som forventet.
- Vær opmærksom på, at ikke alle signaler kan fanges, og nogle kan have standardhandlinger, der ikke kan ændres.