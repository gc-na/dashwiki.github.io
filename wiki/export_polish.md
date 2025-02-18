# [Debian] Debian Almquist Shell (dash) export użycie: Ustawianie zmiennych środowiskowych

## Overview
Polecenie `export` w powłoce Debian Almquist Shell (dash) służy do ustawiania zmiennych środowiskowych, które mogą być używane przez inne procesy uruchamiane w bieżącej sesji powłoki. Dzięki `export` można przekazać wartości zmiennych do podprocesów.

## Usage
Podstawowa składnia polecenia `export` jest następująca:

```sh
export [opcje] [argumenty]
```

## Common Options
- `-p`: Wyświetla wszystkie zmienne środowiskowe, które zostały wyeksportowane.
- `VAR=value`: Ustawia zmienną `VAR` na wartość `value` i eksportuje ją do środowiska.

## Common Examples
1. Ustawienie zmiennej środowiskowej:
   ```sh
   export MY_VAR="Hello, World!"
   ```

2. Sprawdzenie, czy zmienna została ustawiona:
   ```sh
   echo $MY_VAR
   ```

3. Ustawienie i eksportowanie zmiennej w jednym kroku:
   ```sh
   export PATH="$PATH:/usr/local/bin"
   ```

4. Wyświetlenie wszystkich wyeksportowanych zmiennych:
   ```sh
   export -p
   ```

## Tips
- Używaj `export` w skryptach powłoki, aby zapewnić, że zmienne są dostępne dla wszystkich podprocesów.
- Zawsze sprawdzaj, czy zmienne zostały poprawnie ustawione, używając `echo`.
- Pamiętaj, że zmienne środowiskowe są dostępne tylko w bieżącej sesji powłoki oraz jej podprocesach.