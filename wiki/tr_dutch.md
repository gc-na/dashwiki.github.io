# [Nederlands] Debian Almquist Shell (dash) tr: teksttransformatie

## Overzicht
De `tr` (translate) opdracht in de Debian Almquist Shell (dash) wordt gebruikt om tekens in tekstbestanden te vertalen of te verwijderen. Het is een krachtig hulpmiddel voor het manipuleren van tekststromen door specifieke karakters te vervangen of te verwijderen.

## Gebruik
De basis syntaxis van de `tr` opdracht is als volgt:

```bash
tr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`: Verwijder de opgegeven karakters.
- `-s`: Vervang opeenvolgende herhalingen van een karakter door één exemplaar.
- `-c`: Gebruik complement van de opgegeven karakters.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Vervangen van karakters
Vervang alle kleine letters 'a' door hoofdletters 'A' in een tekstbestand.

```bash
echo "een appel" | tr 'a' 'A'
```

### Voorbeeld 2: Verwijderen van karakters
Verwijder alle cijfers uit een tekst.

```bash
echo "Huisnummer 123" | tr -d '0-9'
```

### Voorbeeld 3: Opeenvolgende spaties verminderen
Verminder opeenvolgende spaties tot één enkele spatie.

```bash
echo "Dit    is    een   test." | tr -s ' '
```

### Voorbeeld 4: Gebruik van complement
Vervang alle niet-alfabetische karakters door een spatie.

```bash
echo "Hallo! Hoe gaat het?" | tr -c '[:alpha:]' ' '
```

## Tips
- Gebruik `tr` in combinatie met andere commando's zoals `grep` of `sort` voor geavanceerdere tekstverwerking.
- Wees voorzichtig met het gebruik van `-d`, omdat het gegevens permanent verwijdert.
- Test je `tr` opdrachten met `echo` voordat je ze op bestanden toepast om onbedoelde wijzigingen te voorkomen.