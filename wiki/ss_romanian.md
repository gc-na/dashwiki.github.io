# [Linux] Debian Almquist Shell (dash) ss utilizare: Afișează conexiunile de rețea

## Overview
Comanda `ss` este utilizată pentru a afișa informații despre conexiunile de rețea, inclusiv socket-urile TCP, UDP și alte protocoale. Este un instrument util pentru diagnosticarea problemelor de rețea și pentru monitorizarea activității rețelei pe un sistem.

## Usage
Sintaxa de bază a comenzii `ss` este următoarea:

```bash
ss [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru comanda `ss`:

- `-t`: Afișează doar conexiunile TCP.
- `-u`: Afișează doar conexiunile UDP.
- `-l`: Afișează socket-urile care ascultă.
- `-p`: Afișează informații despre procesele asociate cu socket-urile.
- `-n`: Afișează adresele și porturile în format numeric, fără a le rezolva în nume.

## Common Examples
Iată câteva exemple practice ale utilizării comenzii `ss`:

1. Afișarea tuturor conexiunilor TCP active:
   ```bash
   ss -t
   ```

2. Afișarea socket-urilor UDP:
   ```bash
   ss -u
   ```

3. Afișarea socket-urilor care ascultă:
   ```bash
   ss -l
   ```

4. Afișarea conexiunilor TCP împreună cu procesele asociate:
   ```bash
   ss -tp
   ```

5. Afișarea tuturor conexiunilor, inclusiv cele în starea de ascultare:
   ```bash
   ss -a
   ```

## Tips
- Folosește opțiunea `-n` pentru a obține rezultate mai rapide, evitând rezolvarea numelui gazdelor.
- Combină opțiunile pentru a obține informații mai detaliate, de exemplu `ss -tunlp` pentru a vedea toate conexiunile TCP și UDP, împreună cu procesele.
- Verifică periodic conexiunile active pentru a identifica eventuale probleme de securitate sau activități suspecte.