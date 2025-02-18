# [Danish] Debian Almquist Shell (dash) cd brug: Skift katalog

## Overview
`cd` (change directory) er en kommando, der bruges til at ændre det aktuelle arbejdsbibliotek i terminalen. Ved at bruge `cd` kan du navigere mellem forskellige mapper i filsystemet.

## Usage
Den grundlæggende syntaks for `cd`-kommandoen er:

```
cd [options] [arguments]
```

## Common Options
- `-`: Skifter til det forrige bibliotek.
- `..`: Skifter til overordnede bibliotek.
- `~`: Skifter til brugerens hjemmemappe.

## Common Examples
Her er nogle praktiske eksempler på brugen af `cd`:

1. Skift til en specifik mappe:
   ```sh
   cd /sti/til/mappen
   ```

2. Skift til den overordnede mappe:
   ```sh
   cd ..
   ```

3. Skift til brugerens hjemmemappe:
   ```sh
   cd ~
   ```

4. Skift tilbage til den forrige mappe:
   ```sh
   cd -
   ```

## Tips
- Brug `cd` med tab-tasten for automatisk at fuldføre mappenavne.
- Tjek din nuværende mappe med `pwd` efter at have brugt `cd` for at sikre, at du er i den ønskede mappe.
- Hvis du ofte skifter til en bestemt mappe, kan du overveje at oprette en alias i din shell-konfiguration.