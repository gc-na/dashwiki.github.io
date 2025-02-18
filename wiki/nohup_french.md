# [Français] Debian Almquist Shell (dash) nohup : Exécuter des commandes sans interruption

## Overview
La commande `nohup` (no hang up) permet d'exécuter des commandes en arrière-plan, en les rendant insensibles aux signaux de déconnexion. Cela signifie que même si vous fermez votre terminal ou vous déconnectez, le processus continuera à s'exécuter.

## Usage
La syntaxe de base de la commande `nohup` est la suivante :

```bash
nohup [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `nohup` :

- `&` : Exécute la commande en arrière-plan.
- `-o` : Spécifie le fichier de sortie (par défaut, la sortie est redirigée vers `nohup.out`).
- `-h` : Affiche l'aide et les informations sur l'utilisation de la commande.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `nohup` :

1. Exécuter un script en arrière-plan :
   ```bash
   nohup ./mon_script.sh &
   ```

2. Exécuter une commande et rediriger la sortie vers un fichier spécifique :
   ```bash
   nohup ls -l > sortie.txt &
   ```

3. Exécuter un serveur web en arrière-plan :
   ```bash
   nohup python -m http.server 8000 &
   ```

4. Exécuter une tâche longue et vérifier la sortie :
   ```bash
   nohup tar -czf archive.tar.gz /dossier_long &
   ```

## Tips
- Toujours rediriger la sortie vers un fichier pour éviter de perdre des informations importantes.
- Utilisez `jobs` pour vérifier les tâches en arrière-plan et `fg` pour ramener une tâche au premier plan si nécessaire.
- Pensez à utiliser `disown` après avoir lancé une commande avec `nohup` pour vous assurer qu'elle ne sera pas affectée par la fermeture du terminal.