# [Polski] Debian Almquist Shell (dash) grep Użycie: Wyszukiwanie wzorców w plikach

## Przegląd
Polecenie `grep` służy do wyszukiwania wzorców w plikach tekstowych. Umożliwia filtrowanie danych na podstawie określonych wyrażeń regularnych, co czyni je niezwykle przydatnym narzędziem w pracy z tekstem.

## Użycie
Podstawowa składnia polecenia `grep` jest następująca:

```bash
grep [opcje] [argumenty]
```

## Wspólne opcje
- `-i`: Ignoruje wielkość liter podczas wyszukiwania.
- `-v`: Zwraca linie, które **nie** pasują do wzorca.
- `-r`: Przeszukuje katalogi rekurencyjnie.
- `-n`: Wyświetla numery linii, w których występuje dopasowanie.
- `-l`: Zwraca tylko nazwy plików, które zawierają dopasowanie.

## Przykłady
Oto kilka praktycznych przykładów użycia `grep`:

1. Wyszukiwanie prostego wzorca w pliku:
   ```bash
   grep "tekst" plik.txt
   ```

2. Wyszukiwanie wzorca bez uwzględniania wielkości liter:
   ```bash
   grep -i "tekst" plik.txt
   ```

3. Wyszukiwanie wzorca w wielu plikach:
   ```bash
   grep "tekst" *.txt
   ```

4. Wyszukiwanie wzorca rekurencyjnie w katalogu:
   ```bash
   grep -r "tekst" /ścieżka/do/katalogu
   ```

5. Wyświetlanie numerów linii z dopasowaniami:
   ```bash
   grep -n "tekst" plik.txt
   ```

## Wskazówki
- Używaj opcji `-i`, gdy nie chcesz, aby wielkość liter wpływała na wyniki wyszukiwania.
- Opcja `-v` jest przydatna, gdy chcesz znaleźć linie, które nie zawierają określonego wzorca.
- Pamiętaj, że `grep` obsługuje wyrażenia regularne, co pozwala na bardziej zaawansowane wyszukiwanie.
- Aby poprawić wydajność, ograniczaj wyszukiwanie do konkretnych plików lub katalogów, zamiast przeszukiwać cały system plików.