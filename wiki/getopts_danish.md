# [Danish] Debian Almquist Shell (dash) getopts brug: Håndtering af kommandolinjeindstillinger

## Oversigt
`getopts` er et indbygget shell-kommando, der bruges til at analysere kommandolinjeindstillinger og argumenter i scripts. Det gør det muligt for brugeren at definere og håndtere indstillinger, der kan gives til et script, hvilket gør det mere fleksibelt og brugervenligt.

## Brug
Den grundlæggende syntaks for `getopts` er som følger:

```sh
getopts [options] [arguments]
```

## Almindelige muligheder
- `-a`: Angiver, at `getopts` skal analysere indstillingerne i en specifik rækkefølge.
- `-o`: Definerer de tilladte indstillinger, der kan bruges i scriptet.
- `-l`: Angiver lange indstillinger, der kan bruges i stedet for korte indstillinger.

## Almindelige eksempler

### Eksempel 1: Grundlæggende brug af getopts
Her er et simpelt script, der bruger `getopts` til at håndtere indstillinger:

```sh
#!/bin/sh

while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected with argument: $OPTARG"
      ;;
    c)
      echo "Option C selected with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### Eksempel 2: Brug af lange indstillinger
Dette eksempel viser, hvordan man kan bruge lange indstillinger med `getopts`:

```sh
#!/bin/sh

while getopts "a-b:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

### Eksempel 3: Håndtering af flere indstillinger
I dette eksempel håndteres flere indstillinger samtidigt:

```sh
#!/bin/sh

while getopts "abc:" opt; do
  case $opt in
    a)
      echo "Option A selected"
      ;;
    b)
      echo "Option B selected"
      ;;
    c)
      echo "Option C selected with argument: $OPTARG"
      ;;
    *)
      echo "Invalid option"
      ;;
  esac
done
```

## Tips
- Sørg for at definere alle mulige indstillinger i `getopts`-strengen for at undgå uventede resultater.
- Brug `$OPTARG` til at få adgang til argumenter, der følger efter indstillingerne.
- Test dit script grundigt for at sikre, at alle indstillinger håndteres korrekt.