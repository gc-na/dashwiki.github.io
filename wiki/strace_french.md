# [Français] Debian Almquist Shell (dash) strace : Suivre les appels système

## Overview
La commande `strace` est un outil puissant qui permet de suivre les appels système et les signaux d'un programme en cours d'exécution. Cela peut être très utile pour le débogage et l'analyse des performances des applications.

## Usage
La syntaxe de base de la commande `strace` est la suivante :

```bash
strace [options] [arguments]
```

## Common Options
Voici quelques options courantes de `strace` avec de brèves explications :

- `-c` : Résume les statistiques des appels système effectués.
- `-e` : Filtre les appels système à tracer (par exemple, `-e trace=open` pour ne tracer que les appels `open`).
- `-o <file>` : Écrit la sortie dans un fichier spécifié au lieu de la sortie standard.
- `-p <pid>` : Attache `strace` à un processus en cours d'exécution identifié par son PID.
- `-f` : Suit les processus fils créés par le programme.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `strace` :

1. **Tracer un programme simple :**
   ```bash
   strace ls
   ```

2. **Suivre les appels système et écrire la sortie dans un fichier :**
   ```bash
   strace -o sortie.txt ls
   ```

3. **Obtenir un résumé des appels système :**
   ```bash
   strace -c ls
   ```

4. **Filtrer pour ne tracer que les appels `open` :**
   ```bash
   strace -e trace=open ls
   ```

5. **Attacher à un processus en cours d'exécution :**
   ```bash
   strace -p 1234
   ```

## Tips
- Utilisez `strace` avec prudence sur des programmes critiques, car cela peut affecter leur performance.
- Combinez `strace` avec d'autres outils comme `grep` pour filtrer les résultats et trouver des informations spécifiques.
- Familiarisez-vous avec les appels système les plus courants pour mieux comprendre les sorties de `strace`.