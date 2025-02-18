# [Debian] Debian Almquist Shell (dash) uname użycie: wyświetlanie informacji o systemie

## Overview
Polecenie `uname` służy do wyświetlania informacji o systemie operacyjnym, na którym jest uruchomione. Może dostarczać szczegółowe dane, takie jak nazwa jądra, nazwa hosta, wersja systemu i inne istotne informacje.

## Usage
Podstawowa składnia polecenia `uname` jest następująca:

```bash
uname [opcje]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `uname`:

- `-a`: Wyświetla wszystkie dostępne informacje o systemie.
- `-s`: Wyświetla nazwę jądra systemu.
- `-n`: Wyświetla nazwę hosta.
- `-r`: Wyświetla wersję jądra.
- `-v`: Wyświetla dodatkowe informacje o wersji jądra.
- `-m`: Wyświetla architekturę maszyny.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `uname`:

1. Wyświetlenie wszystkich informacji o systemie:
   ```bash
   uname -a
   ```

2. Wyświetlenie tylko nazwy jądra:
   ```bash
   uname -s
   ```

3. Wyświetlenie wersji jądra:
   ```bash
   uname -r
   ```

4. Wyświetlenie architektury maszyny:
   ```bash
   uname -m
   ```

## Tips
- Używaj opcji `-a`, aby uzyskać pełny przegląd informacji o systemie w jednym poleceniu.
- Możesz łączyć różne opcje, aby uzyskać bardziej szczegółowe dane, na przykład `uname -sr` wyświetli zarówno nazwę jądra, jak i jego wersję.
- Pamiętaj, że `uname` jest przydatne w skryptach do automatyzacji, gdzie potrzebujesz informacji o systemie.