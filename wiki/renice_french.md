# [Français] Debian Almquist Shell (dash) renice : Modifier la priorité d'un processus

## Overview
La commande `renice` permet de modifier la priorité d'un ou plusieurs processus en cours d'exécution. En ajustant la priorité, vous pouvez influencer la quantité de ressources processeur qu'un processus reçoit, ce qui peut être utile pour optimiser les performances de votre système.

## Usage
La syntaxe de base de la commande `renice` est la suivante :

```bash
renice [options] [arguments]
```

## Common Options
- `-n`, `--priority` : Définit la nouvelle priorité pour le processus. Les valeurs peuvent aller de -20 (priorité maximale) à 19 (priorité minimale).
- `-p`, `--pid` : Spécifie le ou les identifiants de processus (PID) à modifier.
- `-g`, `--pgrp` : Modifie la priorité de tous les processus dans un groupe de processus donné.
- `-u`, `--user` : Modifie la priorité de tous les processus appartenant à un utilisateur spécifique.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `renice` :

1. Modifier la priorité d'un processus avec un PID de 1234 à une priorité de 10 :

   ```bash
   renice -n 10 -p 1234
   ```

2. Changer la priorité de tous les processus d'un utilisateur nommé "alice" à une priorité de 5 :

   ```bash
   renice -n 5 -u alice
   ```

3. Ajuster la priorité de tous les processus dans un groupe de processus avec un ID de groupe de 5678 à -5 :

   ```bash
   renice -n -5 -g 5678
   ```

4. Vérifier la priorité actuelle d'un processus avant de le modifier :

   ```bash
   ps -o pid,ni,cmd -p 1234
   ```

## Tips
- Utilisez `renice` avec prudence, car une priorité trop élevée pour un processus peut affecter la réactivité du système.
- Pour voir la liste des processus en cours et leurs priorités, vous pouvez utiliser la commande `top` ou `ps`.
- Il est souvent utile de vérifier la priorité d'un processus avant de la modifier, afin de prendre une décision éclairée.