# [Français] Debian Almquist Shell (dash) socat : [transférer des données entre deux flux]

## Overview
La commande `socat` (SOcket CAT) est un outil puissant qui permet de créer des connexions entre différents types de flux de données. Elle peut relier des sockets, des fichiers, des terminaux, et bien d'autres, facilitant ainsi le transfert de données entre ces entités.

## Usage
La syntaxe de base de la commande `socat` est la suivante :

```bash
socat [options] [arguments]
```

## Common Options
Voici quelques options courantes de `socat` avec de courtes explications :

- `-d` : Affiche des messages de débogage.
- `-v` : Affiche les données transférées.
- `TCP:<adresse>:<port>` : Se connecte à un hôte et un port spécifiés via TCP.
- `UDP:<adresse>:<port>` : Se connecte à un hôte et un port spécifiés via UDP.
- `FILE:<nom_de_fichier>` : Utilise un fichier comme source ou destination des données.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `socat` :

1. **Transférer des données d'un port TCP à un autre :**

```bash
socat TCP-LISTEN:1234,fork TCP:localhost:5678
```

2. **Créer un tunnel UDP :**

```bash
socat UDP-LISTEN:1234,fork UDP:localhost:5678
```

3. **Rediriger un fichier vers un port TCP :**

```bash
socat FILE:/path/to/file.txt TCP:localhost:1234
```

4. **Écouter sur un port et afficher les données reçues :**

```bash
socat -v TCP-LISTEN:1234,fork -
```

## Tips
- Utilisez l'option `-d -v` pour le débogage afin de mieux comprendre ce qui se passe lors de l'exécution de vos commandes.
- Pensez à utiliser `fork` lorsque vous écoutez sur un port pour permettre à plusieurs connexions d'être gérées simultanément.
- Testez vos configurations dans un environnement sécurisé avant de les déployer en production pour éviter des fuites de données.