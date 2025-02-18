# [Debian] Debian Almquist Shell (dash) jobs : Gérer les tâches en arrière-plan

## Overview
La commande `jobs` dans le shell Almquist de Debian (dash) permet d'afficher la liste des tâches en arrière-plan et des tâches suspendues dans la session actuelle du terminal. Cela est particulièrement utile pour gérer plusieurs processus sans avoir à les fermer.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
jobs [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `jobs` :

- `-l` : Affiche les identifiants de processus (PID) des tâches.
- `-n` : Affiche uniquement les tâches qui ont changé d'état depuis la dernière exécution de la commande.
- `-p` : Affiche uniquement les identifiants de processus des tâches.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `jobs` :

1. **Afficher toutes les tâches en arrière-plan :**

   ```bash
   jobs
   ```

2. **Afficher les tâches avec leurs identifiants de processus :**

   ```bash
   jobs -l
   ```

3. **Afficher uniquement les tâches qui ont changé d'état :**

   ```bash
   jobs -n
   ```

4. **Afficher uniquement les identifiants de processus des tâches :**

   ```bash
   jobs -p
   ```

## Tips
- Utilisez `bg` pour reprendre une tâche suspendue en arrière-plan après avoir utilisé `Ctrl+Z`.
- Utilisez `fg` pour ramener une tâche en avant-plan.
- Vérifiez régulièrement l'état de vos tâches avec `jobs` pour éviter d'avoir trop de processus en cours d'exécution.