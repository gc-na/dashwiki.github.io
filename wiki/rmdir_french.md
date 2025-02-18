# [Français] Debian Almquist Shell (dash) rmdir : Supprimer des répertoires vides

## Overview
La commande `rmdir` est utilisée pour supprimer des répertoires vides dans le système de fichiers. Si le répertoire contient des fichiers ou d'autres répertoires, la commande échouera.

## Usage
La syntaxe de base de la commande `rmdir` est la suivante :

```bash
rmdir [options] [arguments]
```

## Common Options
- `--ignore-fail-on-non-empty` : Ignore les erreurs si le répertoire n'est pas vide.
- `--verbose` : Affiche un message pour chaque répertoire supprimé.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `rmdir` :

1. Supprimer un répertoire vide nommé `mon_dossier` :

   ```bash
   rmdir mon_dossier
   ```

2. Supprimer plusieurs répertoires vides à la fois :

   ```bash
   rmdir dossier1 dossier2 dossier3
   ```

3. Utiliser l'option `--verbose` pour afficher les messages de confirmation :

   ```bash
   rmdir --verbose mon_dossier
   ```

4. Ignorer les erreurs si le répertoire n'est pas vide :

   ```bash
   rmdir --ignore-fail-on-non-empty mon_dossier
   ```

## Tips
- Assurez-vous que le répertoire est vide avant d'utiliser `rmdir`, sinon la commande échouera.
- Utilisez l'option `--verbose` pour obtenir des confirmations visuelles lors de la suppression de répertoires.
- Pour supprimer un répertoire non vide, envisagez d'utiliser la commande `rm -r` à la place, mais soyez prudent, car cela supprimera également tous les fichiers et sous-répertoires.