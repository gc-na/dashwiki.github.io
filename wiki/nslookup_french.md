# [Français] Debian Almquist Shell (dash) nslookup usage : recherche d'adresses IP et de noms de domaine

## Overview
La commande `nslookup` est utilisée pour interroger les serveurs DNS afin de résoudre les noms de domaine en adresses IP et vice versa. Elle est particulièrement utile pour diagnostiquer des problèmes de réseau ou pour obtenir des informations sur un domaine.

## Usage
La syntaxe de base de la commande `nslookup` est la suivante :

```bash
nslookup [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `nslookup` :

- `-type=TYPE` : spécifie le type d'enregistrement DNS à rechercher (par exemple, A, MX, CNAME).
- `-timeout=SECONDS` : définit le délai d'attente pour la réponse du serveur DNS.
- `-retry=COUNT` : définit le nombre de tentatives de requête en cas d'échec.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `nslookup` :

1. **Résoudre un nom de domaine en adresse IP :**
   ```bash
   nslookup www.example.com
   ```

2. **Trouver l'enregistrement MX d'un domaine :**
   ```bash
   nslookup -type=MX example.com
   ```

3. **Interroger un serveur DNS spécifique :**
   ```bash
   nslookup www.example.com 8.8.8.8
   ```

4. **Vérifier l'enregistrement CNAME :**
   ```bash
   nslookup -type=CNAME www.example.com
   ```

## Tips
- Utilisez `nslookup` avec un serveur DNS public comme 8.8.8.8 (Google) pour obtenir des résultats rapides et fiables.
- Pensez à vérifier les enregistrements de plusieurs types pour obtenir une vue complète des informations DNS d'un domaine.
- Si vous rencontrez des problèmes, essayez d'augmenter le délai d'attente avec l'option `-timeout` pour des réponses plus lentes.