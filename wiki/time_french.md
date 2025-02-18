# [Debian] Debian Almquist Shell (dash) time : mesurer le temps d'exécution d'une commande

## Overview
La commande `time` est utilisée pour mesurer le temps d'exécution d'une commande dans le shell. Elle fournit des informations sur le temps réel, le temps CPU utilisé en mode utilisateur et en mode système.

## Usage
La syntaxe de base de la commande `time` est la suivante :

```bash
time [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `time` :

- `-p` : Affiche le temps au format POSIX.
- `-o fichier` : Redirige la sortie vers un fichier spécifié.
- `-v` : Affiche des informations détaillées sur l'exécution.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `time` :

1. Mesurer le temps d'exécution d'une commande simple :

   ```bash
   time ls -l
   ```

2. Enregistrer la sortie dans un fichier :

   ```bash
   time -o resultat.txt sleep 2
   ```

3. Afficher des informations détaillées sur l'exécution :

   ```bash
   time -v find / -name "fichier.txt"
   ```

4. Mesurer le temps d'exécution d'un script :

   ```bash
   time ./mon_script.sh
   ```

## Tips
- Utilisez l'option `-p` si vous souhaitez un format de sortie plus simple et conforme à POSIX.
- Pensez à rediriger la sortie vers un fichier si vous exécutez des commandes longues pour garder une trace des résultats.
- Pour des scripts complexes, l'option `-v` peut fournir des informations utiles pour l'optimisation des performances.