# [Debian] Debian Almquist Shell (dash) traceroute6 : tracer le chemin des paquets IPv6

## Overview
La commande `traceroute6` est utilisée pour tracer le chemin que prennent les paquets IPv6 à travers un réseau. Elle permet d'identifier les différents nœuds (routeurs) que les paquets traversent pour atteindre leur destination, ce qui peut être utile pour diagnostiquer des problèmes de connectivité.

## Usage
La syntaxe de base de la commande est la suivante :

```bash
traceroute6 [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `traceroute6` :

- `-m <max_ttl>` : Définit le nombre maximum de sauts (TTL) à suivre.
- `-p <port>` : Spécifie le port à utiliser pour l'envoi des paquets.
- `-w <timeout>` : Définit le délai d'attente en secondes pour chaque réponse.
- `-q <nqueries>` : Définit le nombre de requêtes à envoyer par saut.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `traceroute6` :

1. **Traceroute vers un hôte spécifique :**
   ```bash
   traceroute6 google.com
   ```

2. **Traceroute avec un nombre maximum de sauts de 15 :**
   ```bash
   traceroute6 -m 15 google.com
   ```

3. **Traceroute en utilisant un port spécifique :**
   ```bash
   traceroute6 -p 80 google.com
   ```

4. **Traceroute avec un délai d'attente de 2 secondes :**
   ```bash
   traceroute6 -w 2 google.com
   ```

## Tips
- Utilisez `traceroute6` pour diagnostiquer les problèmes de réseau en vérifiant où les paquets sont perdus.
- Combinez les options pour affiner vos résultats, par exemple, en ajustant le TTL et le délai d'attente.
- Vérifiez que vous avez les permissions nécessaires pour exécuter `traceroute6`, car certaines configurations réseau peuvent restreindre son utilisation.