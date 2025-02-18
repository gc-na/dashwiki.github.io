# [Svenska] Debian Almquist Shell (dash) datum: [visa och formatera datum och tid]

## Översikt
Kommandot `date` används för att visa och formatera datum och tid i Unix-liknande operativsystem. Det kan också användas för att ställa in systemets datum och tid.

## Användning
Den grundläggande syntaxen för kommandot `date` är:

```bash
date [alternativ] [argument]
```

## Vanliga alternativ
- `+FORMAT`: Formaterar utdata enligt det angivna formatet.
- `-u`: Visar datum och tid i UTC (Coordinated Universal Time).
- `-d "STRING"`: Tolkar och visar datum och tid baserat på den angivna strängen.

## Vanliga exempel
Visa det aktuella datumet och tiden:

```bash
date
```

Visa datum och tid i UTC:

```bash
date -u
```

Formatera datumet för att visa endast år, månad och dag:

```bash
date +"%Y-%m-%d"
```

Visa datum och tid från en specifik sträng:

```bash
date -d "2023-10-01 12:00:00"
```

## Tips
- Använd `date +"%c"` för att visa datum och tid i lokal tidszon i ett format som är lätt att läsa.
- Experimentera med olika formatsträngar för att få utdata i det format som passar dina behov bäst.
- Kom ihåg att `date` kan användas i skript för att automatisera datum- och tidsrelaterade uppgifter.