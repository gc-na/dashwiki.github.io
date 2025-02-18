# [Français] Debian Almquist Shell (dash) uname Utilisation : Afficher les informations système

## Overview
La commande `uname` est utilisée pour afficher des informations sur le système d'exploitation et le matériel sur lequel le shell est exécuté. Elle fournit des détails tels que le nom du noyau, la version et d'autres informations pertinentes.

## Usage
La syntaxe de base de la commande `uname` est la suivante :

```bash
uname [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `uname` :

- `-a` : Affiche toutes les informations disponibles sur le système.
- `-s` : Affiche le nom du noyau.
- `-n` : Affiche le nom de l'hôte du système.
- `-r` : Affiche la version du noyau.
- `-v` : Affiche des informations supplémentaires sur la version du noyau.
- `-m` : Affiche l'architecture matérielle du système.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `uname` :

1. Afficher toutes les informations sur le système :

   ```bash
   uname -a
   ```

2. Afficher uniquement le nom du noyau :

   ```bash
   uname -s
   ```

3. Afficher la version du noyau :

   ```bash
   uname -r
   ```

4. Afficher l'architecture matérielle :

   ```bash
   uname -m
   ```

5. Afficher le nom de l'hôte :

   ```bash
   uname -n
   ```

## Tips
- Utilisez l'option `-a` pour obtenir un aperçu complet de votre système en une seule commande.
- Combinez `uname` avec d'autres commandes pour des scripts plus avancés, par exemple, pour vérifier la compatibilité des logiciels avec votre architecture.
- Pensez à exécuter `uname` avec des privilèges d'administrateur si vous avez besoin d'informations spécifiques sur le système qui peuvent être restreintes.