# [Polski] Debian Almquist Shell (dash) xargs użycie: Przekazywanie argumentów do poleceń

## Overview
Polecenie `xargs` w powłoce Debian Almquist Shell (dash) służy do przetwarzania danych wejściowych i przekazywania ich jako argumentów do innych poleceń. Umożliwia to efektywne przetwarzanie dużych zbiorów danych, które mogą być generowane przez inne polecenia, takie jak `find` czy `grep`.

## Usage
Podstawowa składnia polecenia `xargs` jest następująca:

```bash
xargs [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `xargs`:

- `-n N`: Przekazuje maksymalnie N argumentów do polecenia.
- `-d DELIM`: Używa określonego delimitera zamiast domyślnego znaku nowej linii.
- `-0`: Oczekuje, że dane wejściowe będą zakończone znakiem null, co jest przydatne przy pracy z plikami zawierającymi spacje.
- `-p`: Pyta użytkownika o potwierdzenie przed wykonaniem każdego polecenia.
- `-I {}`: Umożliwia zastąpienie `{}` w poleceniu argumentem z wejścia.

## Common Examples
Oto kilka praktycznych przykładów użycia `xargs`:

1. **Usuwanie plików znalezionych przez `find`:**
   ```bash
   find . -name "*.tmp" | xargs rm
   ```

2. **Zliczanie linii w plikach:**
   ```bash
   ls *.txt | xargs wc -l
   ```

3. **Kopiowanie plików do innego katalogu:**
   ```bash
   find /source -name "*.jpg" | xargs -I {} cp {} /destination
   ```

4. **Przekazywanie argumentów z użyciem delimitera:**
   ```bash
   echo "file1.txt,file2.txt,file3.txt" | xargs -d ',' cp {} /destination
   ```

## Tips
- Używaj opcji `-n` aby ograniczyć liczbę argumentów przekazywanych do polecenia, co może być przydatne w przypadku poleceń, które nie obsługują dużej liczby argumentów.
- Zawsze testuj polecenia z `echo` przed ich wykonaniem, aby upewnić się, że argumenty są przekazywane poprawnie.
- W przypadku plików z nazwami zawierającymi spacje, używaj opcji `-0` w połączeniu z `find -print0`, aby uniknąć problemów z interpretacją nazw plików.