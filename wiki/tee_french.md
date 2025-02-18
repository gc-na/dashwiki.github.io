# [Français] Debian Almquist Shell (dash) tee : [rediriger la sortie vers un fichier]

## Overview
La commande `tee` permet de lire l'entrée standard et de la rediriger à la fois vers la sortie standard et vers un ou plusieurs fichiers. Cela est particulièrement utile pour enregistrer des données tout en continuant à les afficher à l'écran.

## Usage
La syntaxe de base de la commande `tee` est la suivante :

```bash
tee [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `tee` :

- `-a` : Ajoute la sortie à la fin du fichier au lieu de l'écraser.
- `-i` : Ignore les signaux d'interruption.
- `-p` : Affiche les erreurs de fichier.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `tee` :

1. **Rediriger la sortie d'une commande vers un fichier :**
   ```bash
   echo "Bonjour, monde!" | tee fichier.txt
   ```

2. **Ajouter à un fichier existant :**
   ```bash
   echo "Nouvelle ligne" | tee -a fichier.txt
   ```

3. **Utiliser tee avec plusieurs fichiers :**
   ```bash
   echo "Données importantes" | tee fichier1.txt fichier2.txt
   ```

4. **Combiner tee avec d'autres commandes :**
   ```bash
   ls -l | tee liste_fichiers.txt | grep ".txt"
   ```

## Tips
- Utilisez l'option `-a` si vous souhaitez ajouter des données à un fichier sans écraser son contenu.
- Combinez `tee` avec d'autres commandes pour filtrer ou manipuler les données tout en les enregistrant.
- Vérifiez toujours les permissions des fichiers pour éviter les erreurs lors de l'écriture.