# [Svenska] Debian Almquist Shell (dash) export användning: Hantera miljövariabler

## Översikt
Kommandot `export` används i Debian Almquist Shell (dash) för att göra miljövariabler tillgängliga för alla underprocesser som startas från den aktuella skalen. Genom att exportera en variabel kan andra program och skript få tillgång till dess värde.

## Användning
Den grundläggande syntaxen för kommandot `export` är:

```sh
export [alternativ] [variabelnamn[=värde]]
```

## Vanliga alternativ
- `-n`: Ta bort exportstatus för en variabel, vilket gör att den inte längre är tillgänglig för underprocesser.
- `-p`: Visa alla exporterade variabler och deras värden.

## Vanliga exempel

### Exportera en variabel
För att exportera en variabel, använd följande kommando:

```sh
export MY_VAR="Hello, World!"
```

### Kontrollera exporterade variabler
För att se alla exporterade variabler kan du använda:

```sh
export -p
```

### Ta bort exportstatus för en variabel
Om du vill ta bort exportstatus för en variabel, gör så här:

```sh
export -n MY_VAR
```

### Använda en exporterad variabel i ett skript
Om du har exporterat en variabel kan du använda den i ett skript:

```sh
export MY_VAR="Hello"
sh -c 'echo $MY_VAR'
```

## Tips
- Tänk på att variabler som inte exporteras endast är tillgängliga i den aktuella skalsessionen.
- Använd `export` för att säkerställa att viktiga konfigurationer är tillgängliga för alla program som körs från skalen.
- Var försiktig med att överskriva befintliga variabler; kontrollera alltid deras nuvarande värden innan du sätter nya.