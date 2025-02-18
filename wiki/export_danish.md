# [Danish] Debian Almquist Shell (dash) export brug: Sætte miljøvariabler

## Oversigt
`export`-kommandoen i Debian Almquist Shell (dash) bruges til at gøre miljøvariabler tilgængelige for underordnede processer. Når en variabel eksporteres, kan den tilgås af alle programmer, der startes fra den nuværende shell-session.

## Brug
Den grundlæggende syntaks for `export`-kommandoen er som følger:

```sh
export [options] [arguments]
```

## Almindelige muligheder
- `-n`: Fjerner eksporten af en variabel, så den ikke længere er tilgængelig for underordnede processer.
- `-p`: Viser alle nuværende eksportede variabler.

## Almindelige eksempler

### Eksportere en variabel
For at eksportere en variabel, kan du bruge følgende kommando:

```sh
export MY_VAR="Hello, World!"
```

### Tjekke eksportede variabler
For at se, hvilke variabler der er eksporteret, kan du bruge:

```sh
export -p
```

### Fjerne eksporten af en variabel
Hvis du vil fjerne eksporten af en variabel, kan du gøre det med:

```sh
export -n MY_VAR
```

### Eksportere flere variabler
Du kan også eksportere flere variabler på én gang:

```sh
export VAR1="Value1" VAR2="Value2"
```

## Tips
- Husk at eksportere variabler, som du ønsker at gøre tilgængelige for underordnede processer, ellers vil de kun være tilgængelige i den aktuelle shell-session.
- Brug `export -p` til hurtigt at få et overblik over alle eksportede variabler.
- Vær opmærksom på navngivning af variabler; brug store bogstaver for at følge konventionen for miljøvariabler.