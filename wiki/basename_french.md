# [Français] Debian Almquist Shell (dash) basename utilisation : extraire le nom de fichier

## Overview
La commande `basename` est utilisée pour extraire le nom de fichier d'un chemin donné, en supprimant le répertoire et éventuellement une extension de fichier. Cela permet de travailler plus facilement avec les noms de fichiers dans des scripts ou des commandes.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
basename [options] [arguments]
```

## Common Options
- `-a` : Traite tous les arguments fournis et renvoie chacun d'eux.
- `-s` : Supprime une extension spécifique du nom de fichier.
- `--help` : Affiche l'aide et les options disponibles.
- `--version` : Affiche la version de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `basename` :

1. Extraire le nom de fichier d'un chemin complet :

   ```bash
   basename /chemin/vers/fichier.txt
   ```

   **Sortie :** `fichier.txt`

2. Extraire le nom de fichier sans l'extension :

   ```bash
   basename /chemin/vers/fichier.txt .txt
   ```

   **Sortie :** `fichier`

3. Traiter plusieurs fichiers à la fois :

   ```bash
   basename -a /chemin/vers/fichier1.txt /chemin/vers/fichier2.txt
   ```

   **Sortie :**
   ```
   fichier1.txt
   fichier2.txt
   ```

4. Supprimer une extension différente :

   ```bash
   basename /chemin/vers/fichier.tar.gz .tar.gz
   ```

   **Sortie :** `fichier`

## Tips
- Utilisez l'option `-a` pour traiter plusieurs fichiers en une seule commande, ce qui peut rendre votre script plus efficace.
- Lorsque vous utilisez l'option `-s`, assurez-vous que l'extension que vous souhaitez supprimer est correcte pour éviter des résultats inattendus.
- `basename` est particulièrement utile dans les scripts shell pour manipuler des noms de fichiers sans avoir à gérer les chemins complets.