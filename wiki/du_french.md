# [Debian] Debian Almquist Shell (dash) du : afficher l'utilisation de l'espace disque

## Overview
La commande `du` (disk usage) est utilisée pour estimer et afficher l'utilisation de l'espace disque des fichiers et des répertoires. Elle permet aux utilisateurs de comprendre combien d'espace est occupé par leurs fichiers et dossiers, ce qui est essentiel pour la gestion de l'espace disque.

## Usage
La syntaxe de base de la commande `du` est la suivante :

```bash
du [options] [arguments]
```

## Common Options
Voici quelques options courantes de la commande `du` :

- `-h` : Affiche les tailles dans un format lisible par l'homme (ex. : Ko, Mo, Go).
- `-s` : Affiche uniquement le total pour chaque argument, sans détailler les sous-répertoires.
- `-a` : Affiche l'utilisation de l'espace pour tous les fichiers, pas seulement les répertoires.
- `-c` : Affiche un total cumulatif à la fin de la sortie.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `du` :

1. Afficher l'utilisation de l'espace disque d'un répertoire :

   ```bash
   du /chemin/vers/repertoire
   ```

2. Afficher l'utilisation de l'espace dans un format lisible par l'homme :

   ```bash
   du -h /chemin/vers/repertoire
   ```

3. Afficher uniquement le total pour un répertoire :

   ```bash
   du -sh /chemin/vers/repertoire
   ```

4. Afficher l'utilisation de l'espace pour tous les fichiers et répertoires dans le répertoire courant :

   ```bash
   du -ah
   ```

5. Afficher un total cumulatif de l'utilisation de l'espace pour plusieurs répertoires :

   ```bash
   du -ch /chemin/vers/repertoire1 /chemin/vers/repertoire2
   ```

## Tips
- Utilisez l'option `-h` pour rendre les résultats plus faciles à lire, surtout lorsque vous travaillez avec de grandes quantités de données.
- Combinez `du` avec d'autres commandes comme `sort` pour trier les résultats par taille, par exemple :

  ```bash
  du -h /chemin/vers/repertoire | sort -h
  ```

- Pour une analyse plus approfondie, envisagez d'utiliser `ncdu`, un outil interactif basé sur `du` qui offre une interface utilisateur plus conviviale.