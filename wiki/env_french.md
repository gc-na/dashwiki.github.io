# [Debian] Debian Almquist Shell (dash) env : [exécuter des commandes avec des variables d'environnement]

## Overview
La commande `env` est utilisée pour exécuter des commandes dans un environnement modifié. Elle permet de définir ou de modifier des variables d'environnement avant d'exécuter une commande spécifique.

## Usage
La syntaxe de base de la commande `env` est la suivante :

```bash
env [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande env :

- `-i` : Exécute la commande dans un environnement vide, sans variables d'environnement héritées.
- `-u` : Supprime une variable d'environnement spécifique avant d'exécuter la commande.
- `VAR=valeur` : Définit une variable d'environnement pour la commande qui suit.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `env` :

1. **Afficher toutes les variables d'environnement :**
   ```bash
   env
   ```

2. **Exécuter une commande avec une variable d'environnement définie :**
   ```bash
   env MY_VAR=Hello world
   ```

3. **Supprimer une variable d'environnement avant d'exécuter une commande :**
   ```bash
   env -u MY_VAR command
   ```

4. **Exécuter une commande dans un environnement vide :**
   ```bash
   env -i bash
   ```

## Tips
- Utilisez `env` pour tester des scripts dans un environnement contrôlé en définissant ou en supprimant des variables d'environnement.
- Vérifiez toujours les variables d'environnement avant d'exécuter des commandes critiques pour éviter des comportements inattendus.
- Combinez `env` avec d'autres commandes pour créer des scripts flexibles et portables.