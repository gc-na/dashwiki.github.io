# [Nederlands] Debian Almquist Shell (dash) ulimit gebruik: Beperk systeembronnen

## Overzicht
De `ulimit`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om de systeembronnen te beperken die een shell- of procesgebruiker kan gebruiken. Dit is nuttig voor het beheren van systeembronnen en het voorkomen van overbelasting van het systeem door individuele processen.

## Gebruik
De basis syntaxis van de `ulimit`-opdracht is als volgt:

```bash
ulimit [opties] [argumenten]
```

## Veelvoorkomende opties
- `-a`: Toont alle huidige limieten.
- `-c [waarde]`: Stelt de maximale grootte van core-bestanden in.
- `-d [waarde]`: Stelt de maximale grootte van het datasegment in.
- `-f [waarde]`: Stelt de maximale grootte van bestanden in die kunnen worden aangemaakt.
- `-l [waarde]`: Stelt de maximale grootte van gelockte geheugen in.
- `-m [waarde]`: Stelt de maximale grootte van fysiek geheugen in.
- `-n [waarde]`: Stelt het maximale aantal open bestanden in.
- `-s [waarde]`: Stelt de maximale grootte van de stack in.
- `-t [waarde]`: Stelt de maximale CPU-tijd in (in seconden).
- `-v [waarde]`: Stelt de maximale virtuele geheugenruimte in.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `ulimit`:

1. **Toon alle huidige limieten**:
   ```bash
   ulimit -a
   ```

2. **Stel de maximale grootte van bestanden in op 100 MB**:
   ```bash
   ulimit -f 102400
   ```

3. **Stel de maximale grootte van core-bestanden in op 0 (geen core dumps)**:
   ```bash
   ulimit -c 0
   ```

4. **Stel het maximale aantal open bestanden in op 200**:
   ```bash
   ulimit -n 200
   ```

5. **Stel de maximale CPU-tijd in op 60 seconden**:
   ```bash
   ulimit -t 60
   ```

## Tips
- Controleer altijd de huidige limieten met `ulimit -a` voordat je wijzigingen aanbrengt.
- Wees voorzichtig bij het verhogen van limieten, aangezien dit kan leiden tot systeeminstabiliteit.
- Het is aan te raden om limieten in een shell-configuratiebestand (zoals `.bashrc` of `.profile`) in te stellen voor consistentie bij elke nieuwe sessie.