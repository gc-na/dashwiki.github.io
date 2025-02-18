# [Polski] Debian Almquist Shell (dash) passwd użycie: Zmiana haseł użytkowników

## Overview
Polecenie `passwd` służy do zmiany haseł użytkowników w systemie. Umożliwia administratorom oraz użytkownikom aktualizację swojego hasła, co jest kluczowe dla utrzymania bezpieczeństwa systemu.

## Usage
Podstawowa składnia polecenia `passwd` jest następująca:

```
passwd [opcje] [argumenty]
```

## Common Options
- `-d`: Usuwa hasło użytkownika, co oznacza, że konto stanie się dostępne bez hasła.
- `-e`: Wymusza natychmiastową zmianę hasła przy następnym logowaniu.
- `-l`: Blokuje konto użytkownika, co uniemożliwia logowanie.
- `-u`: Odblokowuje konto użytkownika.

## Common Examples
1. **Zmiana hasła bieżącego użytkownika:**
   ```bash
   passwd
   ```

2. **Zmiana hasła dla innego użytkownika (wymaga uprawnień administratora):**
   ```bash
   sudo passwd nazwa_użytkownika
   ```

3. **Wymuszenie zmiany hasła przy następnym logowaniu:**
   ```bash
   passwd -e nazwa_użytkownika
   ```

4. **Usunięcie hasła użytkownika:**
   ```bash
   sudo passwd -d nazwa_użytkownika
   ```

5. **Blokowanie konta użytkownika:**
   ```bash
   sudo passwd -l nazwa_użytkownika
   ```

## Tips
- Zawsze używaj silnych haseł, aby zwiększyć bezpieczeństwo swojego konta.
- Regularnie zmieniaj hasła, zwłaszcza w przypadku kont administracyjnych.
- Używaj opcji `-e`, aby wymusić na użytkownikach zmianę haseł po określonym czasie.