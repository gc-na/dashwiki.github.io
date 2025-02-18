# [Polski] Debian Almquist Shell (dash) pidstat użycie: Monitorowanie statystyk procesów

## Overview
Polecenie `pidstat` jest używane do monitorowania statystyk wydajności procesów w systemie. Umożliwia użytkownikom śledzenie zużycia CPU, pamięci i innych zasobów przez poszczególne procesy w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `pidstat` jest następująca:

```bash
pidstat [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `pidstat`:

- `-h` : Wyświetla nagłówki kolumn w bardziej czytelny sposób.
- `-r` : Pokazuje statystyki użycia pamięci.
- `-u` : Wyświetla statystyki użycia CPU.
- `-p <pid>` : Monitoruje określony proces o podanym identyfikatorze PID.
- `-t` : Pokazuje statystyki dla wszystkich wątków procesu.

## Common Examples

1. Monitorowanie użycia CPU dla wszystkich procesów:
   ```bash
   pidstat -u
   ```

2. Monitorowanie użycia pamięci dla wszystkich procesów:
   ```bash
   pidstat -r
   ```

3. Monitorowanie konkretnego procesu o PID 1234:
   ```bash
   pidstat -p 1234
   ```

4. Monitorowanie wszystkich wątków dla procesu o PID 5678:
   ```bash
   pidstat -p 5678 -t
   ```

5. Wyświetlanie nagłówków kolumn w czytelnej formie:
   ```bash
   pidstat -h -u
   ```

## Tips
- Używaj opcji `-r` i `-u` razem, aby uzyskać pełny obraz wydajności procesów.
- Regularne monitorowanie procesów może pomóc w identyfikacji problemów z wydajnością w systemie.
- Możesz używać `pidstat` w skryptach, aby automatycznie zbierać dane o wydajności procesów w określonych interwałach czasowych.