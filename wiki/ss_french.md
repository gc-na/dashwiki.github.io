# [Français] Debian Almquist Shell (dash) ss : afficher les connexions réseau

## Overview
La commande `ss` est utilisée pour afficher des informations sur les connexions réseau sur un système. Elle permet de visualiser les sockets, qu'ils soient en écoute ou établis, et fournit des détails sur les protocoles utilisés.

## Usage
La syntaxe de base de la commande `ss` est la suivante :

```bash
ss [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ss` :

- `-t` : Affiche uniquement les connexions TCP.
- `-u` : Affiche uniquement les connexions UDP.
- `-l` : Affiche les sockets en écoute.
- `-p` : Affiche le processus utilisant le socket.
- `-n` : Affiche les adresses et numéros de port sous forme numérique, sans résolution de nom.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ss` :

1. Afficher toutes les connexions TCP :
   ```bash
   ss -t
   ```

2. Afficher toutes les connexions UDP :
   ```bash
   ss -u
   ```

3. Afficher les sockets en écoute :
   ```bash
   ss -l
   ```

4. Afficher les connexions avec les processus associés :
   ```bash
   ss -p
   ```

5. Afficher les connexions en utilisant des adresses numériques :
   ```bash
   ss -n
   ```

## Tips
- Utilisez l'option `-a` pour afficher à la fois les connexions établies et les sockets en écoute.
- Combinez plusieurs options pour affiner vos résultats, par exemple `ss -tunlp` pour afficher les connexions TCP et UDP avec les processus en écoute.
- Pour une sortie plus lisible, vous pouvez rediriger la sortie vers `less` : 
  ```bash
  ss -tuln | less
  ```