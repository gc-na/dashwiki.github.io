# [Debian] Debian Almquist Shell (dash) true : [renvoie toujours un code de sortie vrai]

## Overview
La commande `true` dans le shell Almquist Debian (dash) est une commande simple qui renvoie toujours un code de sortie de succès (0). Elle est souvent utilisée dans des scripts pour indiquer que quelque chose a réussi ou pour remplir des espaces où une commande est attendue.

## Usage
La syntaxe de base de la commande `true` est la suivante :

```bash
true [options] [arguments]
```

## Common Options
La commande `true` n'a pas d'options ou d'arguments spécifiques. Elle est généralement utilisée telle quelle.

## Common Examples

Voici quelques exemples pratiques de l'utilisation de la commande `true` :

### Exemple 1 : Utilisation dans un script
Vous pouvez utiliser `true` pour créer un script qui ne fait rien mais réussit :

```bash
#!/bin/dash
true
echo "Le script a réussi."
```

### Exemple 2 : Boucle infinie
Dans une boucle, `true` peut être utilisé pour exécuter indéfiniment une commande :

```bash
while true; do
    echo "Cette boucle tourne indéfiniment."
    sleep 1
done
```

### Exemple 3 : Conditionnel
Vous pouvez l'utiliser dans une condition pour indiquer que quelque chose a réussi :

```bash
if true; then
    echo "Ceci s'affiche toujours."
fi
```

## Tips
- Utilisez `true` pour remplir des espaces dans des scripts où une commande est requise mais où aucune action n'est nécessaire.
- Combinez `true` avec d'autres commandes dans des scripts pour gérer des flux de contrôle sans effectuer d'actions réelles.
- Évitez d'utiliser `true` dans des scripts critiques, car il ne fait rien et pourrait rendre le débogage plus difficile si utilisé de manière inappropriée.