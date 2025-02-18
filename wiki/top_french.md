# [Debian] Debian Almquist Shell (dash) top : Afficher les processus en cours

## Overview
La commande `top` est un outil puissant qui permet de surveiller en temps réel les processus en cours d'exécution sur un système. Elle affiche des informations sur l'utilisation du CPU, de la mémoire et d'autres ressources, ce qui aide les utilisateurs à identifier les processus gourmands en ressources.

## Usage
La syntaxe de base de la commande `top` est la suivante :

```bash
top [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `top` :

- `-d <seconds>` : Définit l'intervalle de mise à jour en secondes.
- `-p <pid>` : Affiche uniquement le processus avec l'identifiant spécifié.
- `-u <user>` : Affiche uniquement les processus appartenant à l'utilisateur spécifié.
- `-n <number>` : Définit le nombre de mises à jour avant de quitter.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `top` :

1. Lancer `top` avec les mises à jour par défaut :
   ```bash
   top
   ```

2. Lancer `top` avec un intervalle de mise à jour de 2 secondes :
   ```bash
   top -d 2
   ```

3. Afficher uniquement les processus d'un utilisateur spécifique :
   ```bash
   top -u nom_utilisateur
   ```

4. Afficher un processus spécifique par son identifiant :
   ```bash
   top -p 1234
   ```

5. Exécuter `top` pour un nombre limité de mises à jour (par exemple, 5) :
   ```bash
   top -n 5
   ```

## Tips
- Pour quitter l'interface `top`, appuyez sur `q`.
- Vous pouvez trier les processus en appuyant sur les touches correspondantes, comme `M` pour trier par utilisation de la mémoire.
- Utilisez `h` dans l'interface `top` pour afficher l'aide et découvrir d'autres fonctionnalités.