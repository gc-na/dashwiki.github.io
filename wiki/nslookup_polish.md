# [Polski] Debian Almquist Shell (dash) nslookup użycie: Sprawdzanie adresów IP i nazw domen

## Przegląd
Polecenie `nslookup` służy do uzyskiwania informacji o systemach nazw domen (DNS). Umożliwia użytkownikom sprawdzanie adresów IP dla nazw domen oraz odwrotnie, co jest przydatne w diagnostyce problemów z siecią.

## Użycie
Podstawowa składnia polecenia `nslookup` jest następująca:

```bash
nslookup [opcje] [argumenty]
```

## Częste opcje
- `-type=typ`: Określa typ zapytania DNS, np. `A`, `MX`, `CNAME`.
- `-timeout=czas`: Ustala czas oczekiwania na odpowiedź serwera DNS.
- `-retry=liczba`: Ustala liczbę prób ponownego zapytania w przypadku braku odpowiedzi.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `nslookup`:

1. Sprawdzenie adresu IP dla nazwy domeny:
   ```bash
   nslookup example.com
   ```

2. Uzyskanie informacji o rekordach MX dla domeny:
   ```bash
   nslookup -type=MX example.com
   ```

3. Ustalenie adresu IP dla konkretnego serwera DNS:
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. Ustalenie typu rekordu CNAME:
   ```bash
   nslookup -type=CNAME www.example.com
   ```

## Wskazówki
- Używaj opcji `-type` do precyzyjnego określenia, jakie informacje chcesz uzyskać.
- Jeśli napotkasz problemy z odpowiedzią, spróbuj zmienić serwer DNS, korzystając z opcji `nslookup [domena] [serwer]`.
- Regularnie sprawdzaj różne typy rekordów, aby lepiej zrozumieć konfigurację DNS dla danej domeny.