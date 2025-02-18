# [Polski] Debian Almquist Shell (dash) strace użycie: Śledzenie wywołań systemowych

## Overview
Polecenie `strace` służy do śledzenia wywołań systemowych i sygnałów, które są generowane przez procesy w systemie operacyjnym. Umożliwia to użytkownikom analizowanie interakcji programów z jądrem systemu, co jest przydatne w debugowaniu i monitorowaniu.

## Usage
Podstawowa składnia polecenia `strace` jest następująca:

```bash
strace [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `strace`:

- `-o <plik>`: Zapisuje wyjście do określonego pliku zamiast na standardowe wyjście.
- `-e <wyrażenie>`: Filtruje wywołania systemowe według podanego wyrażenia.
- `-p <PID>`: Śledzi już działający proces o podanym identyfikatorze procesu (PID).
- `-c`: Podsumowuje statystyki wywołań systemowych i wyświetla je na końcu.

## Common Examples
Oto kilka praktycznych przykładów użycia `strace`:

1. Śledzenie nowego procesu:
   ```bash
   strace ls
   ```

2. Zapisanie wyjścia do pliku:
   ```bash
   strace -o output.txt ls
   ```

3. Śledzenie konkretnego wywołania systemowego:
   ```bash
   strace -e open ls
   ```

4. Śledzenie działającego procesu:
   ```bash
   strace -p 1234
   ```

5. Podsumowanie statystyk wywołań:
   ```bash
   strace -c ls
   ```

## Tips
- Używaj opcji `-o`, aby zapisać wyniki do pliku, co ułatwia analizę.
- Filtruj wywołania systemowe za pomocą opcji `-e`, aby skupić się na interesujących cię operacjach.
- Pamiętaj, że `strace` może spowolnić działanie programu, więc używaj go w środowiskach testowych, jeśli to możliwe.