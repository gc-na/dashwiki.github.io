# [Français] Debian Almquist Shell (dash) rsync : Synchroniser des fichiers et des répertoires

## Overview
La commande `rsync` est un outil puissant utilisé pour synchroniser des fichiers et des répertoires entre différentes emplacements, que ce soit sur le même système ou à travers un réseau. Elle est particulièrement appréciée pour sa capacité à transférer uniquement les fichiers qui ont changé, ce qui la rend efficace en termes de bande passante et de temps.

## Usage
La syntaxe de base de la commande `rsync` est la suivante :

```bash
rsync [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `rsync` :

- `-a` : Archive mode, qui préserve les permissions, les timestamps, et les liens symboliques.
- `-v` : Mode verbeux, pour afficher les fichiers en cours de transfert.
- `-z` : Compression des données lors du transfert, utile pour réduire la taille des fichiers envoyés.
- `-r` : Récursif, pour copier des répertoires et leur contenu.
- `--delete` : Supprime les fichiers dans la destination qui ne sont pas présents dans la source.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `rsync` :

1. **Synchroniser un répertoire local :**

```bash
rsync -av /chemin/vers/source/ /chemin/vers/destination/
```

2. **Synchroniser un répertoire vers un serveur distant :**

```bash
rsync -avz /chemin/vers/source/ utilisateur@serveur:/chemin/vers/destination/
```

3. **Synchroniser tout en supprimant les fichiers obsolètes :**

```bash
rsync -av --delete /chemin/vers/source/ /chemin/vers/destination/
```

4. **Synchroniser un répertoire tout en affichant les détails :**

```bash
rsync -av --progress /chemin/vers/source/ /chemin/vers/destination/
```

## Tips
- Toujours utiliser un chemin avec un `/` à la fin pour indiquer que vous souhaitez synchroniser le contenu du répertoire plutôt que le répertoire lui-même.
- Effectuez d'abord un test avec l'option `--dry-run` pour voir ce qui sera transféré sans effectuer de modifications.
- Utilisez des connexions SSH pour des transferts sécurisés lorsque vous travaillez avec des serveurs distants.