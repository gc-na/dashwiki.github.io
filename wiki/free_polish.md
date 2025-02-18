# [Debian] Debian Almquist Shell (dash) free: wyświetlanie informacji o pamięci

## Overview
Polecenie `free` służy do wyświetlania informacji o pamięci systemowej, w tym pamięci RAM oraz pamięci wymiany (swap). Dzięki temu użytkownicy mogą szybko ocenić, ile pamięci jest dostępne, a ile jest używane przez system i uruchomione procesy.

## Usage
Podstawowa składnia polecenia `free` jest następująca:

```
free [opcje]
```

## Common Options
- `-h` – wyświetla wartości w formacie czytelnym dla człowieka (np. MB, GB).
- `-m` – wyświetla pamięć w megabajtach.
- `-g` – wyświetla pamięć w gigabajtach.
- `-s [sekundy]` – aktualizuje wyjście co określoną liczbę sekund.
- `-t` – wyświetla całkowitą pamięć (RAM + swap).

## Common Examples
1. Wyświetlenie podstawowych informacji o pamięci:
   ```bash
   free
   ```

2. Wyświetlenie informacji w formacie czytelnym dla człowieka:
   ```bash
   free -h
   ```

3. Wyświetlenie pamięci w megabajtach:
   ```bash
   free -m
   ```

4. Wyświetlenie pamięci w gigabajtach:
   ```bash
   free -g
   ```

5. Aktualizacja informacji co 5 sekund:
   ```bash
   free -s 5
   ```

6. Wyświetlenie całkowitej pamięci:
   ```bash
   free -t
   ```

## Tips
- Używaj opcji `-h`, aby szybko zrozumieć, ile pamięci jest dostępne i używane, bez potrzeby przeliczania jednostek.
- Regularne monitorowanie pamięci za pomocą opcji `-s` może pomóc w identyfikacji problemów z wydajnością systemu.
- Zwracaj uwagę na różnicę między pamięcią używaną a pamięcią dostępną, aby lepiej zrozumieć, jak system zarządza pamięcią.