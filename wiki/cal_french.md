# [Debian] Debian Almquist Shell (dash) cal : Afficher un calendrier

## Overview
La commande `cal` permet d'afficher un calendrier dans le terminal. Elle peut afficher le calendrier d'un mois spécifique ou d'une année entière, facilitant ainsi la consultation des dates.

## Usage
La syntaxe de base de la commande `cal` est la suivante :

```bash
cal [options] [arguments]
```

## Common Options
- `-m` : Affiche le calendrier en commençant par le lundi.
- `-y` : Affiche le calendrier de l'année en cours.
- `-3` : Affiche le mois précédent, le mois courant et le mois suivant.
- `-j` : Affiche les numéros de jour julien.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `cal` :

1. Afficher le calendrier du mois courant :
   ```bash
   cal
   ```

2. Afficher le calendrier d'un mois spécifique (par exemple, mars 2023) :
   ```bash
   cal 03 2023
   ```

3. Afficher le calendrier de l'année en cours :
   ```bash
   cal -y
   ```

4. Afficher le calendrier des trois mois (précédent, courant, suivant) :
   ```bash
   cal -3
   ```

5. Afficher le calendrier avec les jours julien :
   ```bash
   cal -j
   ```

## Tips
- Utilisez l'option `-m` si vous préférez voir le calendrier commençant par le lundi, ce qui est courant dans de nombreux pays.
- Pour une consultation rapide, combinez `cal` avec d'autres commandes comme `grep` pour rechercher des dates spécifiques.
- Pensez à utiliser `man cal` pour consulter la page de manuel et découvrir d'autres options disponibles.