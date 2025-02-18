# [Danish] Debian Almquist Shell (dash) expr brug: Beregn udtryk

## Overview
`expr` er et kommando-linje værktøj, der bruges til at evaluere udtryk og udføre grundlæggende aritmetiske operationer, sammenligninger og strenge manipulationer. Det er nyttigt til at udføre enkle beregninger og betingede operationer i scripts.

## Usage
Den grundlæggende syntaks for `expr`-kommandoen er:

```sh
expr [options] [arguments]
```

## Common Options
- `+` : Addition af to tal.
- `-` : Subtraktion af to tal.
- `*` : Multiplikation af to tal (bemærk at `*` skal escapes eller omsluttes i anførselstegn).
- `/` : Division af to tal.
- `%` : Modulus (resten af division).
- `=` : Sammenligning for lighed.
- `!=` : Sammenligning for ulighed.
- `>` : Sammenligning for større end.
- `<` : Sammenligning for mindre end.

## Common Examples
Her er nogle praktiske eksempler på brugen af `expr`:

### Aritmetiske operationer
Addition af to tal:
```sh
expr 5 + 3
```

Subtraktion af to tal:
```sh
expr 10 - 4
```

Multiplikation af to tal:
```sh
expr 6 \* 7
```

Division af to tal:
```sh
expr 20 / 4
```

Modulus operation:
```sh
expr 10 % 3
```

### Sammenligninger
Tjek om to tal er lige:
```sh
expr 5 = 5
```

Tjek om et tal er større end et andet:
```sh
expr 10 \> 3
```

### Streng manipulation
Beregn længden af en streng:
```sh
expr length "Hello, World!"
```

## Tips
- Husk at escape `*` med en backslash (`\`) eller omslutte det i anførselstegn for at undgå problemer med shell-udvidelse.
- Brug `expr` i scripts til at håndtere simple betingelser og beregninger effektivt.
- Vær opmærksom på, at `expr` kun arbejder med heltal og ikke understøtter flydende decimaler.