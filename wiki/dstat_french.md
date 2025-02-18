# [Français] Debian Almquist Shell (dash) dstat : surveiller les ressources système

## Overview
La commande `dstat` est un outil puissant qui permet de surveiller en temps réel les ressources système, telles que l'utilisation du processeur, la mémoire, le réseau, et bien plus encore. Elle combine les fonctionnalités de plusieurs outils de surveillance, offrant une vue d'ensemble complète des performances de votre système.

## Usage
La syntaxe de base de la commande `dstat` est la suivante :

```bash
dstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `dstat` :

- `-c` : Affiche l'utilisation du processeur.
- `-d` : Affiche l'activité du disque.
- `-n` : Affiche l'activité réseau.
- `-m` : Affiche l'utilisation de la mémoire.
- `-t` : Affiche l'horodatage.
- `--full` : Affiche toutes les statistiques disponibles.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `dstat` :

1. Afficher l'utilisation du processeur et de la mémoire :
   ```bash
   dstat -c -m
   ```

2. Surveiller l'activité du disque et du réseau :
   ```bash
   dstat -d -n
   ```

3. Afficher toutes les statistiques avec un horodatage :
   ```bash
   dstat -t --full
   ```

4. Surveiller le système pendant 10 secondes :
   ```bash
   dstat 10
   ```

## Tips
- Utilisez `dstat` avec des options combinées pour obtenir une vue plus complète de l'état de votre système.
- Pensez à rediriger la sortie vers un fichier pour une analyse ultérieure, par exemple :
  ```bash
  dstat -c -d > dstat_output.txt
  ```
- Familiarisez-vous avec les différentes options pour personnaliser la sortie selon vos besoins spécifiques.