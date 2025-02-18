# [Polski] Debian Almquist Shell (dash) whoami <Użycie>: identyfikacja użytkownika

## Przegląd
Polecenie `whoami` służy do wyświetlania nazwy aktualnie zalogowanego użytkownika w systemie. Jest to przydatne narzędzie, gdy chcemy szybko sprawdzić, pod jakim kontem wykonujemy polecenia w terminalu.

## Użycie
Podstawowa składnia polecenia `whoami` jest następująca:

```
whoami [opcje] [argumenty]
```

## Częste opcje
Polecenie `whoami` nie ma wielu opcji, ale oto najczęściej używane:

- `--help`: Wyświetla pomoc dotyczącą polecenia.
- `--version`: Pokazuje wersję polecenia.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `whoami`:

1. Aby wyświetlić nazwę aktualnego użytkownika:
   ```bash
   whoami
   ```

2. Aby uzyskać pomoc dotyczącą polecenia:
   ```bash
   whoami --help
   ```

3. Aby sprawdzić wersję polecenia:
   ```bash
   whoami --version
   ```

## Wskazówki
- Używaj `whoami` w skryptach, aby dynamicznie identyfikować użytkownika wykonującego skrypt.
- Możesz użyć `whoami` w połączeniu z innymi poleceniami, aby dostosować działanie skryptów w zależności od użytkownika.
- Pamiętaj, że `whoami` zwraca tylko nazwę użytkownika, a nie inne informacje, takie jak identyfikator użytkownika (UID).