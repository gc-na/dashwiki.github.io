# [Danish] Debian Almquist Shell (dash) strace brug: Spore systemopkald

## Oversigt
`strace` er et kraftfuldt værktøj, der bruges til at overvåge og diagnosticere systemopkald og signaler, der genereres af et program. Det er nyttigt til fejlfinding og forståelse af, hvordan et program interagerer med systemet.

## Brug
Den grundlæggende syntaks for `strace` er som følger:

```bash
strace [muligheder] [argumenter]
```

## Almindelige muligheder
- `-c`: Sammenfatning af systemopkald og deres tid.
- `-e`: Filtrering af systemopkald, f.eks. `-e trace=open` for kun at vise `open` opkald.
- `-o filnavn`: Gem output i den angivne fil i stedet for standard output.
- `-p PID`: Vedhæft `strace` til et kørende proces med det angivne proces-ID (PID).

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge `strace`:

1. Spore et program:
   ```bash
   strace ls
   ```

2. Gemme output til en fil:
   ```bash
   strace -o output.txt ls
   ```

3. Sammenfatte systemopkald:
   ```bash
   strace -c ls
   ```

4. Spore kun specifikke systemopkald:
   ```bash
   strace -e trace=open,close ls
   ```

5. Vedhæfte til en kørende proces:
   ```bash
   strace -p 1234
   ```

## Tips
- Brug `-c` for hurtigt at få en oversigt over, hvilke systemopkald der tager mest tid.
- Filtrér output med `-e` for at fokusere på specifikke opkald, hvilket kan gøre det lettere at finde problemer.
- Gem output til en fil, hvis du skal analysere det senere, især hvis der er meget output.