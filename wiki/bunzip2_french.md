# [Français] Debian Almquist Shell (dash) bunzip2 utilisation : Décompresser des fichiers Bzip2

## Overview
La commande `bunzip2` est utilisée pour décompresser des fichiers qui ont été compressés au format Bzip2. Elle est souvent utilisée pour réduire la taille des fichiers, facilitant ainsi leur stockage et leur transfert.

## Usage
La syntaxe de base de la commande `bunzip2` est la suivante :

```bash
bunzip2 [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `bunzip2` :

- `-k` : Garde le fichier d'origine après la décompression.
- `-f` : Force la décompression, même si le fichier de destination existe déjà.
- `-v` : Affiche des informations détaillées sur le processus de décompression.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `bunzip2` :

1. Décompresser un fichier Bzip2 :
   ```bash
   bunzip2 fichier.bz2
   ```

2. Décompresser un fichier tout en conservant le fichier d'origine :
   ```bash
   bunzip2 -k fichier.bz2
   ```

3. Forcer la décompression d'un fichier existant :
   ```bash
   bunzip2 -f fichier.bz2
   ```

4. Afficher des informations détaillées lors de la décompression :
   ```bash
   bunzip2 -v fichier.bz2
   ```

## Tips
- Assurez-vous d'avoir suffisamment d'espace disque avant de décompresser un fichier, surtout si vous ne conservez pas le fichier d'origine.
- Utilisez l'option `-k` si vous souhaitez garder le fichier compressé pour une utilisation future.
- Vérifiez toujours le format du fichier avant d'utiliser `bunzip2`, car cette commande ne fonctionne qu'avec des fichiers au format Bzip2.