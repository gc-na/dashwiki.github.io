# [Debian] Debian Almquist Shell (dash) umask użycie: Ustawianie domyślnych uprawnień plików

## Overview
Polecenie `umask` w powłoce Debian Almquist Shell (dash) służy do ustawiania domyślnych uprawnień dla nowych plików i katalogów. Umask określa, które uprawnienia będą odejmowane od domyślnych uprawnień, co pozwala na kontrolowanie dostępu do tworzonych zasobów.

## Usage
Podstawowa składnia polecenia `umask` wygląda następująco:

```sh
umask [opcje] [argumenty]
```

## Common Options
- `-S`: Wyświetla umask w formacie symbolicznym.
- `-p`: Wyświetla aktualną wartość umask w formacie, który można użyć w skryptach powłoki.

## Common Examples
1. **Wyświetlenie aktualnej wartości umask:**
   ```sh
   umask
   ```

2. **Ustawienie umask na 022 (domyślne uprawnienia dla plików to 644, a dla katalogów 755):**
   ```sh
   umask 022
   ```

3. **Ustawienie umask na 007 (domyślne uprawnienia dla plików to 660, a dla katalogów 770):**
   ```sh
   umask 007
   ```

4. **Wyświetlenie umask w formacie symbolicznym:**
   ```sh
   umask -S
   ```

5. **Ustawienie umask na 027 i sprawdzenie nowej wartości:**
   ```sh
   umask 027
   umask
   ```

## Tips
- Ustawienie umask w pliku konfiguracyjnym powłoki (np. `.profile` lub `.bashrc`) zapewnia, że nowe ustawienia będą stosowane przy każdym uruchomieniu powłoki.
- Używaj umask z rozwagą, aby nie ograniczać dostępu do plików, które powinny być dostępne dla innych użytkowników.
- Sprawdzaj wartość umask przed tworzeniem nowych plików, aby upewnić się, że mają one odpowiednie uprawnienia.