# [Română] Debian Almquist Shell (dash) cd utilizare: Schimbă directorul curent

## Overview
Comanda `cd` (change directory) este utilizată pentru a schimba directorul curent în shell. Aceasta permite utilizatorului să navigheze între diferite directoare din sistemul de fișiere.

## Usage
Sintaxa de bază a comenzii `cd` este următoarea:

```
cd [opțiuni] [argumente]
```

## Common Options
- `-`: Schimbă la directorul anterior.
- `~`: Schimbă la directorul home al utilizatorului curent.
- `..`: Schimbă la directorul părinte al directorului curent.

## Common Examples
- Schimbarea la directorul home:
  ```sh
  cd ~
  ```

- Schimbarea la un director specific:
  ```sh
  cd /path/catre/director
  ```

- Revenirea la directorul anterior:
  ```sh
  cd -
  ```

- Navigarea la directorul părinte:
  ```sh
  cd ..
  ```

## Tips
- Folosește `cd -` pentru a naviga rapid între două directoare.
- Poți utiliza `cd` fără argumente pentru a reveni la directorul home.
- Verifică întotdeauna calea curentă folosind comanda `pwd` după ce ai folosit `cd` pentru a te asigura că te afli în directorul dorit.