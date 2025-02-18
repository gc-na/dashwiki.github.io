# [Debian] Debian Almquist Shell (dash) cmp <Comparer des fichiers>: Compare le contenu de deux fichiers

## Overview
La commande `cmp` est utilisée pour comparer le contenu de deux fichiers byte par byte. Elle permet de déterminer si les fichiers sont identiques ou de localiser la première différence entre eux.

## Usage
La syntaxe de base de la commande `cmp` est la suivante :

```bash
cmp [options] [arguments]
```

## Common Options
- `-l` : Affiche les octets différents en format numérique.
- `-s` : Ne produit aucune sortie, mais renvoie un code de sortie indiquant si les fichiers sont identiques ou non.
- `-i <offset>` : Ignore les premiers `<offset>` octets des fichiers.
- `-n <number>` : Compare seulement les premiers `<number>` octets des fichiers.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cmp` :

1. Comparer deux fichiers et afficher la première différence :
   ```bash
   cmp fichier1.txt fichier2.txt
   ```

2. Comparer deux fichiers sans afficher de sortie, mais en vérifiant l'égalité :
   ```bash
   cmp -s fichier1.txt fichier2.txt
   ```

3. Afficher les octets différents entre deux fichiers :
   ```bash
   cmp -l fichier1.txt fichier2.txt
   ```

4. Comparer les premiers 100 octets de deux fichiers :
   ```bash
   cmp -n 100 fichier1.txt fichier2.txt
   ```

5. Ignorer les premiers 10 octets lors de la comparaison :
   ```bash
   cmp -i 10 fichier1.txt fichier2.txt
   ```

## Tips
- Utilisez l'option `-s` pour intégrer `cmp` dans des scripts où vous avez besoin de vérifier l'égalité sans afficher de détails.
- Pour des fichiers très volumineux, utilisez l'option `-n` pour limiter la comparaison à un nombre spécifié d'octets, ce qui peut accélérer le processus.
- Si vous devez comparer plusieurs fichiers, envisagez d'utiliser une boucle pour automatiser le processus avec `cmp`.