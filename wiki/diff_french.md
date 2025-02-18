# [Debian] Debian Almquist Shell (dash) diff : comparer des fichiers

## Overview
La commande `diff` est utilisée pour comparer le contenu de deux fichiers ligne par ligne. Elle affiche les différences entre ces fichiers, ce qui est particulièrement utile pour les développeurs et les administrateurs système qui souhaitent voir les modifications apportées à un fichier.

## Usage
La syntaxe de base de la commande `diff` est la suivante :

```bash
diff [options] [fichier1] [fichier2]
```

## Common Options
Voici quelques options courantes pour la commande `diff` :

- `-u` : Affiche les différences en mode "unifié", ce qui rend la sortie plus lisible.
- `-i` : Ignore la casse lors de la comparaison.
- `-w` : Ignore les espaces blancs lors de la comparaison.
- `-r` : Compare les répertoires de manière récursive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `diff` :

1. Comparer deux fichiers texte :
   ```bash
   diff fichier1.txt fichier2.txt
   ```

2. Afficher les différences en mode unifié :
   ```bash
   diff -u fichier1.txt fichier2.txt
   ```

3. Ignorer les espaces blancs lors de la comparaison :
   ```bash
   diff -w fichier1.txt fichier2.txt
   ```

4. Comparer deux répertoires :
   ```bash
   diff -r dossier1/ dossier2/
   ```

## Tips
- Utilisez l'option `-u` pour obtenir une sortie plus lisible, surtout si vous devez partager les différences avec d'autres.
- Lorsque vous travaillez avec des fichiers de code source, l'option `-i` peut être utile pour éviter des différences dues à des variations de casse.
- Pensez à utiliser `diff` avec des outils de contrôle de version pour suivre les modifications dans vos projets.