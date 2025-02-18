# [Français] Debian Almquist Shell (dash) uniq : Supprimer les lignes en double

## Overview
La commande `uniq` est utilisée pour filtrer les lignes répétées dans un fichier ou une entrée standard. Elle ne supprime que les lignes consécutives identiques, ce qui signifie que pour qu'une ligne soit considérée comme un doublon, elle doit apparaître plusieurs fois de suite.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
uniq [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `uniq` :

- `-c` : Compte le nombre d'occurrences de chaque ligne.
- `-d` : Affiche uniquement les lignes qui apparaissent plus d'une fois.
- `-u` : Affiche uniquement les lignes qui apparaissent une seule fois.
- `-i` : Ignore la casse lors de la comparaison des lignes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `uniq` :

1. **Supprimer les doublons d'un fichier :**
   ```bash
   uniq fichier.txt
   ```

2. **Compter les occurrences de chaque ligne :**
   ```bash
   uniq -c fichier.txt
   ```

3. **Afficher uniquement les lignes répétées :**
   ```bash
   uniq -d fichier.txt
   ```

4. **Ignorer la casse lors de la suppression des doublons :**
   ```bash
   uniq -i fichier.txt
   ```

## Tips
- Assurez-vous que votre fichier est trié avant d'utiliser `uniq`, car il ne supprime que les doublons consécutifs. Vous pouvez utiliser la commande `sort` pour trier le fichier.
- Combinez `uniq` avec d'autres commandes comme `sort` pour obtenir des résultats plus précis. Par exemple :
  ```bash
  sort fichier.txt | uniq
  ```
- Pour traiter des entrées standard, vous pouvez utiliser `uniq` directement avec un pipe :
  ```bash
  cat fichier.txt | uniq
  ```