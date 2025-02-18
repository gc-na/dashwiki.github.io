# [Français] Debian Almquist Shell (dash) export : définir des variables d'environnement

## Overview
La commande `export` dans le shell Debian Almquist (dash) est utilisée pour définir des variables d'environnement qui peuvent être accessibles par les processus enfants. Cela permet de partager des valeurs entre différents programmes exécutés dans le shell.

## Usage
La syntaxe de base de la commande `export` est la suivante :

```sh
export [options] [arguments]
```

## Common Options
- `-n` : Supprime l'exportation d'une variable, la rendant non disponible pour les processus enfants.
- `-p` : Affiche toutes les variables d'environnement exportées.

## Common Examples

1. **Exporter une variable simple :**
   ```sh
   export MY_VAR="Hello, World!"
   ```
   Cela définit la variable `MY_VAR` avec la valeur "Hello, World!" et la rend accessible aux processus enfants.

2. **Exporter plusieurs variables :**
   ```sh
   export VAR1="Value1" VAR2="Value2"
   ```
   Ici, `VAR1` et `VAR2` sont définies et exportées en une seule commande.

3. **Vérifier les variables exportées :**
   ```sh
   export -p
   ```
   Cette commande affiche toutes les variables d'environnement actuellement exportées.

4. **Supprimer l'exportation d'une variable :**
   ```sh
   export -n MY_VAR
   ```
   Cela retire `MY_VAR` de l'environnement exporté, la rendant inaccessible aux processus enfants.

## Tips
- Utilisez `export` pour vous assurer que les variables d'environnement sont disponibles pour les scripts ou programmes que vous exécutez dans le shell.
- Pour éviter les conflits de noms, choisissez des noms de variables uniques et significatifs.
- Pensez à vérifier les variables exportées avec `export -p` avant de lancer des scripts pour vous assurer que les valeurs correctes sont disponibles.