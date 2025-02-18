# [Français] Debian Almquist Shell (dash) crontab : Planifier des tâches

## Overview
La commande `crontab` permet de planifier l'exécution de tâches à des intervalles réguliers sur un système Unix/Linux. Elle utilise un fichier de configuration, souvent appelé "crontab", pour spécifier les commandes à exécuter et leur fréquence.

## Usage
La syntaxe de base de la commande `crontab` est la suivante :

```bash
crontab [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `crontab` :

- `-e` : Édite le fichier crontab de l'utilisateur courant.
- `-l` : Affiche le contenu du fichier crontab de l'utilisateur courant.
- `-r` : Supprime le fichier crontab de l'utilisateur courant.
- `-i` : Demande une confirmation avant de supprimer le crontab.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `crontab` :

1. **Éditer le crontab** :
   Pour ouvrir le fichier crontab dans un éditeur de texte :
   ```bash
   crontab -e
   ```

2. **Lister les tâches planifiées** :
   Pour afficher les tâches actuellement planifiées :
   ```bash
   crontab -l
   ```

3. **Supprimer le crontab** :
   Pour supprimer toutes les tâches planifiées (avec confirmation) :
   ```bash
   crontab -r -i
   ```

4. **Planifier une tâche** :
   Pour exécuter un script tous les jours à 2h du matin, ajoutez la ligne suivante dans le crontab :
   ```bash
   0 2 * * * /chemin/vers/script.sh
   ```

5. **Planifier une tâche chaque minute** :
   Pour exécuter une commande chaque minute :
   ```bash
   * * * * * /chemin/vers/commande
   ```

## Tips
- Utilisez `crontab -l` pour vérifier vos tâches planifiées avant de les modifier.
- Soyez prudent avec les chemins d'accès dans vos scripts, utilisez des chemins absolus pour éviter les erreurs.
- Redirigez la sortie des commandes vers un fichier log pour faciliter le débogage, par exemple :
  ```bash
  0 2 * * * /chemin/vers/script.sh >> /chemin/vers/log.txt 2>&1
  ```