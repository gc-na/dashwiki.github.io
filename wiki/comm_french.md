# [Français] Debian Almquist Shell (dash) comm : comparer des fichiers ligne par ligne

## Overview
La commande `comm` est utilisée pour comparer deux fichiers triés ligne par ligne. Elle affiche les lignes qui sont uniques à chaque fichier ainsi que les lignes communes.

## Usage
La syntaxe de base de la commande est la suivante :

```
comm [options] [fichier1] [fichier2]
```

## Common Options
- `-1` : Supprime les lignes uniques au premier fichier de la sortie.
- `-2` : Supprime les lignes uniques au deuxième fichier de la sortie.
- `-3` : Supprime les lignes communes de la sortie.
- `--nocheck-order` : Ne vérifie pas si les fichiers sont triés.

## Common Examples

### Exemple 1 : Comparer deux fichiers
Pour comparer deux fichiers `file1.txt` et `file2.txt`, utilisez la commande suivante :

```bash
comm file1.txt file2.txt
```

### Exemple 2 : Afficher uniquement les lignes communes
Pour afficher uniquement les lignes qui apparaissent dans les deux fichiers, utilisez l'option `-1` et `-2` :

```bash
comm -12 file1.txt file2.txt
```

### Exemple 3 : Afficher les lignes uniques au premier fichier
Pour afficher uniquement les lignes qui sont présentes dans `file1.txt` mais pas dans `file2.txt`, utilisez l'option `-2` :

```bash
comm -23 file1.txt file2.txt
```

### Exemple 4 : Afficher les lignes uniques au deuxième fichier
Pour afficher uniquement les lignes qui sont présentes dans `file2.txt` mais pas dans `file1.txt`, utilisez l'option `-1` :

```bash
comm -13 file1.txt file2.txt
```

## Tips
- Assurez-vous que les fichiers sont triés avant d'utiliser `comm`, sinon les résultats peuvent ne pas être fiables.
- Vous pouvez rediriger la sortie de `comm` vers un fichier en utilisant `>` pour enregistrer les résultats.
- Utilisez `sort` en combinaison avec `comm` si vous n'êtes pas sûr que vos fichiers soient triés :

```bash
comm <(sort file1.txt) <(sort file2.txt)
```