# [Debian] Debian Almquist Shell (dash) nice : Ajuster la priorité des processus

## Overview
La commande `nice` permet de modifier la priorité d'exécution des processus sous Unix et Linux. En ajustant la priorité, vous pouvez influencer la quantité de ressources CPU qu'un processus peut utiliser, ce qui est particulièrement utile pour gérer les performances du système.

## Usage
La syntaxe de base de la commande `nice` est la suivante :

```bash
nice [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `nice` :

- `-n, --adjustment=N` : Définit la valeur d'ajustement de la priorité. Par défaut, cette valeur est de 10.
- `-h, --help` : Affiche l'aide et les options disponibles pour la commande.
- `-v, --version` : Affiche la version de la commande `nice`.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `nice` :

1. Exécuter un script avec une priorité réduite :
   ```bash
   nice -n 10 ./mon_script.sh
   ```

2. Lancer une commande avec une priorité plus élevée :
   ```bash
   nice -n -5 ./mon_autre_script.sh
   ```

3. Vérifier la priorité d'un processus en cours d'exécution :
   ```bash
   ps -o pid,ni,cmd
   ```

4. Exécuter un programme en arrière-plan avec une priorité ajustée :
   ```bash
   nice -n 15 ./mon_programme & 
   ```

## Tips
- Utilisez des valeurs négatives pour augmenter la priorité d'un processus, mais soyez prudent, car cela peut affecter les autres processus du système.
- Vérifiez régulièrement l'utilisation des ressources avec des outils comme `top` ou `htop` pour ajuster les priorités si nécessaire.
- Évitez d'utiliser des priorités trop élevées pour des processus non critiques, afin de ne pas perturber le fonctionnement général du système.