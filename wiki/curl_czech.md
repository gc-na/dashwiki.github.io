# [Český] Debian Almquist Shell (dash) curl použití: Získání dat z URL

## Přehled
Příkaz `curl` slouží k přenosu dat pomocí různých protokolů, jako je HTTP, HTTPS, FTP a další. Umožňuje uživatelům stahovat nebo odesílat data na server a je velmi užitečný pro testování a interakci s webovými API.

## Použití
Základní syntaxe příkazu `curl` je následující:

```bash
curl [možnosti] [argumenty]
```

## Běžné možnosti
- `-o <soubor>`: Uloží výstup do zadaného souboru.
- `-I`: Získá pouze hlavičky odpovědi.
- `-L`: Sleduje přesměrování.
- `-d <data>`: Odesílá data jako POST požadavek.
- `-H <hlavička>`: Přidá vlastní hlavičku k požadavku.

## Běžné příklady
Stahování obsahu webové stránky:

```bash
curl https://example.com
```

Uložení obsahu do souboru:

```bash
curl -o soubor.html https://example.com
```

Získání pouze hlaviček odpovědi:

```bash
curl -I https://example.com
```

Odeslání dat pomocí POST požadavku:

```bash
curl -d "jméno=Jan&věk=30" https://example.com/api
```

Sledování přesměrování:

```bash
curl -L https://example.com
```

## Tipy
- Používejte `-o` možnost pro uložení výstupu do souboru, pokud plánujete pracovat s většími daty.
- Při testování API můžete kombinovat `-H` pro přidání potřebných hlaviček, jako je `Content-Type`.
- Nezapomeňte na možnost `-L`, pokud očekáváte, že URL může být přesměrována na jinou adresu.