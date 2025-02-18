# [Français] Debian Almquist Shell (dash) pkill : Terminer des processus par nom

## Overview
La commande `pkill` est utilisée pour terminer des processus en fonction de leur nom ou d'autres attributs. Cela permet aux utilisateurs de gérer facilement les processus en cours d'exécution sans avoir à rechercher leur identifiant de processus (PID).

## Usage
La syntaxe de base de la commande `pkill` est la suivante :

```bash
pkill [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `pkill` :

- `-f` : Correspond à l'ensemble de la ligne de commande du processus.
- `-n` : Tuer le dernier processus correspondant.
- `-o` : Tuer le premier processus correspondant.
- `-signal` : Spécifie le signal à envoyer au processus (par défaut, c'est SIGTERM).

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `pkill` :

1. Terminer tous les processus nommés `firefox` :

   ```bash
   pkill firefox
   ```

2. Terminer tous les processus contenant le mot `python` dans leur ligne de commande :

   ```bash
   pkill -f python
   ```

3. Envoyer un signal spécifique (comme SIGKILL) à tous les processus nommés `myapp` :

   ```bash
   pkill -9 myapp
   ```

4. Terminer uniquement le dernier processus `ssh` lancé :

   ```bash
   pkill -n ssh
   ```

## Tips
- Utilisez `pkill -l` pour lister tous les signaux disponibles avant de spécifier un signal.
- Soyez prudent lorsque vous utilisez `pkill` sans options, car cela peut terminer plusieurs processus si le nom est commun.
- Pour tester la commande sans tuer réellement les processus, vous pouvez utiliser `pgrep`, qui affiche les processus correspondants sans les terminer.