# [Debian] Debian Almquist Shell (dash) wait : Attendre la fin d'un processus

## Overview
La commande `wait` dans le shell Almquist Debian (dash) est utilisée pour attendre la fin d'un ou plusieurs processus en arrière-plan. Elle permet de s'assurer qu'un script ne continue pas son exécution tant que les processus spécifiés ne sont pas terminés.

## Usage
La syntaxe de base de la commande `wait` est la suivante :

```sh
wait [options] [arguments]
```

## Common Options
- `PID` : Spécifie l'identifiant du processus (PID) que vous souhaitez attendre. Si aucun PID n'est fourni, `wait` attendra tous les processus en arrière-plan lancés par le shell actuel.

## Common Examples

### Attendre tous les processus en arrière-plan
Pour attendre la fin de tous les processus en arrière-plan, vous pouvez simplement utiliser :

```sh
wait
```

### Attendre un processus spécifique
Si vous avez lancé un processus en arrière-plan et que vous souhaitez attendre sa fin, utilisez son PID :

```sh
sleep 10 &
wait $!
```
Dans cet exemple, le script attendra que le processus `sleep` de 10 secondes se termine.

### Attendre plusieurs processus
Vous pouvez également attendre plusieurs processus en fournissant plusieurs PIDs :

```sh
sleep 5 &
PID1=$!
sleep 10 &
PID2=$!
wait $PID1 $PID2
```
Ici, le script attendra que les deux processus `sleep` se terminent.

## Tips
- Utilisez `wait` dans des scripts pour synchroniser des tâches qui dépendent de l'achèvement d'autres processus.
- Vérifiez le code de sortie d'un processus après l'utilisation de `wait` pour gérer les erreurs potentielles.
- Évitez d'utiliser `wait` sans spécifier de PID si vous avez plusieurs processus en arrière-plan, car cela peut rendre le débogage plus difficile.