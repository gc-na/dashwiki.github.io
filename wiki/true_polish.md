# [Debian] Debian Almquist Shell (dash) true: Zwraca prawdę

## Overview
Polecenie `true` w powłoce Debian Almquist Shell (dash) jest prostym narzędziem, które zawsze zwraca kod zakończenia 0, co oznacza sukces. Jest często używane w skryptach, aby zasygnalizować, że operacja zakończyła się pomyślnie, lub jako placeholder w miejscach, gdzie wymagana jest komenda.

## Usage
Podstawowa składnia polecenia `true` jest następująca:

```sh
true [opcje] [argumenty]
```

## Common Options
Polecenie `true` nie ma żadnych opcji ani argumentów. Jego jedyną funkcją jest zwrócenie kodu zakończenia 0.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `true`:

1. **Użycie w skrypcie**:
   ```sh
   #!/bin/dash
   if true; then
       echo "To zawsze się wykona."
   fi
   ```

2. **Zastosowanie w pętli**:
   ```sh
   while true; do
       echo "Ta pętla będzie działać w nieskończoność."
       sleep 1
   done
   ```

3. **Jako placeholder**:
   ```sh
   for i in 1 2 3; do
       true # Możesz tu wstawić inną komendę w przyszłości
   done
   ```

## Tips
- Używaj `true` w skryptach, gdy potrzebujesz komendy, która zawsze zakończy się sukcesem.
- Może być przydatne w testach warunkowych, gdzie chcesz, aby dany blok kodu był zawsze wykonywany.
- `true` jest bardzo szybkie i nie wymaga żadnych zasobów, co czyni je idealnym do użycia w skryptach automatyzacyjnych.