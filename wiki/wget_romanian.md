# [Linux] Debian Almquist Shell (dash) wget utilizare: Descărcarea fișierelor de pe internet

## Overview
Comanda `wget` este un instrument puternic folosit pentru a descărca fișiere de pe internet. Aceasta suportă protocoale precum HTTP, HTTPS și FTP, permițând utilizatorilor să obțină conținut de pe servere web.

## Usage
Sintaxa de bază pentru utilizarea comenzii `wget` este următoarea:

```
wget [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru `wget`:

- `-O <fișier>`: Salvează fișierul descărcat sub un alt nume.
- `-c`: Continuă o descărcare întreruptă.
- `-q`: Rulează în mod silențios, fără a afișa progresul.
- `--limit-rate=<viteză>`: Limitează viteza de descărcare.
- `-r`: Descarcă recursiv, inclusiv toate fișierele legate.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `wget`:

1. **Descărcarea unui fișier**:
   ```bash
   wget https://example.com/fișier.txt
   ```

2. **Descărcarea unui fișier și salvarea sub un alt nume**:
   ```bash
   wget -O nou_fișier.txt https://example.com/fișier.txt
   ```

3. **Continuarea unei descărcări întrerupte**:
   ```bash
   wget -c https://example.com/fișier_mare.zip
   ```

4. **Descarcă recursiv toate fișierele dintr-un director**:
   ```bash
   wget -r https://example.com/directory/
   ```

5. **Descărcarea unui fișier cu limitarea vitezei**:
   ```bash
   wget --limit-rate=200k https://example.com/fișier.txt
   ```

## Tips
- Asigurați-vă că aveți permisiunea de a descărca fișierele de pe site-urile web pentru a evita problemele legale.
- Utilizați opțiunea `-q` pentru a rula descărcările în fundal fără a fi deranjat de mesaje de progres.
- Verificați întotdeauna integritatea fișierelor descărcate, mai ales dacă sunt mari sau importante.