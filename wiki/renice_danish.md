# [Danish] Debian Almquist Shell (dash) renice brug: Juster prioriteten for kørende processer

## Oversigt
`renice`-kommandoen bruges til at ændre prioriteten af kørende processer i et Unix-lignende operativsystem. Ved at justere prioriteten kan brugeren styre, hvor meget CPU-tid en proces får i forhold til andre processer.

## Brug
Den grundlæggende syntaks for `renice`-kommandoen er:

```bash
renice [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n, --priority <værdi>`: Angiv den nye prioritet (mellem -20 og 19, hvor -20 er højeste prioritet).
- `-p, --pid <pid>`: Angiv proces-ID'et for den proces, hvis prioritet skal ændres.
- `-g, --pgrp <pgrp>`: Angiv procesgruppen, hvis prioritet skal ændres.
- `-u, --user <bruger>`: Angiv brugeren, hvis processer skal have deres prioritet ændret.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `renice` kan bruges:

1. Ændre prioriteten for en proces med PID 1234 til 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Ændre prioriteten for alle processer, der tilhører brugeren "john", til -5:
   ```bash
   renice -n -5 -u john
   ```

3. Ændre prioriteten for en procesgruppe med gruppe-ID 5678 til 0:
   ```bash
   renice -n 0 -g 5678
   ```

4. Tjekke den nuværende prioritet for en proces med PID 4321:
   ```bash
   ps -o pid,ni,comm -p 4321
   ```

## Tips
- Vær forsigtig med at sætte prioriteten for systemprocesser for lavt, da det kan påvirke systemets stabilitet.
- Brug `renice` med administratorrettigheder (sudo), hvis du skal ændre prioriteten for processer, der tilhører andre brugere.
- Overvåg systemets ydeevne efter ændringer af prioriteten for at sikre, at det fungerer som forventet.