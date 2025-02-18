# [Debian] Debian Almquist Shell (dash) expr użycie: wykonanie obliczeń i porównań

## Overview
Polecenie `expr` w powłoce Debian Almquist Shell (dash) służy do wykonywania prostych obliczeń arytmetycznych oraz porównań. Umożliwia obliczanie wartości liczbowych, manipulację tekstem oraz porównywanie wartości.

## Usage
Podstawowa składnia polecenia `expr` wygląda następująco:

```sh
expr [opcje] [argumenty]
```

## Common Options
- `+` : Dodawanie dwóch liczb.
- `-` : Odejmowanie drugiej liczby od pierwszej.
- `*` : Mnożenie dwóch liczb (należy używać `\*` w celu uniknięcia interpretacji przez powłokę).
- `/` : Dzielenie pierwszej liczby przez drugą.
- `%` : Reszta z dzielenia.
- `=` : Porównanie równości.
- `!=` : Porównanie nierówności.
- `>` : Sprawdzenie, czy pierwsza liczba jest większa od drugiej.
- `<` : Sprawdzenie, czy pierwsza liczba jest mniejsza od drugiej.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `expr`:

1. **Dodawanie dwóch liczb:**
   ```sh
   expr 5 + 3
   ```
   Wynik: `8`

2. **Odejmowanie:**
   ```sh
   expr 10 - 4
   ```
   Wynik: `6`

3. **Mnożenie:**
   ```sh
   expr 7 \* 6
   ```
   Wynik: `42`

4. **Dzielenie:**
   ```sh
   expr 20 / 4
   ```
   Wynik: `5`

5. **Porównanie:**
   ```sh
   expr 5 = 5
   ```
   Wynik: `1` (prawda)

6. **Sprawdzanie, czy liczba jest większa:**
   ```sh
   expr 10 \> 3
   ```
   Wynik: `1` (prawda)

## Tips
- Używaj znaku `\` przed `*`, aby uniknąć błędów związanych z interpretacją przez powłokę.
- Pamiętaj, że `expr` zwraca wartość 0 dla fałszywych porównań i 1 dla prawdziwych.
- Możesz używać `expr` w skryptach powłoki do prostych obliczeń i logiki warunkowej.