# [Debian] Debian Almquist Shell (dash) head : afficher les premières lignes d'un fichier

## Overview
La commande `head` permet d'afficher les premières lignes d'un fichier texte. Par défaut, elle montre les 10 premières lignes, mais cela peut être modifié selon les besoins de l'utilisateur.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
head [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `head` :

- `-n N` : Affiche les N premières lignes du fichier. Par défaut, N est 10.
- `-c N` : Affiche les N premiers octets du fichier.
- `-q` : Ne pas afficher le nom des fichiers lors de l'affichage de plusieurs fichiers.
- `-v` : Affiche le nom du fichier avant son contenu, même pour un seul fichier.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `head` :

1. Afficher les 10 premières lignes d'un fichier nommé `exemple.txt` :

    ```bash
    head exemple.txt
    ```

2. Afficher les 5 premières lignes d'un fichier :

    ```bash
    head -n 5 exemple.txt
    ```

3. Afficher les 20 premiers octets d'un fichier :

    ```bash
    head -c 20 exemple.txt
    ```

4. Afficher les 3 premières lignes de plusieurs fichiers :

    ```bash
    head -n 3 fichier1.txt fichier2.txt
    ```

5. Afficher le contenu d'un fichier sans afficher son nom :

    ```bash
    head -q fichier.txt
    ```

## Tips
- Utilisez `head` en combinaison avec d'autres commandes, comme `grep`, pour filtrer les résultats avant d'afficher les premières lignes.
- Pour une visualisation rapide des fichiers volumineux, `head` est très utile pour obtenir un aperçu sans avoir à ouvrir le fichier entier.
- Pensez à utiliser l'option `-v` si vous travaillez avec plusieurs fichiers et souhaitez garder une trace de leur provenance dans la sortie.