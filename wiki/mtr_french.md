# [Français] Debian Almquist Shell (dash) mtr : analyser les chemins réseau

## Overview
La commande `mtr` (My Traceroute) combine les fonctionnalités de `traceroute` et `ping` pour fournir des informations sur le chemin qu'un paquet de données prend pour atteindre une destination. Elle permet de diagnostiquer les problèmes de réseau en affichant la latence et la perte de paquets à chaque saut.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
mtr [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `mtr` :

- `-r` : Exécute `mtr` en mode rapport, affichant les résultats à la fin.
- `-c <count>` : Définit le nombre de paquets à envoyer pour chaque saut.
- `-i <interval>` : Définit l'intervalle entre les paquets envoyés.
- `-p` : Affiche les numéros de port utilisés pour les requêtes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `mtr` :

1. **Analyse de base d'une adresse IP ou d'un domaine :**

   ```bash
   mtr example.com
   ```

2. **Exécution d'un rapport avec un nombre défini de paquets :**

   ```bash
   mtr -r -c 10 example.com
   ```

3. **Analyse avec un intervalle de 1 seconde entre les paquets :**

   ```bash
   mtr -i 1 example.com
   ```

4. **Utilisation de `mtr` avec un port spécifique :**

   ```bash
   mtr -p 80 example.com
   ```

## Tips
- Utilisez le mode rapport (`-r`) pour obtenir une vue d'ensemble rapide des résultats après un nombre défini de paquets.
- Pour des diagnostics réguliers, envisagez d'utiliser des scripts qui exécutent `mtr` à intervalles réguliers.
- Combinez `mtr` avec d'autres outils de réseau pour une analyse plus approfondie, comme `ping` ou `traceroute`.