# [Français] Debian Almquist Shell (dash) mv Utilisation : Déplacer ou renommer des fichiers

## Overview
La commande `mv` est utilisée pour déplacer ou renommer des fichiers et des répertoires dans le système de fichiers. Elle permet de changer l'emplacement d'un fichier ou de modifier son nom sans créer de copie.

## Usage
La syntaxe de base de la commande `mv` est la suivante :

```bash
mv [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mv` :

- `-i` : Demande confirmation avant d'écraser un fichier existant.
- `-u` : Déplace uniquement si le fichier source est plus récent que le fichier de destination ou si le fichier de destination n'existe pas.
- `-v` : Affiche les détails des opérations effectuées.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mv` :

1. **Déplacer un fichier vers un autre répertoire :**
   ```bash
   mv fichier.txt /chemin/vers/nouveau/repertoire/
   ```

2. **Renommer un fichier :**
   ```bash
   mv ancien_nom.txt nouveau_nom.txt
   ```

3. **Déplacer plusieurs fichiers vers un répertoire :**
   ```bash
   mv fichier1.txt fichier2.txt /chemin/vers/repertoire/
   ```

4. **Déplacer un fichier avec confirmation :**
   ```bash
   mv -i fichier.txt /chemin/vers/nouveau/repertoire/
   ```

5. **Déplacer un fichier uniquement s'il est plus récent :**
   ```bash
   mv -u fichier.txt /chemin/vers/nouveau/repertoire/
   ```

## Tips
- Utilisez l'option `-i` pour éviter d'écraser accidentellement des fichiers importants.
- Vérifiez toujours le chemin de destination avant de déplacer des fichiers pour éviter de les perdre.
- Pour des opérations complexes, envisagez d'utiliser des scripts shell pour automatiser le processus.