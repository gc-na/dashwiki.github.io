# [Debian] Debian Almquist Shell (dash) scp użycie: Przesyłanie plików przez SSH

## Overview
Polecenie `scp` (Secure Copy Protocol) służy do bezpiecznego przesyłania plików pomiędzy lokalnym a zdalnym systemem lub pomiędzy dwoma zdalnymi systemami przy użyciu protokołu SSH. Dzięki temu, dane są szyfrowane podczas transferu, co zapewnia ich bezpieczeństwo.

## Usage
Podstawowa składnia polecenia `scp` wygląda następująco:

```bash
scp [opcje] [źródło] [cel]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `scp`:

- `-r`: Rekursywne kopiowanie katalogów.
- `-P`: Określenie portu SSH (domyślnie 22).
- `-i`: Użycie określonego pliku klucza prywatnego do autoryzacji.
- `-v`: Włączenie trybu szczegółowego, który wyświetla więcej informacji o postępie operacji.

## Common Examples

1. **Kopiowanie pliku z lokalnego systemu na zdalny serwer:**

```bash
scp lokalny_plik.txt użytkownik@zdalny_serwer:/ścieżka/do/katalogu/
```

2. **Kopiowanie pliku z zdalnego serwera na lokalny system:**

```bash
scp użytkownik@zdalny_serwer:/ścieżka/do/zdalnego_pliku.txt /lokalna/ścieżka/
```

3. **Rekurencyjne kopiowanie katalogu na zdalny serwer:**

```bash
scp -r lokalny_katalog/ użytkownik@zdalny_serwer:/ścieżka/do/katalogu/
```

4. **Kopiowanie pliku z określonym portem:**

```bash
scp -P 2222 lokalny_plik.txt użytkownik@zdalny_serwer:/ścieżka/do/katalogu/
```

## Tips
- Używaj opcji `-v`, aby uzyskać więcej informacji o błędach, jeśli napotkasz problemy podczas przesyłania plików.
- Zawsze upewnij się, że masz odpowiednie uprawnienia do zapisu w katalogu docelowym na zdalnym serwerze.
- Rozważ użycie kluczy SSH zamiast hasła dla większego bezpieczeństwa i wygody podczas łączenia się z zdalnymi serwerami.