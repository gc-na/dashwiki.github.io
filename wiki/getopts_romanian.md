# [România] Debian Almquist Shell (dash) getopts utilizare: [analiza argumentelor de linie de comandă]

## Overview
Comanda `getopts` este utilizată în shell-urile Unix pentru a analiza opțiunile și argumentele din linia de comandă. Aceasta permite scripturilor să preia argumente opționale și să le gestioneze într-un mod structurat.

## Usage
Sintaxa de bază a comenzii `getopts` este următoarea:

```sh
getopts [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru `getopts`:

- `-a`: Activează modul de analiză a argumentelor.
- `-d`: Afișează informații de depanare.
- `-n`: Specifică numele programului pentru mesajele de eroare.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `getopts`:

### Exemplul 1: Analiza opțiunilor simple
```sh
#!/bin/sh
while getopts "ab:c:" opt; do
  case $opt in
    a)
      echo "Opțiunea a a fost selectată."
      ;;
    b)
      echo "Opțiunea b a fost selectată cu argumentul: $OPTARG"
      ;;
    c)
      echo "Opțiunea c a fost selectată cu argumentul: $OPTARG"
      ;;
    *)
      echo "Opțiune invalidă."
      ;;
  esac
done
```

### Exemplul 2: Utilizarea cu argumente
```sh
#!/bin/sh
while getopts "f:d:" opt; do
  case $opt in
    f)
      echo "Fișierul specificat este: $OPTARG"
      ;;
    d)
      echo "Directorul specificat este: $OPTARG"
      ;;
    *)
      echo "Opțiune invalidă."
      ;;
  esac
done
```

### Exemplul 3: Opțiuni fără argumente
```sh
#!/bin/sh
while getopts "x:y" opt; do
  case $opt in
    x)
      echo "Opțiunea x a fost selectată cu argumentul: $OPTARG"
      ;;
    y)
      echo "Opțiunea y a fost selectată fără argument."
      ;;
    *)
      echo "Opțiune invalidă."
      ;;
  esac
done
```

## Tips
- Asigurați-vă că opțiunile care necesită argumente sunt urmate de `:` în specificația opțiunilor.
- Utilizați `OPTARG` pentru a accesa argumentele asociate opțiunilor.
- Verificați întotdeauna opțiunile invalide pentru a îmbunătăți experiența utilizatorului.