# [Français] Debian Almquist Shell (dash) pidstat : surveiller les statistiques des processus

## Overview
La commande `pidstat` est utilisée pour surveiller les statistiques des processus en cours d'exécution sur un système. Elle permet d'afficher des informations détaillées sur l'utilisation du CPU, de la mémoire et d'autres ressources pour des processus spécifiques.

## Usage
La syntaxe de base de la commande `pidstat` est la suivante :

```bash
pidstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `pidstat` :

- `-h` : Affiche l'aide et les options disponibles.
- `-r` : Affiche les statistiques de mémoire.
- `-u` : Affiche les statistiques d'utilisation du CPU.
- `-p <pid>` : Spécifie le PID (identifiant de processus) à surveiller.
- `-t` : Affiche les statistiques pour tous les threads de chaque processus.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `pidstat` :

1. Afficher l'utilisation du CPU pour tous les processus :
   ```bash
   pidstat -u
   ```

2. Surveiller un processus spécifique avec son PID :
   ```bash
   pidstat -p 1234
   ```

3. Afficher les statistiques de mémoire pour tous les processus :
   ```bash
   pidstat -r
   ```

4. Surveiller les statistiques de tous les threads d'un processus :
   ```bash
   pidstat -t -p 1234
   ```

5. Afficher les statistiques d'utilisation du CPU toutes les 5 secondes :
   ```bash
   pidstat -u 5
   ```

## Tips
- Utilisez l'option `-h` pour obtenir de l'aide sur les différentes options disponibles.
- Combinez plusieurs options pour obtenir des informations plus détaillées sur l'utilisation des ressources par les processus.
- Pour une surveillance continue, envisagez d'utiliser `pidstat` dans un script pour automatiser la collecte de données.