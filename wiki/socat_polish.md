# [Polski] Debian Almquist Shell (dash) socat użycie: Narzędzie do przesyłania danych między różnymi źródłami

## Overview
`socat` to potężne narzędzie w systemie Linux, które umożliwia przesyłanie danych między różnymi źródłami, takimi jak gniazda, pliki, czy urządzenia. Działa jako "socket cat", co oznacza, że może łączyć różne strumienie danych i przekazywać je w czasie rzeczywistym.

## Usage
Podstawowa składnia polecenia `socat` jest następująca:

```bash
socat [opcje] [argumenty]
```

## Common Options
- `-d` : Włącz tryb debugowania, aby uzyskać więcej informacji o działaniu polecenia.
- `-v` : Włącz tryb wyjścia, aby zobaczyć przesyłane dane.
- `TCP:<adres>:<port>` : Umożliwia połączenie z zdalnym hostem przez protokół TCP.
- `UDP:<adres>:<port>` : Umożliwia połączenie z zdalnym hostem przez protokół UDP.
- `FILE:<ścieżka>` : Umożliwia przesyłanie danych z lub do pliku.

## Common Examples

### Przykład 1: Proste połączenie TCP
Aby utworzyć połączenie TCP z lokalnym serwerem na porcie 8080, użyj:

```bash
socat - TCP:localhost:8080
```

### Przykład 2: Przesyłanie danych z pliku
Aby przesłać zawartość pliku do gniazda TCP:

```bash
socat TCP:localhost:8080 FILE:/ścieżka/do/pliku.txt
```

### Przykład 3: Odbieranie danych z gniazda i zapis do pliku
Aby odbierać dane z gniazda TCP i zapisywać je do pliku:

```bash
socat FILE:/ścieżka/do/plik.txt TCP-LISTEN:8080
```

### Przykład 4: Przesyłanie danych między dwoma gniazdami
Aby przesyłać dane między dwoma gniazdami TCP:

```bash
socat TCP-LISTEN:8080,fork TCP:remotehost:9090
```

## Tips
- Używaj opcji `-d -v`, aby uzyskać więcej informacji na temat działania `socat`, co może pomóc w rozwiązywaniu problemów.
- Zawsze testuj połączenia w środowisku lokalnym przed wdrożeniem w produkcji.
- Pamiętaj o zabezpieczeniach, gdy używasz `socat` do przesyłania danych przez sieć, aby uniknąć nieautoryzowanego dostępu.