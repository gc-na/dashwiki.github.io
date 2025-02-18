# [Debian] Debian Almquist Shell (dash) w : afficher les utilisateurs connectés

## Overview
La commande `w` permet d'afficher des informations sur les utilisateurs actuellement connectés au système ainsi que sur les processus qu'ils exécutent. Elle fournit un aperçu utile de l'activité des utilisateurs en temps réel.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
w [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `w` :

- `-h` : Ne pas afficher l'en-tête.
- `-s` : Afficher les informations dans un format plus compact.
- `-u` : Afficher l'heure de connexion des utilisateurs.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `w` :

1. Afficher tous les utilisateurs connectés :
   ```bash
   w
   ```

2. Afficher les utilisateurs sans l'en-tête :
   ```bash
   w -h
   ```

3. Afficher les informations dans un format compact :
   ```bash
   w -s
   ```

4. Afficher les utilisateurs avec l'heure de connexion :
   ```bash
   w -u
   ```

## Tips
- Utilisez `w` régulièrement pour surveiller l'activité des utilisateurs sur votre système.
- Combinez `w` avec d'autres commandes comme `grep` pour filtrer les résultats. Par exemple, pour trouver un utilisateur spécifique :
  ```bash
  w | grep nom_utilisateur
  ```
- Familiarisez-vous avec les options pour personnaliser la sortie selon vos besoins.