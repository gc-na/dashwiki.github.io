# [Français] Debian Almquist Shell (dash) df : Afficher l'espace disque disponible

## Overview
La commande `df` (disk free) est utilisée pour afficher l'espace disque disponible et utilisé sur les systèmes de fichiers montés. Elle fournit des informations essentielles sur l'utilisation de l'espace disque, ce qui est utile pour la gestion des ressources système.

## Usage
La syntaxe de base de la commande `df` est la suivante :

```bash
df [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `df` :

- `-h` : Affiche les tailles dans un format lisible par l'homme (par exemple, Ko, Mo, Go).
- `-T` : Affiche le type de système de fichiers.
- `-a` : Inclut tous les systèmes de fichiers, même ceux qui ont une taille de 0.
- `-i` : Affiche l'utilisation des inodes au lieu de l'espace disque.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `df` :

1. Afficher l'espace disque disponible dans un format lisible par l'homme :

   ```bash
   df -h
   ```

2. Afficher les informations sur les systèmes de fichiers avec leur type :

   ```bash
   df -T
   ```

3. Inclure tous les systèmes de fichiers, même ceux avec une taille de 0 :

   ```bash
   df -a
   ```

4. Afficher l'utilisation des inodes :

   ```bash
   df -i
   ```

## Tips
- Utilisez l'option `-h` pour rendre les informations plus faciles à lire, surtout si vous travaillez avec de grandes quantités de données.
- Vérifiez régulièrement l'espace disque disponible pour éviter les problèmes de saturation du disque.
- Combinez `df` avec d'autres commandes comme `grep` pour filtrer les résultats selon vos besoins. Par exemple, pour afficher uniquement les systèmes de fichiers de type ext4 :

   ```bash
   df -T | grep ext4
   ```