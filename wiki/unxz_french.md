# [Français] Debian Almquist Shell (dash) unxz : Décompresser des fichiers .xz

## Overview
La commande `unxz` est utilisée pour décompresser des fichiers compressés au format `.xz`. Elle est souvent utilisée pour réduire la taille des fichiers et faciliter leur stockage ou leur transfert.

## Usage
La syntaxe de base de la commande `unxz` est la suivante :

```bash
unxz [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `unxz` :

- `-k`, `--keep` : Conserve le fichier d'origine après décompression.
- `-f`, `--force` : Force la décompression, même si le fichier de destination existe déjà.
- `-v`, `--verbose` : Affiche des informations détaillées sur le processus de décompression.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `unxz` :

1. Décompresser un fichier `.xz` :

    ```bash
    unxz fichier.xz
    ```

2. Décompresser un fichier tout en conservant l'original :

    ```bash
    unxz -k fichier.xz
    ```

3. Décompresser un fichier et forcer l'écrasement d'un fichier existant :

    ```bash
    unxz -f fichier.xz
    ```

4. Afficher des informations détaillées lors de la décompression :

    ```bash
    unxz -v fichier.xz
    ```

## Tips
- Assurez-vous d'avoir suffisamment d'espace disque avant de décompresser un fichier, surtout si vous utilisez l'option `-k`.
- Utilisez l'option `-v` pour surveiller le progrès de la décompression, surtout avec de gros fichiers.
- Si vous travaillez avec plusieurs fichiers, envisagez d'utiliser un script pour automatiser le processus de décompression.