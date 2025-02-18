# [Polski] Debian Almquist Shell (dash) shift <Użycie: Przesunięcie argumentów pozycyjnych>

## Przegląd
Polecenie `shift` w powłoce Debian Almquist Shell (dash) służy do przesuwania argumentów pozycyjnych w skryptach powłoki. Umożliwia to usunięcie pierwszego argumentu z listy, co pozwala na łatwiejsze zarządzanie pozostałymi argumentami.

## Użycie
Podstawowa składnia polecenia `shift` wygląda następująco:

```sh
shift [n]
```

Gdzie `n` to liczba argumentów, które mają zostać przesunięte. Jeśli `n` nie jest podane, domyślnie przesuwany jest jeden argument.

## Częste opcje
- `n`: Liczba argumentów do przesunięcia. Jeśli nie zostanie podana, przesunięcie dotyczy jednego argumentu.

## Częste przykłady
1. **Podstawowe przesunięcie**:
   Przesunięcie jednego argumentu pozycyjnego.
   ```sh
   #!/bin/dash
   set -- a b c
   echo "$1"  # Wypisuje: a
   shift
   echo "$1"  # Wypisuje: b
   ```

2. **Przesunięcie wielu argumentów**:
   Przesunięcie dwóch argumentów pozycyjnych.
   ```sh
   #!/bin/dash
   set -- 1 2 3 4 5
   echo "$1"  # Wypisuje: 1
   shift 2
   echo "$1"  # Wypisuje: 3
   ```

3. **Użycie w pętli**:
   Przesuwanie argumentów w pętli do przetwarzania wszystkich.
   ```sh
   #!/bin/dash
   set -- apple banana cherry
   while [ "$#" -gt 0 ]; do
       echo "$1"
       shift
   done
   # Wypisuje:
   # apple
   # banana
   # cherry
   ```

## Wskazówki
- Używaj `shift` w skryptach, gdy potrzebujesz przetwarzać argumenty w pętli, aby uprościć kod.
- Pamiętaj, że po użyciu `shift`, liczba argumentów pozycyjnych (`$#`) zmniejsza się, co może wpłynąć na dalsze przetwarzanie.
- Używaj `shift` w połączeniu z `set` do dynamicznego zarządzania argumentami w skryptach.