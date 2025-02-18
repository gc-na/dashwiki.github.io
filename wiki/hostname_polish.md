# [Polski] Debian Almquist Shell (dash) hostname użycie: Ustawia lub wyświetla nazwę hosta

## Overview
Polecenie `hostname` w systemie Linux służy do wyświetlania lub ustawiania nazwy hosta systemu. Nazwa hosta to unikalny identyfikator, który pozwala na rozróżnienie urządzeń w sieci.

## Usage
Podstawowa składnia polecenia `hostname` jest następująca:

```bash
hostname [opcje] [argumenty]
```

## Common Options
- `-f`, `--fqdn`: Wyświetla pełną nazwę domenową (FQDN) hosta.
- `-i`, `--ip-address`: Wyświetla adres IP hosta.
- `-s`, `--short`: Wyświetla krótką nazwę hosta.
- `--help`: Wyświetla pomoc dotyczącą polecenia.
- `--version`: Wyświetla wersję polecenia.

## Common Examples
1. Aby wyświetlić aktualną nazwę hosta:
   ```bash
   hostname
   ```

2. Aby ustawić nową nazwę hosta:
   ```bash
   sudo hostname nowa_nazwa
   ```

3. Aby wyświetlić pełną nazwę domenową:
   ```bash
   hostname -f
   ```

4. Aby wyświetlić adres IP hosta:
   ```bash
   hostname -i
   ```

5. Aby wyświetlić krótką nazwę hosta:
   ```bash
   hostname -s
   ```

## Tips
- Używaj polecenia `sudo`, aby zmienić nazwę hosta, ponieważ może być to wymagane przez system.
- Po zmianie nazwy hosta, rozważ ponowne uruchomienie systemu, aby zmiany zostały w pełni zastosowane.
- Sprawdź plik `/etc/hostname`, aby upewnić się, że nowa nazwa hosta została poprawnie zapisana.