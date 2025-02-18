# [Debian] Debian Almquist Shell (dash) gunzip użycie: Rozpakowywanie plików gzip

## Overview
Polecenie `gunzip` służy do dekompresji plików skompresowanych za pomocą algorytmu gzip. Umożliwia przywrócenie oryginalnych plików z formatu .gz.

## Usage
Podstawowa składnia polecenia `gunzip` jest następująca:

```bash
gunzip [opcje] [argumenty]
```

## Common Options
- `-c`: Wyświetla dekompresowany plik na standardowym wyjściu (stdout) zamiast zapisywać go na dysku.
- `-f`: Wymusza dekompresję, nawet jeśli plik docelowy już istnieje.
- `-k`: Zachowuje oryginalny plik skompresowany po dekompresji.
- `-r`: Rekursywnie dekompresuje pliki w podkatalogach.

## Common Examples
- Dekompresja pojedynczego pliku:
```bash
gunzip plik.gz
```

- Dekompresja wielu plików:
```bash
gunzip plik1.gz plik2.gz plik3.gz
```

- Dekompresja pliku i zachowanie oryginału:
```bash
gunzip -k plik.gz
```

- Wyświetlenie zawartości dekompresowanego pliku na standardowym wyjściu:
```bash
gunzip -c plik.gz
```

- Rekursywna dekompresja plików w katalogu:
```bash
gunzip -r katalog/
```

## Tips
- Zawsze sprawdzaj, czy masz kopię zapasową oryginalnych plików przed ich dekompresją, zwłaszcza gdy używasz opcji `-f`.
- Używaj opcji `-c`, gdy chcesz szybko sprawdzić zawartość pliku bez zapisywania go na dysku.
- Pamiętaj, że dekompresja plików może zająć trochę czasu w zależności od ich rozmiaru, więc bądź cierpliwy.