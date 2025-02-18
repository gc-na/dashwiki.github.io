# [Debian] Debian Almquist Shell (dash) sed użycie: Edytowanie tekstu w strumieniu

## Overview
Polecenie `sed` (stream editor) jest narzędziem do przetwarzania tekstu, które umożliwia edytowanie danych wejściowych w czasie rzeczywistym. Używane jest głównie do przekształcania tekstu, wyszukiwania i zastępowania wzorców oraz wykonywania prostych operacji na plikach tekstowych.

## Usage
Podstawowa składnia polecenia `sed` jest następująca:

```bash
sed [opcje] [argumenty]
```

## Common Options
- `-e`: Umożliwia podanie wielu poleceń `sed` w jednym wywołaniu.
- `-i`: Edytuje pliki w miejscu, bez potrzeby tworzenia kopii zapasowej.
- `-n`: Tylko wyświetla linie, które pasują do wzorca, nie wyświetla wszystkich linii.
- `s/pattern/replacement/`: Podstawowa składnia do zastępowania wzorców.

## Common Examples
1. **Zastępowanie tekstu w pliku**:
   Zastąp wszystkie wystąpienia "stare" na "nowe" w pliku `plik.txt`.
   ```bash
   sed -i 's/stare/nowe/g' plik.txt
   ```

2. **Wyświetlanie tylko linii pasujących do wzorca**:
   Wyświetl tylko linie zawierające "szukany_tekst" z pliku `plik.txt`.
   ```bash
   sed -n '/szukany_tekst/p' plik.txt
   ```

3. **Usuwanie linii z pliku**:
   Usuń wszystkie linie zawierające "do_usunięcia" z pliku `plik.txt`.
   ```bash
   sed -i '/do_usunięcia/d' plik.txt
   ```

4. **Zastępowanie tekstu w strumieniu**:
   Zastąp "stare" na "nowe" w standardowym wejściu.
   ```bash
   echo "To jest stare zdanie." | sed 's/stare/nowe/'
   ```

## Tips
- Zawsze testuj swoje polecenia `sed` na kopii pliku, aby uniknąć niezamierzonych zmian.
- Używaj opcji `-n` w połączeniu z `p`, aby ograniczyć wyjście do tylko tych linii, które chcesz zobaczyć.
- Pamiętaj, że `sed` używa wyrażeń regularnych, więc znajomość ich składni może znacznie zwiększyć możliwości edycji tekstu.