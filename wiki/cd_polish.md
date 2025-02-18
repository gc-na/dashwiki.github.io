# [Debian] Debian Almquist Shell (dash) cd użycie: Zmiana katalogu roboczego

## Overview
Polecenie `cd` (change directory) w powłoce Debian Almquist Shell (dash) służy do zmiany bieżącego katalogu roboczego. Umożliwia użytkownikowi nawigację po systemie plików, co jest kluczowe dla efektywnej pracy w terminalu.

## Usage
Podstawowa składnia polecenia `cd` jest następująca:

```sh
cd [opcje] [argumenty]
```

## Common Options
- `-P`: Użyj fizycznej ścieżki, nie śledź dowiązań symbolicznych.
- `-L`: Użyj dowiązań symbolicznych (domyślne zachowanie).

## Common Examples
1. Aby przejść do katalogu domowego użytkownika:
   ```sh
   cd
   ```

2. Aby przejść do konkretnego katalogu, na przykład `/usr/local`:
   ```sh
   cd /usr/local
   ```

3. Aby wrócić do katalogu nadrzędnego:
   ```sh
   cd ..
   ```

4. Aby przejść do katalogu o nazwie `projekty`, znajdującego się w bieżącym katalogu:
   ```sh
   cd projekty
   ```

5. Aby przejść do katalogu, używając ścieżki względnej:
   ```sh
   cd ./dokumenty
   ```

## Tips
- Używaj `cd -`, aby szybko przełączyć się między dwoma ostatnimi katalogami.
- Możesz użyć klawisza Tab, aby automatycznie uzupełniać nazwy katalogów, co przyspiesza nawigację.
- Zawsze sprawdzaj, w którym katalogu się znajdujesz, używając polecenia `pwd` (print working directory), aby uniknąć dezorientacji.