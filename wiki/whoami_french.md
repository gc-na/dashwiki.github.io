# [Français] Debian Almquist Shell (dash) whoami : identifier l'utilisateur courant

## Overview
La commande `whoami` permet d'afficher le nom de l'utilisateur actuellement connecté au système. C'est un outil simple mais utile pour vérifier l'identité de l'utilisateur en cours d'exécution d'un shell.

## Usage
La syntaxe de base de la commande `whoami` est la suivante :

```bash
whoami [options] [arguments]
```

## Common Options
La commande `whoami` ne possède pas de nombreuses options, mais voici celles qui sont couramment utilisées :

- `--help` : Affiche l'aide et les options disponibles pour la commande.
- `--version` : Affiche la version de la commande `whoami`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `whoami` :

1. **Afficher le nom de l'utilisateur courant** :
   ```bash
   whoami
   ```

2. **Afficher l'aide de la commande** :
   ```bash
   whoami --help
   ```

3. **Afficher la version de la commande** :
   ```bash
   whoami --version
   ```

## Tips
- Utilisez `whoami` dans des scripts pour vérifier l'utilisateur qui exécute le script, afin de s'assurer qu'il a les permissions nécessaires.
- Combinez `whoami` avec d'autres commandes pour des vérifications de sécurité, par exemple, en vérifiant si l'utilisateur courant est un administrateur avant d'exécuter des commandes sensibles.