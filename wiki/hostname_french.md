# [Debian] Debian Almquist Shell (dash) hostname : Afficher ou définir le nom d'hôte

## Overview
La commande `hostname` permet d'afficher ou de définir le nom d'hôte du système. Le nom d'hôte est un identifiant unique pour un appareil sur un réseau, facilitant son identification.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
hostname [options] [arguments]
```

## Common Options
- `-f`, `--fqdn` : Affiche le nom d'hôte complet (Fully Qualified Domain Name).
- `-i`, `--ip-address` : Affiche l'adresse IP du nom d'hôte.
- `-s`, `--short` : Affiche uniquement le nom d'hôte court.
- `-y`, `--domain` : Affiche le nom de domaine.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `hostname` :

1. Afficher le nom d'hôte actuel :

    ```bash
    hostname
    ```

2. Afficher le nom d'hôte complet :

    ```bash
    hostname -f
    ```

3. Afficher l'adresse IP du nom d'hôte :

    ```bash
    hostname -i
    ```

4. Définir un nouveau nom d'hôte :

    ```bash
    sudo hostname nouveau-nom
    ```

5. Afficher uniquement le nom d'hôte court :

    ```bash
    hostname -s
    ```

## Tips
- Utilisez `sudo` pour changer le nom d'hôte, car cela nécessite des privilèges d'administrateur.
- Pour que le changement de nom d'hôte soit permanent, modifiez également le fichier `/etc/hostname`.
- Vérifiez le fichier `/etc/hosts` pour vous assurer que le nouveau nom d'hôte est correctement mappé à l'adresse IP locale.