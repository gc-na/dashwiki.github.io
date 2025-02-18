# [Debian] Debian Almquist Shell (dash) sftp użycie: Przesyłanie plików przez SSH

## Overview
Polecenie `sftp` (Secure File Transfer Protocol) służy do bezpiecznego przesyłania plików między komputerami za pomocą protokołu SSH. Umożliwia zarówno przesyłanie plików, jak i zarządzanie zdalnymi katalogami.

## Usage
Podstawowa składnia polecenia `sftp` wygląda następująco:

```bash
sftp [opcje] [użytkownik@host]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `sftp`:

- `-o` : Umożliwia przekazanie dodatkowych opcji do klienta SSH.
- `-P` : Określa port, na którym nasłuchuje serwer SSH (domyślnie 22).
- `-b` : Umożliwia wykonanie poleceń z pliku wsadowego.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `sftp`:

1. Połączenie z serwerem SFTP:
   ```bash
   sftp user@hostname
   ```

2. Przesyłanie pliku na serwer:
   ```bash
   put lokalny_plik.txt
   ```

3. Pobieranie pliku z serwera:
   ```bash
   get zdalny_plik.txt
   ```

4. Przesyłanie katalogu:
   ```bash
   put -r lokalny_katalog
   ```

5. Wykonywanie poleceń z pliku wsadowego:
   ```bash
   sftp -b polecenia.txt user@hostname
   ```

## Tips
- Zawsze używaj opcji `-P`, jeśli serwer SSH nasłuchuje na innym porcie niż domyślny.
- Możesz używać komendy `ls` w sesji `sftp`, aby wyświetlić zawartość zdalnego katalogu.
- Zapisuj często używane polecenia w pliku wsadowym, aby uprościć proces przesyłania plików.