# [Français] Debian Almquist Shell (dash) ftp utilisation : Transférer des fichiers via le protocole FTP

## Overview
La commande `ftp` permet de transférer des fichiers entre un client et un serveur en utilisant le protocole File Transfer Protocol (FTP). Elle est couramment utilisée pour télécharger ou téléverser des fichiers sur des serveurs distants.

## Usage
La syntaxe de base de la commande `ftp` est la suivante :

```bash
ftp [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `ftp` :

- `-i` : Désactive le mode interactif, ce qui permet de transférer plusieurs fichiers sans confirmation.
- `-v` : Active le mode verbeux, affichant des informations détaillées sur le transfert.
- `-n` : Empêche l'auto-connexion à un serveur FTP lors du démarrage de la commande.
- `-p` : Utilise le mode passif pour établir la connexion, ce qui peut être utile derrière un pare-feu.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `ftp` :

### Connexion à un serveur FTP
```bash
ftp ftp.example.com
```

### Téléchargement d'un fichier
```bash
get fichier.txt
```

### Téléversement d'un fichier
```bash
put fichier.txt
```

### Téléchargement de plusieurs fichiers
```bash
mget *.jpg
```

### Téléversement de plusieurs fichiers
```bash
mput *.txt
```

### Quitter la session FTP
```bash
bye
```

## Tips
- Utilisez l'option `-i` pour éviter les confirmations lors du transfert de plusieurs fichiers.
- Pensez à utiliser le mode passif (`-p`) si vous rencontrez des problèmes de connexion derrière un pare-feu.
- Vérifiez toujours les permissions des fichiers sur le serveur pour éviter les erreurs lors des téléversements.