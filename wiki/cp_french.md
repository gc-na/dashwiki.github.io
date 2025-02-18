# [Debian] Debian Almquist Shell (dash) cp : Copier des fichiers et des répertoires

## Overview
La commande `cp` est utilisée pour copier des fichiers et des répertoires dans le système de fichiers. Elle permet de dupliquer des fichiers d'un emplacement à un autre, facilitant ainsi la gestion des données.

## Usage
La syntaxe de base de la commande `cp` est la suivante :

```bash
cp [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `cp` :

- `-r` : Copie récursivement les répertoires et leur contenu.
- `-i` : Demande confirmation avant d'écraser un fichier existant.
- `-u` : Copie uniquement les fichiers qui sont plus récents que ceux de la destination ou qui n'existent pas.
- `-v` : Affiche les fichiers au fur et à mesure qu'ils sont copiés (mode verbeux).

## Common Examples
Voici quelques exemples pratiques de la commande `cp` :

1. Copier un fichier dans un autre emplacement :
   ```bash
   cp fichier.txt /chemin/vers/destination/
   ```

2. Copier un répertoire et son contenu :
   ```bash
   cp -r mon_repertoire /chemin/vers/destination/
   ```

3. Copier un fichier tout en demandant confirmation avant d'écraser :
   ```bash
   cp -i fichier.txt /chemin/vers/destination/
   ```

4. Copier un fichier uniquement s'il est plus récent :
   ```bash
   cp -u fichier.txt /chemin/vers/destination/
   ```

5. Copier un fichier avec affichage des détails :
   ```bash
   cp -v fichier.txt /chemin/vers/destination/
   ```

## Tips
- Utilisez l'option `-i` pour éviter d'écraser accidentellement des fichiers importants.
- Pour copier plusieurs fichiers à la fois, listez-les avant le répertoire de destination :
  ```bash
  cp fichier1.txt fichier2.txt /chemin/vers/destination/
  ```
- Pensez à utiliser l'option `-r` lorsque vous copiez des répertoires pour vous assurer que tout le contenu est inclus.