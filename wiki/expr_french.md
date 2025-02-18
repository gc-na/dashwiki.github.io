# [Français] Debian Almquist Shell (dash) expr : [évaluer des expressions]

## Overview
La commande `expr` est utilisée dans le shell pour évaluer des expressions arithmétiques, des chaînes de caractères et des expressions logiques. Elle permet d'effectuer des calculs simples et de manipuler des chaînes de texte dans des scripts shell.

## Usage
La syntaxe de base de la commande `expr` est la suivante :

```bash
expr [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `expr` :

- `+` : Additionne deux nombres.
- `-` : Soustrait le second nombre du premier.
- `*` : Multiplie deux nombres. Notez que l'astérisque doit être échappé avec un antislash (`\`) ou entouré de guillemets.
- `/` : Divise le premier nombre par le second.
- `%` : Renvoie le reste de la division du premier nombre par le second.
- `=` : Compare deux chaînes de caractères pour l'égalité.
- `!=` : Compare deux chaînes de caractères pour l'inégalité.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `expr` :

### Exemple 1 : Addition
Pour additionner deux nombres :

```bash
expr 5 + 3
```
*Sortie :* `8`

### Exemple 2 : Soustraction
Pour soustraire un nombre d'un autre :

```bash
expr 10 - 4
```
*Sortie :* `6`

### Exemple 3 : Multiplication
Pour multiplier deux nombres :

```bash
expr 7 \* 6
```
*Sortie :* `42`

### Exemple 4 : Division
Pour diviser un nombre par un autre :

```bash
expr 20 / 4
```
*Sortie :* `5`

### Exemple 5 : Reste de la division
Pour obtenir le reste d'une division :

```bash
expr 10 % 3
```
*Sortie :* `1`

### Exemple 6 : Comparaison de chaînes
Pour comparer deux chaînes :

```bash
expr "hello" = "hello"
```
*Sortie :* `1` (vrai)

## Tips
- Utilisez des guillemets autour des chaînes contenant des espaces pour éviter des erreurs.
- Évitez d'utiliser `expr` pour des calculs complexes ; préférez des langages comme `awk` ou `bc` pour des opérations plus avancées.
- N'oubliez pas d'échapper l'astérisque (`*`) lors de la multiplication pour éviter des erreurs de syntaxe.