# [Français] Debian Almquist Shell (dash) umask : Gérer les permissions par défaut des fichiers

## Overview
La commande `umask` permet de définir les permissions par défaut pour les nouveaux fichiers et répertoires créés dans le système. Elle spécifie les bits de permission qui doivent être masqués lors de la création de nouveaux fichiers.

## Usage
La syntaxe de base de la commande `umask` est la suivante :

```bash
umask [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `umask` :

- `-S` : Affiche les permissions sous forme symbolique.
- `-p` : Affiche la valeur actuelle de umask pour le shell en cours.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `umask` :

1. **Afficher la valeur actuelle de umask :**
   ```bash
   umask
   ```

2. **Définir umask à 022 (permissions 755 pour les répertoires et 644 pour les fichiers) :**
   ```bash
   umask 022
   ```

3. **Afficher umask en format symbolique :**
   ```bash
   umask -S
   ```

4. **Définir umask à 077 (permissions 700 pour les répertoires et 600 pour les fichiers) :**
   ```bash
   umask 077
   ```

## Tips
- Il est conseillé de vérifier la valeur de `umask` avant de créer des fichiers sensibles pour s'assurer que les permissions sont appropriées.
- Utilisez `umask -S` pour avoir une vue claire des permissions sous forme symbolique, ce qui peut être plus facile à comprendre.
- Pensez à définir `umask` dans vos fichiers de configuration de shell (comme `.bashrc` ou `.profile`) pour appliquer vos préférences à chaque session.