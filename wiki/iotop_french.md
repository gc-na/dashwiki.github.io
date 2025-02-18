# [Français] Debian Almquist Shell (dash) iotop : surveiller l'utilisation des entrées/sorties

## Overview
La commande `iotop` permet de surveiller l'utilisation des entrées/sorties (I/O) des processus en temps réel. Elle affiche les processus qui consomment le plus de ressources I/O, ce qui est utile pour diagnostiquer des problèmes de performance liés au disque.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
iotop [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `iotop` :

- `-o` : Affiche uniquement les processus qui effectuent des opérations d'I/O.
- `-b` : Exécute `iotop` en mode batch, ce qui est utile pour les scripts.
- `-d <seconds>` : Définit l'intervalle de mise à jour en secondes.
- `-p <pid>` : Affiche uniquement les informations pour le processus avec l'identifiant spécifié.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `iotop` :

1. **Afficher l'utilisation I/O en temps réel :**
   ```bash
   iotop
   ```

2. **Afficher uniquement les processus effectuant des opérations I/O :**
   ```bash
   iotop -o
   ```

3. **Exécuter `iotop` en mode batch avec un intervalle de 5 secondes :**
   ```bash
   iotop -b -d 5
   ```

4. **Surveiller un processus spécifique par son PID :**
   ```bash
   iotop -p 1234
   ```

## Tips
- Utilisez `iotop` avec les droits d'administrateur pour obtenir des informations complètes sur tous les processus.
- Combinez `iotop` avec d'autres outils comme `htop` pour une vue d'ensemble complète des performances système.
- Pensez à utiliser le mode batch pour enregistrer les sorties dans un fichier pour une analyse ultérieure.