# [Debian] Debian Almquist Shell (dash) shift : [déplacer les paramètres de position]

## Overview
La commande `shift` dans le shell Almquist Debian (dash) est utilisée pour décaler les paramètres de position dans un script shell. Cela signifie que les arguments passés à un script peuvent être réorganisés, permettant ainsi d'accéder facilement aux arguments suivants sans avoir à les référencer explicitement.

## Usage
La syntaxe de base de la commande `shift` est la suivante :

```sh
shift [n]
```

Ici, `n` est un nombre optionnel qui indique combien de positions doivent être décalées. Si `n` n'est pas spécifié, la commande décale par défaut d'une position.

## Common Options
- `n` : Un entier qui spécifie le nombre de positions à décaler. Si omis, le décalage est de 1.

## Common Examples

### Exemple 1 : Décalage simple
```sh
#!/bin/dash
set -- arg1 arg2 arg3
echo "Avant shift : $1"  # Affiche arg1
shift
echo "Après shift : $1"   # Affiche arg2
```

### Exemple 2 : Décalage de plusieurs positions
```sh
#!/bin/dash
set -- a b c d e
echo "Avant shift : $1"  # Affiche a
shift 2
echo "Après shift : $1"   # Affiche c
```

### Exemple 3 : Utilisation dans une boucle
```sh
#!/bin/dash
set -- param1 param2 param3
while [ "$#" -gt 0 ]; do
    echo "Traitement de : $1"
    shift
done
```

## Tips
- Utilisez `shift` dans des scripts où vous devez traiter plusieurs arguments de manière séquentielle.
- Faites attention à la valeur de `$#` (le nombre d'arguments restants) après un `shift` pour éviter d'accéder à des arguments inexistants.
- Combinez `shift` avec des structures de contrôle comme des boucles pour un traitement efficace des paramètres.