# [Français] Debian Almquist Shell (dash) mkdir Utilisation : Créer des répertoires

## Overview
La commande `mkdir` est utilisée pour créer de nouveaux répertoires dans le système de fichiers. C'est un outil essentiel pour organiser vos fichiers et dossiers.

## Usage
La syntaxe de base de la commande `mkdir` est la suivante :

```bash
mkdir [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mkdir` :

- `-p` : Crée des répertoires parents si nécessaire. Par exemple, si vous essayez de créer un répertoire dans un chemin qui n'existe pas encore, cette option créera tous les répertoires parents requis.
- `-v` : Affiche un message pour chaque répertoire créé. Cela peut être utile pour vérifier que la commande a fonctionné comme prévu.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mkdir` :

1. Créer un répertoire simple :
   ```bash
   mkdir mon_dossier
   ```

2. Créer plusieurs répertoires à la fois :
   ```bash
   mkdir dossier1 dossier2 dossier3
   ```

3. Créer un répertoire avec des répertoires parents :
   ```bash
   mkdir -p /chemin/vers/mon_dossier
   ```

4. Créer un répertoire et afficher un message :
   ```bash
   mkdir -v mon_dossier
   ```

## Tips
- Utilisez l'option `-p` lorsque vous n'êtes pas sûr que le chemin complet existe déjà, cela évite les erreurs.
- N'oubliez pas de vérifier les permissions du répertoire parent pour vous assurer que vous avez le droit de créer des sous-répertoires.
- Pour éviter les erreurs, utilisez des noms de répertoire clairs et descriptifs.