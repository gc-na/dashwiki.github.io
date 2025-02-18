# [Français] Debian Almquist Shell (dash) cd : changer de répertoire

## Overview
La commande `cd` (change directory) est utilisée pour changer le répertoire de travail actuel dans le shell. Cela permet aux utilisateurs de naviguer dans le système de fichiers et d'accéder à différents dossiers.

## Usage
La syntaxe de base de la commande `cd` est la suivante :

```bash
cd [options] [arguments]
```

## Common Options
- `-` : Retourne au dernier répertoire visité.
- `..` : Permet de remonter d'un niveau dans l'arborescence des répertoires.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cd` :

1. Changer vers un répertoire spécifique :
   ```bash
   cd /home/utilisateur/Documents
   ```

2. Revenir au répertoire parent :
   ```bash
   cd ..
   ```

3. Retourner au dernier répertoire visité :
   ```bash
   cd -
   ```

4. Changer vers le répertoire personnel de l'utilisateur :
   ```bash
   cd ~
   ```

## Tips
- Utilisez `cd -` pour naviguer rapidement entre deux répertoires.
- Pour éviter les erreurs, vérifiez toujours le chemin du répertoire avant d'utiliser `cd`.
- Vous pouvez utiliser la touche `Tab` pour l'auto-complétion des noms de répertoires, ce qui facilite la navigation.