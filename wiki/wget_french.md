# [Français] Debian Almquist Shell (dash) wget utilisation : Téléchargement de fichiers à partir du web

## Overview
La commande `wget` est un outil en ligne de commande utilisé pour télécharger des fichiers à partir du web. Elle prend en charge divers protocoles tels que HTTP, HTTPS et FTP, ce qui en fait un choix polyvalent pour récupérer des ressources sur Internet.

## Usage
La syntaxe de base de la commande `wget` est la suivante :

```bash
wget [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `wget` :

- `-O [fichier]` : Spécifie le nom du fichier de sortie.
- `-c` : Reprend un téléchargement interrompu.
- `-q` : Exécute wget en mode silencieux, sans afficher de messages.
- `--limit-rate=[vitesse]` : Limite la vitesse de téléchargement.
- `-r` : Télécharge récursivement les fichiers d'un site web.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `wget` :

1. Télécharger un fichier à partir d'une URL :

   ```bash
   wget https://example.com/fichier.zip
   ```

2. Télécharger un fichier et le renommer :

   ```bash
   wget -O nouveau_nom.zip https://example.com/fichier.zip
   ```

3. Reprendre un téléchargement interrompu :

   ```bash
   wget -c https://example.com/fichier.zip
   ```

4. Télécharger un site web de manière récursive :

   ```bash
   wget -r https://example.com
   ```

5. Limiter la vitesse de téléchargement à 200 Ko/s :

   ```bash
   wget --limit-rate=200k https://example.com/fichier.zip
   ```

## Tips
- Utilisez l'option `-q` pour éviter l'encombrement de la sortie si vous téléchargez plusieurs fichiers.
- Pensez à vérifier les droits d'accès lorsque vous téléchargez des fichiers à partir de sites protégés par un mot de passe.
- Pour des téléchargements massifs, utilisez l'option `-i [fichier]` pour télécharger tous les fichiers listés dans un fichier texte.