# [Français] Debian Almquist Shell (dash) gunzip : Décompresser des fichiers gzip

## Overview
La commande `gunzip` est utilisée pour décompresser des fichiers compressés au format gzip. Elle restaure le fichier original à partir de son format compressé, ce qui permet d'économiser de l'espace de stockage et de faciliter le transfert de données.

## Usage
La syntaxe de base de la commande `gunzip` est la suivante :

```bash
gunzip [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `gunzip` :

- `-c` : Affiche le contenu décompressé sur la sortie standard sans supprimer le fichier compressé.
- `-f` : Force la décompression, même si le fichier de destination existe déjà.
- `-k` : Garde le fichier compressé après la décompression.
- `-r` : Décompresse les fichiers dans les sous-répertoires de manière récursive.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `gunzip` :

1. Décompresser un fichier simple :
   ```bash
   gunzip fichier.txt.gz
   ```

2. Afficher le contenu décompressé sans supprimer le fichier compressé :
   ```bash
   gunzip -c fichier.txt.gz
   ```

3. Décompresser un fichier tout en conservant le fichier compressé :
   ```bash
   gunzip -k fichier.txt.gz
   ```

4. Décompresser tous les fichiers `.gz` dans un répertoire :
   ```bash
   gunzip *.gz
   ```

5. Décompression récursive dans un répertoire :
   ```bash
   gunzip -r dossier/
   ```

## Tips
- Vérifiez toujours l'espace disque disponible avant de décompresser de gros fichiers pour éviter les erreurs de stockage.
- Utilisez l'option `-c` pour visualiser le contenu des fichiers compressés sans les décompresser si vous avez besoin d'un aperçu rapide.
- Si vous travaillez avec plusieurs fichiers, envisagez d'utiliser des jokers (`*`) pour décompresser plusieurs fichiers à la fois, ce qui peut vous faire gagner du temps.