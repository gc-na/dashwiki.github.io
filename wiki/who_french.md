# [Debian] Debian Almquist Shell (dash) qui : Affiche les utilisateurs connectés

## Aperçu
La commande `who` permet d'afficher une liste des utilisateurs actuellement connectés au système. Elle fournit des informations telles que le nom d'utilisateur, le terminal, la date et l'heure de connexion, ainsi que l'adresse IP ou le nom d'hôte, le cas échéant.

## Utilisation
La syntaxe de base de la commande `who` est la suivante :

```bash
who [options] [arguments]
```

## Options courantes
- `-b` : Affiche la dernière date et heure de redémarrage du système.
- `-q` : Affiche uniquement les noms d'utilisateur et le nombre d'utilisateurs connectés.
- `-H` : Affiche les en-têtes de colonne pour les informations affichées.

## Exemples courants
Voici quelques exemples pratiques de l'utilisation de la commande `who` :

1. **Afficher tous les utilisateurs connectés :**
   ```bash
   who
   ```

2. **Afficher uniquement les noms d'utilisateur et le nombre d'utilisateurs connectés :**
   ```bash
   who -q
   ```

3. **Afficher la dernière date et heure de redémarrage du système :**
   ```bash
   who -b
   ```

4. **Afficher les utilisateurs connectés avec des en-têtes de colonne :**
   ```bash
   who -H
   ```

## Conseils
- Utilisez `who -q` pour obtenir rapidement un aperçu du nombre d'utilisateurs connectés sans trop de détails.
- Combinez `who` avec d'autres commandes comme `grep` pour filtrer les résultats selon des critères spécifiques.
- Pensez à utiliser `man who` pour consulter le manuel et découvrir d'autres options disponibles.