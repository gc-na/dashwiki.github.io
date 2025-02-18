# [Polski] Debian Almquist Shell (dash) id: [wyświetlanie informacji o użytkowniku]

## Overview
Polecenie `id` w systemie Unix/Linux służy do wyświetlania informacji o użytkowniku, w tym identyfikatora użytkownika (UID), identyfikatora grupy (GID) oraz przynależności do grup. To narzędzie jest przydatne do szybkiego sprawdzenia, jakie uprawnienia ma dany użytkownik.

## Usage
Podstawowa składnia polecenia `id` jest następująca:

```sh
id [opcje] [argumenty]
```

## Common Options
- `-u`: Wyświetla tylko identyfikator użytkownika (UID).
- `-g`: Wyświetla tylko identyfikator grupy (GID).
- `-G`: Wyświetla identyfikatory wszystkich grup, do których należy użytkownik.
- `-n`: Wyświetla nazwy zamiast identyfikatorów.
- `-r`: Wyświetla rzeczywiste identyfikatory użytkownika i grupy.

## Common Examples
1. Wyświetlenie podstawowych informacji o bieżącym użytkowniku:
   ```sh
   id
   ```

2. Wyświetlenie tylko identyfikatora użytkownika:
   ```sh
   id -u
   ```

3. Wyświetlenie tylko identyfikatora grupy:
   ```sh
   id -g
   ```

4. Wyświetlenie wszystkich grup, do których należy użytkownik:
   ```sh
   id -G
   ```

5. Wyświetlenie informacji o innym użytkowniku (np. `username`):
   ```sh
   id username
   ```

## Tips
- Używaj opcji `-n`, aby uzyskać bardziej czytelne wyniki, gdy interesują Cię nazwy grup i użytkowników.
- Sprawdzaj przynależność do grup, aby upewnić się, że masz odpowiednie uprawnienia do wykonywania określonych działań w systemie.
- Możesz łączyć różne opcje, aby uzyskać bardziej szczegółowe informacje, na przykład `id -Gn`, aby wyświetlić nazwy grup użytkownika.