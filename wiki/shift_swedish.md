# [Svenska] Debian Almquist Shell (dash) shift användning: Flytta positionsparametrar

## Översikt
Kommandot `shift` används i skript för att flytta positionsparametrarna åt vänster. Detta innebär att det första argumentet (position 1) tas bort, och de efterföljande argumenten flyttas upp ett steg. Det är särskilt användbart när man arbetar med skript som tar emot flera argument och man vill bearbeta dem i ordning.

## Användning
Den grundläggande syntaxen för kommandot `shift` är:

```bash
shift [n]
```

Där `n` är antalet positioner som ska flyttas. Om inget värde anges, flyttas positionerna med ett.

## Vanliga alternativ
- `n`: Anger hur många positioner som ska flyttas. Om `n` är 2, kommer de två första argumenten att tas bort.

## Vanliga exempel

### Exempel 1: Grundläggande användning
Flytta ett argument åt vänster:

```bash
#!/bin/dash
set -- arg1 arg2 arg3
echo "Före shift: $1 $2 $3"
shift
echo "Efter shift: $1 $2 $3"
```
**Utdata:**
```
Före shift: arg1 arg2 arg3
Efter shift: arg2 arg3
```

### Exempel 2: Flytta flera positioner
Flytta två argument åt vänster:

```bash
#!/bin/dash
set -- arg1 arg2 arg3 arg4
echo "Före shift: $1 $2 $3 $4"
shift 2
echo "Efter shift: $1 $2 $3 $4"
```
**Utdata:**
```
Före shift: arg1 arg2 arg3 arg4
Efter shift: arg3 arg4
```

### Exempel 3: Använda i en loop
Bearbeta alla argument i en loop:

```bash
#!/bin/dash
set -- arg1 arg2 arg3 arg4
while [ "$#" -gt 0 ]; do
    echo "Bearbetar: $1"
    shift
done
```
**Utdata:**
```
Bearbetar: arg1
Bearbetar: arg2
Bearbetar: arg3
Bearbetar: arg4
```

## Tips
- Använd `shift` i kombination med loopar för att enkelt bearbeta en lista med argument.
- Kom ihåg att `shift` påverkar alla positioner, så var försiktig när du använder det i skript som förlitar sig på specifika argument.
- Om du behöver kontrollera antalet argument innan du flyttar dem, kan du använda `$#` för att se hur många som finns kvar.