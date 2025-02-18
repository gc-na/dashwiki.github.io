# [Debian] Debian Almquist Shell (dash) sed Utilisation : Modifier et transformer du texte

## Overview
La commande `sed` (stream editor) est un éditeur de texte non interactif qui permet de manipuler et de transformer des flux de texte. Elle est souvent utilisée pour effectuer des substitutions, des suppressions ou des insertions de lignes dans des fichiers ou des entrées standard.

## Usage
La syntaxe de base de la commande `sed` est la suivante :

```bash
sed [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `sed` :

- `-e` : Permet d'ajouter une commande à exécuter.
- `-f` : Spécifie un fichier contenant des commandes `sed`.
- `-i` : Modifie les fichiers en place (sans créer de copie).
- `-n` : Supprime la sortie automatique, utile avec la commande `p` pour afficher uniquement les lignes spécifiées.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `sed` :

1. **Substituer une chaîne de caractères :**
   Remplacer "chat" par "chien" dans un fichier `animaux.txt`.

   ```bash
   sed 's/chat/chien/g' animaux.txt
   ```

2. **Supprimer une ligne contenant un mot spécifique :**
   Supprimer toutes les lignes contenant "erreur" dans un fichier `journal.txt`.

   ```bash
   sed '/erreur/d' journal.txt
   ```

3. **Modifier un fichier en place :**
   Remplacer "ancien" par "nouveau" directement dans le fichier `config.txt`.

   ```bash
   sed -i 's/ancien/nouveau/g' config.txt
   ```

4. **Afficher uniquement les lignes qui contiennent un mot :**
   Afficher toutes les lignes contenant "important" dans un fichier `notes.txt`.

   ```bash
   sed -n '/important/p' notes.txt
   ```

## Tips
- Utilisez l'option `-i` avec précaution, car elle modifie les fichiers originaux. Pensez à faire une sauvegarde si nécessaire.
- Testez vos commandes `sed` sans l'option `-i` d'abord pour vous assurer qu'elles fonctionnent comme prévu.
- Les expressions régulières peuvent être utilisées avec `sed` pour des substitutions plus complexes. Familiarisez-vous avec les bases des expressions régulières pour tirer le meilleur parti de `sed`.