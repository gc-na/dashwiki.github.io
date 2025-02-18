# [Linux] Debian Almquist Shell (dash) curl utilizare: Transferă date prin rețea

## Overview
Comanda `curl` este un instrument de linie de comandă utilizat pentru a transfera date prin rețea folosind diverse protocoale, cum ar fi HTTP, HTTPS, FTP și multe altele. Este foarte util pentru descărcarea fișierelor sau pentru interacțiunea cu API-uri web.

## Usage
Sintaxa de bază a comenzii `curl` este următoarea:

```bash
curl [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru `curl`:

- `-O`: Salvează fișierul descărcat cu același nume ca pe server.
- `-L`: Urmează redirecționările.
- `-d`: Trimite date în corpul unei cereri POST.
- `-H`: Adaugă un antet personalizat la cererea HTTP.
- `-u`: Autentificare utilizator (username:password).

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `curl`:

1. **Descărcarea unui fișier:**

```bash
curl -O http://example.com/fișier.txt
```

2. **Obținerea conținutului unei pagini web:**

```bash
curl http://example.com
```

3. **Trimiterea unei cereri POST cu date:**

```bash
curl -d "nume=John&vârstă=30" http://example.com/api
```

4. **Adăugarea unui antet personalizat:**

```bash
curl -H "Authorization: Bearer token" http://example.com/api
```

5. **Urmează redirecționările:**

```bash
curl -L http://example.com/redirect
```

## Tips
- Folosește opțiunea `-I` pentru a obține doar anteturile răspunsului, fără a descărca corpul.
- Verifică opțiunea `--verbose` pentru a obține informații detaliate despre cererea și răspunsul HTTP.
- Asigură-te că utilizezi `https` pentru a transfera datele în siguranță atunci când este posibil.