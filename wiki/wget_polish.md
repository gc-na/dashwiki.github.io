# [Debian] Debian Almquist Shell (dash) wget użycie: Pobieranie plików z internetu

## Overview
Polecenie `wget` jest narzędziem do pobierania plików z internetu. Umożliwia ściąganie plików z protokołów HTTP, HTTPS oraz FTP, a także obsługuje pobieranie plików w tle.

## Usage
Podstawowa składnia polecenia `wget` jest następująca:

```bash
wget [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `wget`:

- `-O <plik>`: Zapisuje pobrany plik pod wskazaną nazwą.
- `-c`: Wznawia przerwane pobieranie.
- `-q`: Wykonuje operację w trybie cichym, bez wyświetlania komunikatów.
- `--limit-rate=<prędkość>`: Ogranicza prędkość pobierania do określonej wartości.
- `-r`: Włącza rekurencyjne pobieranie, co pozwala na ściąganie całych stron internetowych.

## Common Examples
Oto kilka praktycznych przykładów użycia `wget`:

### Pobieranie pojedynczego pliku
Aby pobrać plik z internetu, użyj:

```bash
wget https://example.com/plik.txt
```

### Zapisanie pliku pod inną nazwą
Aby zapisać plik pod inną nazwą, użyj opcji `-O`:

```bash
wget -O nowa_nazwa.txt https://example.com/plik.txt
```

### Wznawianie przerwanego pobierania
Aby wznowić przerwane pobieranie, użyj opcji `-c`:

```bash
wget -c https://example.com/plik.txt
```

### Ograniczenie prędkości pobierania
Aby ograniczyć prędkość pobierania do 100 KB/s, użyj:

```bash
wget --limit-rate=100k https://example.com/plik.txt
```

### Rekurencyjne pobieranie strony
Aby pobrać całą stronę internetową, użyj opcji `-r`:

```bash
wget -r https://example.com/
```

## Tips
- Używaj opcji `-q`, gdy chcesz, aby `wget` działał w tle bez zbędnych komunikatów.
- Sprawdzaj dostępność plików przed pobraniem, aby uniknąć błędów 404.
- Zawsze używaj opcji `-c`, gdy istnieje ryzyko przerwania pobierania, aby zaoszczędzić czas i zasoby.