# [Debian] Debian Almquist Shell (dash) tr : [convertir des caractères]

## Overview
La commande `tr` (translate) est utilisée pour traduire ou supprimer des caractères dans un flux de texte. Elle est souvent utilisée pour modifier des chaînes de caractères en remplaçant certains caractères par d'autres ou en supprimant des caractères indésirables.

## Usage
La syntaxe de base de la commande `tr` est la suivante :

```bash
tr [options] [arguments]
```

## Common Options
- `-d` : Supprime les caractères spécifiés.
- `-s` : Réduit les séquences de caractères adjacents en un seul caractère.
- `-c` : Complète le jeu de caractères spécifié.
- `-t` : Remplace les caractères spécifiés par d'autres.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `tr` :

1. **Remplacer des caractères :**
   Remplacer toutes les lettres minuscules par des lettres majuscules.
   ```bash
   echo "bonjour" | tr 'a-z' 'A-Z'
   ```

2. **Supprimer des caractères :**
   Supprimer toutes les voyelles d'une chaîne.
   ```bash
   echo "Bonjour le monde" | tr -d 'aeiouy'
   ```

3. **Réduire les espaces :**
   Réduire les espaces multiples en un seul espace.
   ```bash
   echo "Bonjour    le    monde" | tr -s ' '
   ```

4. **Compléter des caractères :**
   Remplacer tous les caractères qui ne sont pas des chiffres par un espace.
   ```bash
   echo "abc123def456" | tr -c '0-9' ' '
   ```

## Tips
- Utilisez `tr` en combinaison avec d'autres commandes comme `grep` ou `sort` pour des manipulations de texte plus avancées.
- Faites attention à la casse des caractères lors de l'utilisation de `tr`, car il est sensible à la casse.
- Pour traiter des fichiers, vous pouvez rediriger l'entrée standard à partir d'un fichier en utilisant `<` :
  ```bash
  tr 'a-z' 'A-Z' < fichier.txt
  ```