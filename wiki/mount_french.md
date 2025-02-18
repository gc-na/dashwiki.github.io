# [Debian] Debian Almquist Shell (dash) mount : Monter des systèmes de fichiers

## Overview
La commande `mount` est utilisée pour monter des systèmes de fichiers dans le système d'exploitation. Cela permet d'accéder aux fichiers et répertoires d'un périphérique de stockage, tel qu'un disque dur, une clé USB ou un partage réseau.

## Usage
La syntaxe de base de la commande `mount` est la suivante :

```bash
mount [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `mount` :

- `-t type` : Spécifie le type de système de fichiers à monter (par exemple, `ext4`, `ntfs`, etc.).
- `-o options` : Permet de spécifier des options de montage supplémentaires, comme `ro` pour lecture seule ou `rw` pour lecture-écriture.
- `-a` : Monte tous les systèmes de fichiers énumérés dans `/etc/fstab`.
- `-r` : Monte le système de fichiers en mode lecture seule.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `mount` :

1. Monter un disque dur au format ext4 :
   ```bash
   mount -t ext4 /dev/sda1 /mnt
   ```

2. Monter une clé USB avec des options de lecture-écriture :
   ```bash
   mount -o rw /dev/sdb1 /media/usb
   ```

3. Monter tous les systèmes de fichiers définis dans `/etc/fstab` :
   ```bash
   mount -a
   ```

4. Monter un partage réseau NFS :
   ```bash
   mount -t nfs 192.168.1.100:/exported/path /mnt/nfs
   ```

## Tips
- Assurez-vous d'avoir les permissions nécessaires pour monter des systèmes de fichiers, souvent requises par l'utilisateur root.
- Vérifiez toujours que le point de montage (répertoire) est vide avant de monter un nouveau système de fichiers pour éviter de perdre des données.
- Utilisez la commande `umount` pour démonter un système de fichiers lorsque vous avez terminé, afin de libérer les ressources.