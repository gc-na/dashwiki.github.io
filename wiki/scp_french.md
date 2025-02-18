# [Français] Debian Almquist Shell (dash) scp : Transférer des fichiers de manière sécurisée

## Overview
La commande `scp` (Secure Copy Protocol) permet de transférer des fichiers de manière sécurisée entre un hôte local et un hôte distant, ou entre deux hôtes distants. Elle utilise le protocole SSH pour garantir la sécurité des données pendant le transfert.

## Usage
La syntaxe de base de la commande `scp` est la suivante :

```bash
scp [options] [source] [destination]
```

## Common Options
Voici quelques options courantes pour la commande `scp` :

- `-r` : Copie récursive des répertoires.
- `-P` : Spécifie le port à utiliser pour la connexion SSH.
- `-i` : Utilise une clé d'identification spécifique pour l'authentification.
- `-v` : Mode verbeux, affiche des informations détaillées sur le processus de transfert.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `scp` :

1. **Transférer un fichier d'un hôte local à un hôte distant :**
   ```bash
   scp fichier.txt utilisateur@hote_distant:/chemin/vers/destination/
   ```

2. **Transférer un répertoire d'un hôte local à un hôte distant :**
   ```bash
   scp -r mon_repertoire utilisateur@hote_distant:/chemin/vers/destination/
   ```

3. **Transférer un fichier d'un hôte distant à un hôte local :**
   ```bash
   scp utilisateur@hote_distant:/chemin/vers/fichier.txt /chemin/local/
   ```

4. **Utiliser un port SSH spécifique pour le transfert :**
   ```bash
   scp -P 2222 fichier.txt utilisateur@hote_distant:/chemin/vers/destination/
   ```

## Tips
- Assurez-vous que le service SSH est en cours d'exécution sur l'hôte distant avant d'utiliser `scp`.
- Pour des transferts fréquents, envisagez d'utiliser des clés SSH pour éviter de saisir votre mot de passe à chaque fois.
- Utilisez l'option `-v` pour déboguer les problèmes de connexion ou de transfert.