# [Français] Debian Almquist Shell (dash) à at : planifier des tâches

## Overview
La commande `at` permet de planifier l'exécution de commandes ou de scripts à un moment précis dans le futur. Elle est utile pour automatiser des tâches sans avoir à rester connecté à un terminal.

## Usage
La syntaxe de base de la commande `at` est la suivante :

```bash
at [options] [time]
```

## Common Options
- `-f` : Spécifie un fichier contenant les commandes à exécuter.
- `-m` : Envoie un e-mail à l'utilisateur lorsque la tâche est terminée.
- `-q` : Définit la file d'attente à utiliser pour la tâche.
- `-l` : Liste les tâches planifiées pour l'utilisateur courant.
- `-d` : Supprime une tâche planifiée.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de la commande `at` :

1. **Planifier une commande pour exécution dans 5 minutes :**
   ```bash
   echo "echo 'Bonjour, le monde!'" | at now + 5 minutes
   ```

2. **Planifier une tâche à une heure précise :**
   ```bash
   echo "backup.sh" | at 14:00
   ```

3. **Utiliser un fichier pour exécuter plusieurs commandes :**
   ```bash
   at -f /path/to/script.sh 09:00
   ```

4. **Lister les tâches planifiées :**
   ```bash
   at -l
   ```

5. **Supprimer une tâche planifiée :**
   ```bash
   at -d 1
   ```

## Tips
- Assurez-vous que le service `atd` est en cours d'exécution pour que les tâches planifiées s'exécutent.
- Utilisez l'option `-m` si vous souhaitez recevoir une notification par e-mail après l'exécution de votre tâche.
- Vérifiez régulièrement vos tâches planifiées avec `at -l` pour éviter d'avoir trop de tâches en attente.