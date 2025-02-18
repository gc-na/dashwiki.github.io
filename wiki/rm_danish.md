# [Danish] Debian Almquist Shell (dash) rm Brug: Slet filer og mapper

## Oversigt
`rm`-kommandoen bruges til at slette filer og mapper fra filsystemet. Det er en kraftfuld kommando, der permanent fjerner angivne filer, så vær forsigtig, når du bruger den.

## Brug
Den grundlæggende syntaks for `rm`-kommandoen er som følger:

```bash
rm [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`: Tvinger sletning uden at spørge om bekræftelse.
- `-i`: Spørger om bekræftelse, før hver fil slettes.
- `-r`: Sletter mapper rekursivt, inklusive deres indhold.
- `-v`: Viser detaljer om, hvad der bliver slettet.

## Almindelige eksempler
Slet en enkelt fil:

```bash
rm filnavn.txt
```

Slet flere filer på én gang:

```bash
rm fil1.txt fil2.txt fil3.txt
```

Slet en mappe og dens indhold rekursivt:

```bash
rm -r mappe_navn
```

Slet en fil uden bekræftelse:

```bash
rm -f filnavn.txt
```

Slet filer med bekræftelse:

```bash
rm -i filnavn.txt
```

## Tips
- Brug `-i`-muligheden, når du sletter vigtige filer, for at undgå utilsigtet sletning.
- Overvej at bruge `-v` for at få feedback om, hvilke filer der bliver slettet.
- Vær ekstra forsigtig med `-r`-muligheden, da den kan slette hele mapper og deres indhold uden mulighed for gendannelse.