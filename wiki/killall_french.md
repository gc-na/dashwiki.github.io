# [Français] Debian Almquist Shell (dash) killall : Terminer des processus par nom

## Overview
La commande `killall` permet de terminer tous les processus en cours d'exécution qui correspondent à un nom de programme spécifié. Cela peut être utile pour gérer les applications qui ne répondent plus ou pour libérer des ressources système.

## Usage
La syntaxe de base de la commande `killall` est la suivante :

```bash
killall [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `killall` :

- `-9` : Force l'arrêt immédiat des processus.
- `-v` : Affiche des informations détaillées sur les processus terminés.
- `-i` : Demande une confirmation avant de terminer chaque processus.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `killall` :

1. Terminer tous les processus nommés `firefox` :

    ```bash
    killall firefox
    ```

2. Forcer l'arrêt de tous les processus nommés `gedit` :

    ```bash
    killall -9 gedit
    ```

3. Afficher les détails lors de la terminaison de tous les processus `ssh` :

    ```bash
    killall -v ssh
    ```

4. Demander confirmation avant de terminer tous les processus `vlc` :

    ```bash
    killall -i vlc
    ```

## Tips
- Utilisez l'option `-v` pour vérifier quels processus ont été terminés, surtout si vous gérez plusieurs applications.
- Soyez prudent avec l'option `-9`, car elle ne permet pas aux processus de se fermer proprement, ce qui peut entraîner la perte de données.
- Vérifiez toujours le nom exact du processus que vous souhaitez terminer pour éviter de fermer des applications importantes par erreur.