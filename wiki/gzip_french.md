# [Debian] Debian Almquist Shell (dash) gzip Utilisation : Compresser des fichiers

## Overview
La commande `gzip` est utilisée pour compresser des fichiers afin de réduire leur taille. Elle utilise l'algorithme de compression DEFLATE et est souvent utilisée pour économiser de l'espace disque ou pour accélérer le transfert de fichiers sur le réseau.

## Usage
La syntaxe de base de la commande `gzip` est la suivante :

```bash
gzip [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `gzip` :

- `-d`, `--decompress` : Décompresse un fichier compressé.
- `-k`, `--keep` : Garde le fichier original après compression.
- `-v`, `--verbose` : Affiche des informations détaillées sur le processus de compression.
- `-r`, `--recursive` : Compresse tous les fichiers dans les sous-répertoires.
- `-f`, `--force` : Force la compression, même si le fichier de destination existe déjà.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `gzip` :

1. **Compresser un fichier :**
   ```bash
   gzip fichier.txt
   ```

2. **Décompresser un fichier :**
   ```bash
   gzip -d fichier.txt.gz
   ```

3. **Compresser un fichier tout en gardant l'original :**
   ```bash
   gzip -k fichier.txt
   ```

4. **Compresser tous les fichiers d'un répertoire :**
   ```bash
   gzip *.txt
   ```

5. **Compresser récursivement tous les fichiers dans un répertoire :**
   ```bash
   gzip -r dossier/
   ```

## Tips
- Utilisez l'option `-v` pour voir le taux de compression et d'autres informations utiles pendant le processus.
- Pour décompresser un fichier `.gz`, vous pouvez également utiliser la commande `gunzip`, qui est un alias pour `gzip -d`.
- Pensez à vérifier l'espace disque disponible avant de compresser de gros fichiers, surtout si vous ne gardez pas les originaux.