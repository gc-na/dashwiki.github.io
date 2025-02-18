# [Français] Debian Almquist Shell (dash) trap : [gérer les signaux]

## Overview
La commande `trap` dans le shell Debian Almquist (dash) est utilisée pour spécifier des actions à exécuter lorsque le shell reçoit certains signaux ou lorsqu'un événement particulier se produit. Cela permet de gérer le comportement des scripts en réponse à des interruptions ou des erreurs.

## Usage
La syntaxe de base de la commande `trap` est la suivante :

```sh
trap [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `trap` :

- `SIGINT` : Capture le signal d'interruption (Ctrl+C).
- `SIGTERM` : Capture le signal de terminaison.
- `EXIT` : Exécute une commande lorsque le script se termine.
- `ERR` : Exécute une commande lorsque la dernière commande échoue.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `trap` :

### Exemple 1 : Intercepter un signal d'interruption
```sh
trap 'echo "Interruption reçue!"' SIGINT
while true; do
    echo "En cours d'exécution... (appuyez sur Ctrl+C pour interrompre)"
    sleep 2
done
```

### Exemple 2 : Nettoyage à la sortie du script
```sh
trap 'echo "Nettoyage en cours..."; rm -f temp.txt' EXIT
echo "Création d'un fichier temporaire."
touch temp.txt
```

### Exemple 3 : Gestion des erreurs
```sh
trap 'echo "Une erreur s'est produite!"' ERR
false  # Cette commande échoue, ce qui déclenche le trap
```

## Tips
- Utilisez `trap` pour s'assurer que des ressources sont libérées correctement, même en cas d'interruption.
- Testez toujours vos scripts avec des signaux pour vous assurer que le comportement est celui attendu.
- Évitez d'utiliser des commandes complexes dans les actions de `trap` pour garantir une exécution rapide et fiable.