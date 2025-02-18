# [Français] Debian Almquist Shell (dash) echo : Afficher des lignes de texte

## Overview
La commande `echo` dans le shell Debian Almquist (dash) est utilisée pour afficher des lignes de texte ou des variables dans le terminal. C'est un outil simple mais puissant pour la sortie de texte.

## Usage
La syntaxe de base de la commande `echo` est la suivante :

```bash
echo [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `echo` :

- `-n` : Ne pas ajouter de nouvelle ligne à la fin de la sortie.
- `-e` : Interpréter les séquences d'échappement (comme `\n` pour une nouvelle ligne).
- `-E` : Désactiver l'interprétation des séquences d'échappement (comportement par défaut).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `echo` :

1. Afficher un simple message :
   ```bash
   echo "Bonjour, monde !"
   ```

2. Afficher plusieurs lignes avec des séquences d'échappement :
   ```bash
   echo -e "Ligne 1\nLigne 2\nLigne 3"
   ```

3. Afficher un message sans nouvelle ligne à la fin :
   ```bash
   echo -n "Ceci est une ligne sans nouvelle ligne."
   ```

4. Afficher la valeur d'une variable :
   ```bash
   nom="Alice"
   echo "Bonjour, $nom !"
   ```

## Tips
- Utilisez l'option `-n` lorsque vous souhaitez que le texte suivant soit affiché sur la même ligne.
- Pour des sorties plus formatées, utilisez `-e` pour inclure des séquences d'échappement.
- Faites attention aux espaces autour des égalités lors de l'utilisation de variables pour éviter des erreurs.