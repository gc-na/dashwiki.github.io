# [Français] Utilisateurs de Debian Almquist Shell (dash) : afficher les utilisateurs connectés

## Overview
La commande `users` permet d'afficher les noms des utilisateurs actuellement connectés au système. C'est un outil simple et efficace pour obtenir rapidement des informations sur les sessions actives.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
users [options] [arguments]
```

## Common Options
La commande `users` a peu d'options, mais voici celles qui sont couramment utilisées :

- `-H`, `--help` : Affiche l'aide et les options disponibles pour la commande.
- `-V`, `--version` : Affiche la version de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `users` :

1. **Afficher les utilisateurs connectés :**
   ```bash
   users
   ```

2. **Afficher l'aide de la commande :**
   ```bash
   users --help
   ```

3. **Afficher la version de la commande :**
   ```bash
   users --version
   ```

## Tips
- Utilisez `users` en combinaison avec d'autres commandes comme `who` ou `w` pour obtenir des informations plus détaillées sur les utilisateurs connectés.
- Pensez à exécuter la commande dans un terminal pour voir les résultats en temps réel, surtout sur un système multi-utilisateur.