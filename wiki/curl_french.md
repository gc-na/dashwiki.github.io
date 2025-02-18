# [Debian] Debian Almquist Shell (dash) curl : Récupérer des données à partir d'URL

## Overview
La commande `curl` est un outil en ligne de commande utilisé pour transférer des données vers ou depuis un serveur à l'aide de divers protocoles, notamment HTTP, HTTPS, FTP, et bien d'autres. Elle est particulièrement utile pour tester des API ou télécharger des fichiers.

## Usage
La syntaxe de base de la commande `curl` est la suivante :

```bash
curl [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `curl` :

- `-O` : Télécharge un fichier et le sauvegarde avec le même nom que celui sur le serveur.
- `-L` : Suit les redirections HTTP.
- `-I` : Affiche uniquement les en-têtes de la réponse.
- `-d` : Envoie des données dans une requête POST.
- `-H` : Ajoute un en-tête HTTP personnalisé à la requête.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `curl` :

1. **Télécharger un fichier :**
   ```bash
   curl -O https://example.com/fichier.txt
   ```

2. **Suivre les redirections :**
   ```bash
   curl -L https://example.com
   ```

3. **Afficher les en-têtes d'une réponse :**
   ```bash
   curl -I https://example.com
   ```

4. **Envoyer des données avec une requête POST :**
   ```bash
   curl -d "param1=valeur1&param2=valeur2" https://example.com/api
   ```

5. **Ajouter un en-tête HTTP :**
   ```bash
   curl -H "Authorization: Bearer token" https://example.com/api
   ```

## Tips
- Utilisez l'option `-v` pour activer le mode verbeux, ce qui vous permet de voir les détails de la requête et de la réponse.
- Pour des tests d'API, envisagez d'utiliser `-X` pour spécifier le type de méthode HTTP (GET, POST, PUT, DELETE, etc.).
- N'oubliez pas de vérifier les certificats SSL avec l'option `-k` si vous travaillez avec des serveurs de test, bien que cela ne soit pas recommandé pour la production.