# [Debian] Debian Almquist Shell (dash) watch utilisation : surveiller les commandes

## Overview
La commande `watch` permet d'exécuter périodiquement une commande et d'afficher sa sortie dans le terminal. Cela est particulièrement utile pour surveiller les changements dans les résultats d'une commande au fil du temps.

## Usage
La syntaxe de base de la commande `watch` est la suivante :

```bash
watch [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `watch` :

- `-n <seconds>` : Définit l'intervalle en secondes entre les exécutions de la commande. Par défaut, l'intervalle est de 2 secondes.
- `-d` : Met en surbrillance les différences entre les sorties successives.
- `-t` : Supprime l'affichage de l'en-tête de la commande, ne montrant que la sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `watch` :

1. Surveiller l'utilisation de l'espace disque :
   ```bash
   watch df -h
   ```

2. Vérifier les processus en cours :
   ```bash
   watch -n 5 ps aux
   ```

3. Surveiller les changements dans un répertoire :
   ```bash
   watch -d ls -l /path/to/directory
   ```

4. Afficher l'utilisation de la mémoire :
   ```bash
   watch -n 1 free -m
   ```

## Tips
- Utilisez l'option `-d` pour mieux visualiser les changements, surtout lorsque vous surveillez des sorties qui changent fréquemment.
- Si vous surveillez une commande qui prend du temps à s'exécuter, augmentez l'intervalle avec `-n` pour éviter une surcharge inutile.
- Pensez à utiliser `Ctrl+C` pour arrêter la commande `watch` à tout moment.