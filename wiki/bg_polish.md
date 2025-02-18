# [Debian] Debian Almquist Shell (dash) bg: Wznawianie zadań w tle

## Overview
Polecenie `bg` w powłoce Debian Almquist Shell (dash) służy do wznawiania zatrzymanych zadań w tle. Umożliwia to kontynuowanie pracy nad zadaniami, które zostały wstrzymane, bez blokowania terminala.

## Usage
Podstawowa składnia polecenia `bg` jest następująca:

```bash
bg [numer_zadania]
```

## Common Options
- `numer_zadania`: Numer zadania, które chcesz wznowić w tle. Możesz go znaleźć, używając polecenia `jobs`.

## Common Examples
1. Wznawianie ostatniego zatrzymanego zadania w tle:
   ```bash
   bg
   ```

2. Wznawianie konkretnego zadania (np. zadanie o numerze 1):
   ```bash
   bg %1
   ```

3. Wznawianie zadania, które zostało zatrzymane przez sygnał (np. Ctrl+Z):
   ```bash
   bg %2
   ```

## Tips
- Aby sprawdzić, które zadania są aktualnie zatrzymane, użyj polecenia `jobs`.
- Możesz używać `bg` w połączeniu z `fg`, aby przełączać się między zadaniami w tle a tymi działającymi w pierwszym planie.
- Pamiętaj, że zadania w tle mogą nadal generować wyjście, więc warto przekierować ich wyjście do pliku, jeśli nie chcesz, aby zaśmiecały terminal.