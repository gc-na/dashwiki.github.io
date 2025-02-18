# [Debian] Debian Almquist Shell (dash) zip utilisation : compresser des fichiers

## Overview
La commande `zip` est utilisée pour compresser des fichiers et des répertoires en un seul fichier archive. Cela permet de réduire l'espace de stockage et de faciliter le partage de plusieurs fichiers.

## Usage
La syntaxe de base de la commande `zip` est la suivante :

```bash
zip [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `zip` :

- `-r` : Compresse récursivement les répertoires.
- `-e` : Chiffre le fichier zip.
- `-9` : Utilise le niveau de compression maximal.
- `-d` : Supprime des fichiers d'une archive zip existante.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `zip` :

1. **Compresser un fichier :**
   ```bash
   zip archive.zip fichier.txt
   ```

2. **Compresser plusieurs fichiers :**
   ```bash
   zip archive.zip fichier1.txt fichier2.txt fichier3.txt
   ```

3. **Compresser un répertoire de manière récursive :**
   ```bash
   zip -r archive.zip mon_repertoire/
   ```

4. **Compresser avec chiffrement :**
   ```bash
   zip -e archive.zip fichier.txt
   ```

5. **Supprimer un fichier d'une archive zip :**
   ```bash
   zip -d archive.zip fichier.txt
   ```

## Tips
- Utilisez l'option `-9` pour une compression maximale, mais sachez que cela peut prendre plus de temps.
- Pensez à chiffrer vos fichiers sensibles avec l'option `-e` pour plus de sécurité.
- Pour vérifier le contenu d'une archive zip sans l'extraire, utilisez la commande `unzip -l archive.zip`.