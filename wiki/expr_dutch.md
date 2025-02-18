# [Nederlands] Debian Almquist Shell (dash) expr gebruik: Voer eenvoudige berekeningen en stringbewerkingen uit

## Overzicht
De `expr`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om eenvoudige wiskundige berekeningen en stringbewerkingen uit te voeren. Het kan worden gebruikt om waarden te evalueren, zoals optellen, aftrekken, en het vergelijken van strings.

## Gebruik
De basis syntaxis van de `expr`-opdracht is als volgt:

```bash
expr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `+` : Optellen van twee getallen.
- `-` : Aftrekken van twee getallen.
- `*` : Vermenigvuldigen van twee getallen (let op dat je dit moet escapen met een backslash `\*`).
- `/` : Delen van twee getallen.
- `%` : Modulus (rest) van twee getallen.
- `=` : Vergelijken van twee waarden op gelijkheid.
- `!=` : Vergelijken van twee waarden op ongelijkheid.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Optellen
```bash
expr 5 + 3
```
Dit geeft `8` als resultaat.

### Voorbeeld 2: Aftrekken
```bash
expr 10 - 4
```
Dit geeft `6` als resultaat.

### Voorbeeld 3: Vermenigvuldigen
```bash
expr 7 \* 6
```
Dit geeft `42` als resultaat.

### Voorbeeld 4: Delen
```bash
expr 20 / 4
```
Dit geeft `5` als resultaat.

### Voorbeeld 5: Modulus
```bash
expr 10 % 3
```
Dit geeft `1` als resultaat.

### Voorbeeld 6: Stringvergelijking
```bash
expr "Hallo" = "Hallo"
```
Dit geeft `1` (waar) als resultaat.

## Tips
- Vergeet niet om de `*` operator te escapen met een backslash (`\*`) om syntaxfouten te voorkomen.
- Gebruik haakjes om de volgorde van bewerkingen te regelen, bijvoorbeeld: `expr \( 3 + 2 \) \* 2`.
- `expr` is handig voor eenvoudige berekeningen, maar voor complexere wiskundige bewerkingen kun je overwegen om andere tools zoals `bc` te gebruiken.