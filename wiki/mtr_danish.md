# [Danish] Debian Almquist Shell (dash) mtr brug: Netværksdiagnoseværktøj

## Oversigt
mtr (My Traceroute) er et netværksdiagnoseværktøj, der kombinerer funktionerne fra traceroute og ping. Det bruges til at overvåge netværksforbindelser og identificere problemer med netværksruter.

## Brug
Den grundlæggende syntaks for mtr-kommandoen er:

```bash
mtr [muligheder] [argumenter]
```

## Almindelige muligheder
- `-r`: Kør i rapporttilstand, hvor resultaterne vises i et mere kompakt format.
- `-c <antal>`: Angiv antallet af pakker, der skal sendes.
- `-i <interval>`: Angiv intervallet mellem pakker i sekunder.
- `-p`: Kør i ping-tilstand, som kun sender ICMP-echo-anmodninger.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du kan bruge mtr:

1. **Standard brug**:
   For at starte en mtr-session mod en specifik adresse:
   ```bash
   mtr google.com
   ```

2. **Rapporttilstand**:
   For at generere en rapport med 10 pakker sendt:
   ```bash
   mtr -r -c 10 google.com
   ```

3. **Angiv interval**:
   For at sende pakker med et interval på 1 sekund:
   ```bash
   mtr -i 1 google.com
   ```

4. **Ping-tilstand**:
   For kun at sende ping-anmodninger:
   ```bash
   mtr -p google.com
   ```

## Tips
- Brug `-r` for at få en hurtig oversigt over netværksforbindelsen uden at skulle se på den løbende opdatering.
- Juster antallet af pakker med `-c` for at få mere præcise resultater, især hvis du tester forbindelser med høj latens.
- Overvej at køre mtr med root-rettigheder for at få mere detaljerede oplysninger om netværksruterne.