# [Français] Debian Almquist Shell (dash) netstat Utilisation : Afficher les connexions réseau

## Overview
La commande `netstat` est utilisée pour afficher des informations sur les connexions réseau, les tables de routage, et les statistiques des interfaces réseau. Elle est utile pour diagnostiquer des problèmes de réseau et pour surveiller l'activité réseau sur un système.

## Usage
La syntaxe de base de la commande `netstat` est la suivante :

```
netstat [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `netstat` :

- `-a` : Affiche toutes les connexions et les ports d'écoute.
- `-t` : Affiche uniquement les connexions TCP.
- `-u` : Affiche uniquement les connexions UDP.
- `-n` : Affiche les adresses et numéros de port sous forme numérique.
- `-l` : Affiche uniquement les ports en écoute.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `netstat` :

1. Afficher toutes les connexions et ports d'écoute :
   ```bash
   netstat -a
   ```

2. Afficher uniquement les connexions TCP :
   ```bash
   netstat -t
   ```

3. Afficher les connexions UDP :
   ```bash
   netstat -u
   ```

4. Afficher les connexions avec adresses et ports numériques :
   ```bash
   netstat -n
   ```

5. Afficher uniquement les ports en écoute :
   ```bash
   netstat -l
   ```

## Tips
- Utilisez `netstat -tuln` pour afficher à la fois les connexions TCP et UDP en écoute avec des adresses numériques.
- Combinez plusieurs options pour obtenir des résultats plus spécifiques, par exemple `netstat -at` pour voir uniquement les connexions TCP actives.
- Pensez à exécuter `netstat` avec des privilèges administratifs pour voir toutes les connexions, y compris celles des autres utilisateurs.