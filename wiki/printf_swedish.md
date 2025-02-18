# [Svenska] Debian Almquist Shell (dash) printf användning: Formatera och skriv ut text

## Översikt
`printf`-kommandot används för att formatera och skriva ut text till standardutgången. Det erbjuder mer kontroll över formatet av utskriften jämfört med det enklare `echo`-kommandot.

## Användning
Den grundläggande syntaxen för `printf` är:

```bash
printf [alternativ] [argument]
```

## Vanliga alternativ
- `-v var`: Spara resultatet i en variabel istället för att skriva ut det.
- `-f format`: Ange ett format för utskriften, där du kan specificera hur data ska visas (t.ex. decimaler, teckenlängd).
- `-n`: Inkludera inte en ny rad i slutet av utskriften.

## Vanliga exempel
Här är några praktiska exempel på hur `printf` kan användas:

### Exempel 1: Enkel textutskrift
```bash
printf "Hej, världen!\n"
```

### Exempel 2: Formatera ett heltal
```bash
printf "Numret är: %d\n" 42
```

### Exempel 3: Formatera flyttal
```bash
printf "Pi är ungefär: %.2f\n" 3.14159
```

### Exempel 4: Utskrift av flera värden
```bash
printf "Namn: %s, Ålder: %d\n" "Alice" 30
```

### Exempel 5: Spara resultatet i en variabel
```bash
printf -v my_var "Värdet är: %d" 100
echo "$my_var"
```

## Tips
- Använd `\n` för att skapa nya rader i utskriften.
- Var noga med att matcha formatsträngarna med de angivna argumenten för att undvika oväntade resultat.
- Testa olika format för att se hur de påverkar utskriften, särskilt med flyttal och teckenlängder.