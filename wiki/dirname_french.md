# [Debian] Debian Almquist Shell (dash) dirname : [extraire le nom de répertoire]

## Overview
La commande `dirname` est utilisée pour extraire le nom du répertoire d'un chemin de fichier donné. Elle renvoie la partie du chemin qui précède le dernier séparateur de répertoire, ce qui est utile pour manipuler des chemins de fichiers dans des scripts.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero` : Traite les chemins d'entrée comme étant séparés par des caractères nuls (null).
- `--help` : Affiche l'aide et quitte.
- `--version` : Affiche la version de la commande et quitte.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `dirname` :

1. Extraire le nom de répertoire d'un chemin de fichier :

```bash
dirname /home/utilisateur/documents/fichier.txt
```
Sortie :
```
/home/utilisateur/documents
```

2. Utiliser `dirname` avec une variable :

```bash
chemin="/var/log/syslog"
dirname "$chemin"
```
Sortie :
```
/var/log
```

3. Traiter plusieurs chemins à la fois :

```bash
dirname /usr/local/bin/script.sh /etc/nginx/nginx.conf
```
Sortie :
```
/usr/local/bin
/etc/nginx
```

4. Utiliser avec un caractère nul comme séparateur :

```bash
dirname -z /home/utilisateur/documents/fichier1.txt\0/home/utilisateur/documents/fichier2.txt
```
Sortie :
```
/home/utilisateur/documents
/home/utilisateur/documents
```

## Tips
- Utilisez des guillemets autour des variables pour éviter des erreurs dues aux espaces dans les chemins.
- Combinez `dirname` avec d'autres commandes comme `basename` pour des manipulations de chemin plus complexes.
- Pensez à utiliser `dirname` dans des scripts pour automatiser la gestion des fichiers et des répertoires.