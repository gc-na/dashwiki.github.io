# [Français] Debian Almquist Shell (dash) uptime : Afficher le temps de fonctionnement du système

## Overview
La commande `uptime` permet d'afficher depuis combien de temps le système est en fonctionnement, ainsi que le nombre d'utilisateurs connectés et la charge moyenne du système sur les 1, 5 et 15 dernières minutes.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
uptime [options] [arguments]
```

## Common Options
- `-p` : Affiche le temps de fonctionnement de manière plus lisible.
- `-s` : Affiche la date et l'heure du dernier démarrage du système.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `uptime` :

### Exemple 1 : Afficher le temps de fonctionnement
```bash
uptime
```
Cela affichera une ligne contenant le temps de fonctionnement, le nombre d'utilisateurs connectés et la charge moyenne.

### Exemple 2 : Afficher le temps de fonctionnement de manière lisible
```bash
uptime -p
```
Cette commande affichera le temps de fonctionnement sous une forme plus compréhensible, par exemple "up 5 hours, 20 minutes".

### Exemple 3 : Afficher la date et l'heure du dernier démarrage
```bash
uptime -s
```
Cela montrera la date et l'heure exactes du dernier redémarrage du système.

## Tips
- Utilisez `uptime` régulièrement pour surveiller la stabilité de votre système.
- Combinez `uptime` avec d'autres commandes comme `top` pour une analyse plus approfondie des performances du système.
- Pensez à utiliser l'option `-p` pour des rapports plus clairs lors de la présentation des résultats à d'autres utilisateurs.