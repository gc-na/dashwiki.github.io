# [Polski] Debian Almquist Shell (dash) nice użycie: Ustawianie priorytetu procesów

## Overview
Polecenie `nice` w systemie Linux służy do uruchamiania procesów z określonym priorytetem. Dzięki temu można kontrolować, jak bardzo dany proces może obciążać system, co jest szczególnie przydatne w przypadku uruchamiania zasobożernych aplikacji.

## Usage
Podstawowa składnia polecenia `nice` wygląda następująco:

```bash
nice [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `nice`:

- `-n, --adjustment=N`: Ustawia wartość priorytetu. Domyślnie wartość wynosi 10, a zakres to od -20 (najwyższy priorytet) do 19 (najniższy priorytet).
- `--help`: Wyświetla pomoc dotyczącą użycia polecenia.
- `--version`: Wyświetla wersję polecenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `nice`:

1. Uruchomienie programu `my_script.sh` z domyślnym priorytetem:
   ```bash
   nice ./my_script.sh
   ```

2. Uruchomienie programu `my_script.sh` z priorytetem -5:
   ```bash
   nice -n -5 ./my_script.sh
   ```

3. Uruchomienie programu `my_script.sh` z priorytetem 15:
   ```bash
   nice -n 15 ./my_script.sh
   ```

4. Sprawdzenie aktualnego priorytetu procesów:
   ```bash
   ps -o pid,ni,cmd
   ```

## Tips
- Używaj `nice` w połączeniu z innymi poleceniami, aby uruchamiać je w tle z niższym priorytetem, co pozwala na lepsze zarządzanie zasobami systemowymi.
- Pamiętaj, że tylko użytkownik root może ustawiać priorytety poniżej 0.
- Monitoruj obciążenie systemu za pomocą narzędzi takich jak `top` lub `htop`, aby lepiej zrozumieć wpływ ustawień priorytetów na wydajność.