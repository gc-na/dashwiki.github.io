# [Debian] Debian Almquist Shell (dash) tr <Użycie: konwersja znaków>

## Overview
Polecenie `tr` w systemie Unix służy do tłumaczenia lub usuwania znaków w strumieniu tekstowym. Jest często używane do przekształcania danych wejściowych, na przykład do zmiany wielkości liter, usuwania niechcianych znaków lub zamiany jednych znaków na inne.

## Usage
Podstawowa składnia polecenia `tr` wygląda następująco:

```bash
tr [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `tr`:

- `-d`: Usuwa znaki z wejścia.
- `-s`: Zmniejsza powtarzające się znaki do jednego wystąpienia.
- `-c`: Używa do tłumaczenia znaków, które nie są wymienione w zestawie.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `tr`:

1. **Zmiana małych liter na wielkie**:
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```

2. **Usuwanie cyfr z tekstu**:
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```

3. **Zamiana spacji na znaki nowej linii**:
   ```bash
   echo "one two three" | tr ' ' '\n'
   ```

4. **Zredukowanie powtarzających się spacji**:
   ```bash
   echo "this    is    a    test" | tr -s ' '
   ```

5. **Zamiana znaków**:
   ```bash
   echo "abc" | tr 'abc' '123'
   ```

## Tips
- Używaj opcji `-s`, aby uprościć tekst i usunąć nadmiarowe znaki.
- Zawsze testuj polecenie na małej próbce danych, aby upewnić się, że działa zgodnie z oczekiwaniami.
- Pamiętaj, że `tr` nie działa na plikach bezpośrednio; musisz używać potoków lub przekierowań, aby przetwarzać zawartość plików.