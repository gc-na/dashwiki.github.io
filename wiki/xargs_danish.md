# [Danish] Debian Almquist Shell (dash) xargs brug: Behandler input til kommandoer

## Oversigt
`xargs` er et kommandolinjeværktøj, der bruges til at konstruere og køre kommandoer ved at tage input fra standard input (stdin) og omdanne det til argumenter til en anden kommando. Det er særligt nyttigt, når du har en liste af elementer, som du ønsker at sende til en kommando, der ikke kan håndtere input direkte fra stdin.

## Brug
Den grundlæggende syntaks for `xargs` er som følger:

```bash
xargs [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n N`: Angiver, at der skal sendes N argumenter til kommandoen ad gangen.
- `-d DELIMITER`: Angiver en brugerdefineret afgrænser for inputlinjer.
- `-0`: Behandler input som null-terminerede strenge, hvilket er nyttigt til at håndtere filnavne med mellemrum.
- `-p`: Spørger brugeren om bekræftelse, før hver kommando køres.
- `-I {}`: Angiver en pladsholder, der kan bruges i kommandoen til at indsætte input.

## Almindelige eksempler

### Eksempel 1: Fjerne filer
Fjern alle `.tmp` filer i den aktuelle mappe:

```bash
find . -name "*.tmp" | xargs rm
```

### Eksempel 2: Begræns antal argumenter
Kør `echo` med maksimalt 2 argumenter ad gangen:

```bash
echo -e "fil1\nfil2\nfil3\nfil4" | xargs -n 2 echo
```

### Eksempel 3: Brug af null-terminerede strenge
Find og fjern alle filer, der ender på `.log`, selvom filnavne indeholder mellemrum:

```bash
find . -name "*.log" -print0 | xargs -0 rm
```

### Eksempel 4: Bekræftelse før udførelse
Spørg om bekræftelse, før du fjerner filer:

```bash
echo -e "fil1\nfil2" | xargs -p rm
```

## Tips
- Brug `-n` for at undgå at overskride kommandolinjelængdegrænsen, når du arbejder med mange filer.
- Kombiner `find` med `xargs` for at håndtere filer effektivt.
- Overvej at bruge `-0` med `find` for at undgå problemer med filnavne, der indeholder mellemrum eller specielle tegn.