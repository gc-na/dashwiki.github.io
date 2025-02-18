# [Debian] Debian Almquist Shell (dash) dig : interroger les enregistrements DNS

## Overview
La commande `dig` (Domain Information Groper) est un outil puissant utilisé pour interroger les serveurs DNS. Elle permet d'obtenir des informations sur les enregistrements DNS d'un domaine, tels que les adresses IP, les enregistrements MX, et bien d'autres.

## Usage
La syntaxe de base de la commande `dig` est la suivante :

```bash
dig [options] [arguments]
```

## Common Options
Voici quelques options courantes que vous pouvez utiliser avec `dig` :

- `@server` : Spécifie le serveur DNS à interroger.
- `-t type` : Définit le type d'enregistrement à rechercher (ex. A, MX, TXT).
- `+short` : Affiche une sortie simplifiée, ne montrant que la réponse.
- `+trace` : Suit la chaîne de requêtes DNS jusqu'à la réponse finale.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `dig` :

1. **Interroger un enregistrement A :**
   ```bash
   dig example.com A
   ```

2. **Obtenir un enregistrement MX :**
   ```bash
   dig example.com MX
   ```

3. **Utiliser un serveur DNS spécifique :**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Afficher uniquement l'adresse IP :**
   ```bash
   dig example.com +short
   ```

5. **Suivre la chaîne de requêtes DNS :**
   ```bash
   dig example.com +trace
   ```

## Tips
- Utilisez l'option `+short` pour obtenir des résultats plus lisibles, surtout lorsque vous ne souhaitez que les réponses.
- Si vous travaillez avec plusieurs types d'enregistrements, envisagez d'utiliser des scripts pour automatiser les requêtes.
- Familiarisez-vous avec les différents types d'enregistrements DNS pour tirer le meilleur parti de `dig`.