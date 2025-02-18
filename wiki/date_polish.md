# [Debian] Debian Almquist Shell (dash) data: [wyświetlanie i formatowanie daty i czasu]

## Overview
Polecenie `date` w systemie Debian Almquist Shell (dash) służy do wyświetlania oraz formatowania daty i czasu. Umożliwia użytkownikom uzyskanie aktualnych informacji o czasie oraz dostosowanie formatu wyjścia według własnych potrzeb.

## Usage
Podstawowa składnia polecenia `date` jest następująca:

```bash
date [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `date`:

- `+FORMAT` - pozwala na określenie formatu wyjścia daty i czasu.
- `-u` - wyświetla czas w formacie UTC (czas uniwersalny).
- `-d "STRING"` - interpretuje podany ciąg jako datę i czas.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `date`:

1. Wyświetlenie aktualnej daty i czasu:
   ```bash
   date
   ```

2. Wyświetlenie daty w formacie "DD-MM-YYYY":
   ```bash
   date +%d-%m-%Y
   ```

3. Wyświetlenie czasu w formacie 24-godzinnym:
   ```bash
   date +%H:%M
   ```

4. Wyświetlenie daty w formacie UTC:
   ```bash
   date -u
   ```

5. Interpretacja podanego ciągu jako daty:
   ```bash
   date -d "next Friday"
   ```

## Tips
- Używaj opcji `+FORMAT`, aby dostosować wyjście do swoich potrzeb, co może być przydatne w skryptach.
- Sprawdź dokumentację polecenia `man date`, aby uzyskać więcej informacji na temat dostępnych formatów i opcji.
- Pamiętaj, że formaty mogą się różnić w zależności od lokalizacji, więc dostosuj je zgodnie z wymaganiami swojego systemu.