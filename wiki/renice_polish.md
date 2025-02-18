# [Polski] Debian Almquist Shell (dash) renice: Zmiana priorytetu procesów

## Overview
Polecenie `renice` służy do zmiany priorytetu już działających procesów w systemie. Priorytet procesów wpływa na to, jak dużo czasu procesora otrzymują w porównaniu do innych procesów. Wyższy priorytet oznacza, że proces będzie miał więcej czasu na wykonanie swoich zadań.

## Usage
Podstawowa składnia polecenia `renice` jest następująca:

```bash
renice [opcje] [argumenty]
```

## Common Options
- `-n`, `--priority`: Umożliwia określenie nowego priorytetu dla procesów. Można podać wartość od -20 (najwyższy priorytet) do 19 (najniższy priorytet).
- `-p`, `--pid`: Określa identyfikator procesu (PID), dla którego ma być zmieniony priorytet.
- `-g`, `--pgrp`: Zmienia priorytet dla grupy procesów.
- `-u`, `--user`: Zmienia priorytet dla wszystkich procesów uruchomionych przez danego użytkownika.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `renice`:

1. Zmiana priorytetu procesu o PID 1234 na 10:

   ```bash
   renice 10 -p 1234
   ```

2. Zmiana priorytetu wszystkich procesów uruchomionych przez użytkownika `janek` na 5:

   ```bash
   renice 5 -u janek
   ```

3. Zmiana priorytetu grupy procesów o PID 5678 na -5:

   ```bash
   renice -5 -g 5678
   ```

4. Sprawdzenie aktualnego priorytetu procesu przed jego zmianą:

   ```bash
   ps -o pid,ni,comm -p 1234
   ```

## Tips
- Używaj `renice` ostrożnie, ponieważ nadawanie zbyt wysokiego priorytetu może spowodować, że inne procesy będą działały wolniej.
- Aby zmienić priorytet, musisz mieć odpowiednie uprawnienia, co oznacza, że możesz potrzebować uruchomić polecenie jako root.
- Zawsze sprawdzaj aktualny priorytet procesów przed ich modyfikacją, aby uniknąć niepożądanych efektów.