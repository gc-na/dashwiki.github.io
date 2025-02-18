# [Français] Debian Almquist Shell (dash) sftp : Transférer des fichiers de manière sécurisée

## Overview
La commande `sftp` (Secure File Transfer Protocol) permet de transférer des fichiers de manière sécurisée entre un client et un serveur. Elle utilise le protocole SSH pour garantir la sécurité des données pendant le transfert.

## Usage
La syntaxe de base de la commande `sftp` est la suivante :

```bash
sftp [options] [user@]hostname
```

## Common Options
Voici quelques options courantes pour la commande `sftp` :

- `-o` : Permet de spécifier des options SSH.
- `-P` : Définit le port à utiliser pour la connexion.
- `-b` : Utilise un fichier de commandes batch pour exécuter des commandes `sftp`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `sftp` :

1. **Se connecter à un serveur SFTP :**
   ```bash
   sftp user@hostname
   ```

2. **Télécharger un fichier depuis le serveur :**
   ```bash
   get /path/to/remote/file /path/to/local/destination
   ```

3. **Téléverser un fichier vers le serveur :**
   ```bash
   put /path/to/local/file /path/to/remote/destination
   ```

4. **Lister les fichiers dans le répertoire distant :**
   ```bash
   ls
   ```

5. **Changer de répertoire sur le serveur :**
   ```bash
   cd /path/to/remote/directory
   ```

## Tips
- Toujours vérifier les permissions des fichiers sur le serveur après un transfert pour s'assurer qu'ils sont correctement configurés.
- Utiliser des clés SSH pour une connexion plus sécurisée et éviter de saisir le mot de passe à chaque fois.
- Pour des transferts de fichiers volumineux, envisagez d'utiliser la commande `-b` pour automatiser le processus avec un fichier de commandes.