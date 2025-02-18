# [Polski] Debian Almquist Shell (dash) trap użycie: obsługuje sygnały i zakończenia skryptów

## Overview
Polecenie `trap` w powłoce Debian Almquist Shell (dash) służy do przechwytywania sygnałów i wykonywania określonych działań w momencie ich otrzymania. Dzięki temu można kontrolować, co się dzieje, gdy skrypt napotyka na sygnały, takie jak przerwanie (SIGINT) czy zakończenie (SIGTERM).

## Usage
Podstawowa składnia polecenia `trap` wygląda następująco:

```sh
trap [akcja] [sygnał...]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `trap`:

- `SIGINT` - sygnał przerwania, zwykle wysyłany przez Ctrl+C.
- `SIGTERM` - sygnał zakończenia, używany do żądania zakończenia procesu.
- `EXIT` - akcja wykonywana przy zakończeniu skryptu, niezależnie od sygnału.

## Common Examples

### Przykład 1: Przechwytywanie sygnału SIGINT
W tym przykładzie, gdy użytkownik naciśnie Ctrl+C, skrypt wyświetli wiadomość i zakończy działanie.

```sh
trap 'echo "Skrypt przerwany"; exit' SIGINT
while true; do
    echo "Działam..."
    sleep 1
done
```

### Przykład 2: Wykonywanie akcji przy zakończeniu skryptu
W tym przykładzie, przy zakończeniu skryptu, zostanie wyświetlona wiadomość.

```sh
trap 'echo "Skrypt zakończony"; exit' EXIT
echo "Rozpoczynam działanie skryptu..."
sleep 5
```

### Przykład 3: Przechwytywanie wielu sygnałów
Można przechwytywać wiele sygnałów i przypisać im tę samą akcję.

```sh
trap 'echo "Otrzymano sygnał"; exit' SIGINT SIGTERM
while true; do
    echo "Czekam na sygnał..."
    sleep 2
done
```

## Tips
- Zawsze używaj `trap` w skryptach, które mogą być przerwane, aby zapewnić, że zasoby są poprawnie zwalniane.
- Używaj `EXIT`, aby wykonywać sprzątanie niezależnie od sposobu zakończenia skryptu.
- Testuj swoje skrypty w bezpiecznym środowisku, aby upewnić się, że `trap` działa zgodnie z oczekiwaniami.