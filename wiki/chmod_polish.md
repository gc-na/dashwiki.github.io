# [Polski] Debian Almquist Shell (dash) chmod użycie: Zmiana uprawnień plików

## Overview
Polecenie `chmod` służy do zmiany uprawnień dostępu do plików i katalogów w systemie Unix i Linux. Umożliwia użytkownikom kontrolowanie, kto może czytać, pisać lub wykonywać dany plik.

## Usage
Podstawowa składnia polecenia `chmod` wygląda następująco:

```bash
chmod [opcje] [argumenty]
```

## Common Options
- `-R`: Rekurencyjnie zmienia uprawnienia w katalogach i ich podkatalogach.
- `-v`: Wyświetla szczegółowe informacje o dokonanych zmianach.
- `-c`: Wyświetla komunikaty tylko dla zmienionych plików.

## Common Examples
1. **Zmiana uprawnień na odczyt i zapis dla właściciela oraz odczyt dla grupy i innych:**
   ```bash
   chmod 644 plik.txt
   ```

2. **Nadanie pełnych uprawnień właścicielowi, a brak uprawnień dla grupy i innych:**
   ```bash
   chmod 700 skrypt.sh
   ```

3. **Rekurencyjna zmiana uprawnień w katalogu:**
   ```bash
   chmod -R 755 katalog/
   ```

4. **Dodanie uprawnienia do wykonywania dla właściciela:**
   ```bash
   chmod u+x program
   ```

5. **Usunięcie uprawnienia do zapisu dla innych:**
   ```bash
   chmod o-w plik.txt
   ```

## Tips
- Zawsze sprawdzaj aktualne uprawnienia pliku przed ich zmianą, używając polecenia `ls -l`.
- Używaj opcji `-v` lub `-c`, aby uzyskać informacje o dokonanych zmianach, co może być pomocne w debugowaniu.
- Zrozumienie systemu uprawnień (użytkownik, grupa, inni) jest kluczowe dla skutecznego korzystania z `chmod`.