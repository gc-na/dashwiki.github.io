# [Nederlands] Debian Almquist Shell (dash) iotop gebruik: Toezicht op schijfactiviteit

## Overzicht
Het `iotop` commando is een handig hulpmiddel voor het monitoren van schijfactiviteit in real-time. Het toont welke processen de meeste I/O-bronnen gebruiken, wat nuttig kan zijn voor het diagnosticeren van prestatieproblemen.

## Gebruik
De basis syntaxis van het `iotop` commando is als volgt:

```bash
iotop [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-o`, `--only`: Toont alleen processen die momenteel I/O-activiteit genereren.
- `-b`, `--batch`: Voert `iotop` uit in batchmodus, wat handig is voor logging.
- `-d`, `--delay`: Stelt de vertraging in seconden in tussen updates (standaard is 1 seconde).
- `-p`, `--pid`: Volgt alleen de opgegeven proces-ID's.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `iotop`:

1. **Basis gebruik**:
   ```bash
   iotop
   ```

2. **Alleen processen met I/O-activiteit tonen**:
   ```bash
   iotop -o
   ```

3. **Batchmodus met een vertraging van 2 seconden**:
   ```bash
   iotop -b -d 2
   ```

4. **Volgen van specifieke processen**:
   ```bash
   iotop -p 1234
   ```

## Tips
- Gebruik `iotop` met rootrechten voor een vollediger overzicht van alle processen.
- Combineer `iotop` met andere monitoringtools zoals `htop` voor een uitgebreidere systeemanalyse.
- Let op de kolom "DISK READ" en "DISK WRITE" om snel te identificeren welke processen de meeste schijfactiviteit genereren.