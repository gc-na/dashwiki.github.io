# [Debian] Debian Almquist Shell (dash) pwd użycie: wyświetlanie bieżącej ścieżki katalogu

## Przegląd
Polecenie `pwd` (print working directory) w powłoce Debian Almquist Shell (dash) służy do wyświetlania pełnej ścieżki do bieżącego katalogu roboczego. Jest to przydatne narzędzie, które pozwala użytkownikom szybko zorientować się, w którym katalogu aktualnie się znajdują.

## Użycie
Podstawowa składnia polecenia `pwd` jest następująca:

```bash
pwd [opcje]
```

## Częste opcje
- `-L` - wyświetla ścieżkę do bieżącego katalogu roboczego, uwzględniając dowiązania symboliczne.
- `-P` - wyświetla rzeczywistą ścieżkę do katalogu roboczego, ignorując dowiązania symboliczne.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `pwd`:

1. Wyświetlenie bieżącej ścieżki katalogu:
   ```bash
   pwd
   ```

2. Wyświetlenie ścieżki z uwzględnieniem dowiązań symbolicznych:
   ```bash
   pwd -L
   ```

3. Wyświetlenie rzeczywistej ścieżki katalogu:
   ```bash
   pwd -P
   ```

## Wskazówki
- Używaj `pwd` regularnie, aby upewnić się, że pracujesz w odpowiednim katalogu, zwłaszcza podczas skryptowania.
- Zawsze sprawdzaj, czy używasz odpowiedniej opcji (`-L` lub `-P`), aby uzyskać pożądany wynik, zwłaszcza w złożonych strukturach katalogów z dowiązaniami symbolicznymi.