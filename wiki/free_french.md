# [Français] Debian Almquist Shell (dash) free : Afficher l'utilisation de la mémoire

## Overview
La commande `free` permet d'afficher des informations sur l'utilisation de la mémoire dans le système. Elle fournit des données sur la mémoire totale, utilisée, libre, ainsi que sur la mémoire swap.

## Usage
La syntaxe de base de la commande `free` est la suivante :

```bash
free [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `free` :

- `-h` : Affiche les valeurs dans un format lisible par l'homme (par exemple, en Ko, Mo, Go).
- `-m` : Affiche les valeurs en mégaoctets.
- `-g` : Affiche les valeurs en gigaoctets.
- `-s <seconds>` : Met à jour les informations à intervalles réguliers spécifiés en secondes.
- `-t` : Affiche un total de la mémoire.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `free` :

1. Afficher l'utilisation de la mémoire en format lisible par l'homme :
   ```bash
   free -h
   ```

2. Afficher l'utilisation de la mémoire en mégaoctets :
   ```bash
   free -m
   ```

3. Afficher l'utilisation de la mémoire avec un total :
   ```bash
   free -t
   ```

4. Mettre à jour les informations toutes les 5 secondes :
   ```bash
   free -s 5
   ```

## Tips
- Utilisez l'option `-h` pour obtenir des informations plus faciles à lire, surtout si vous travaillez avec de grandes quantités de mémoire.
- Combinez `free` avec d'autres commandes comme `watch` pour surveiller l'utilisation de la mémoire en temps réel :
  ```bash
  watch free -h
  ```
- Pensez à vérifier régulièrement l'utilisation de la mémoire pour identifier d'éventuels problèmes de performance dans votre système.