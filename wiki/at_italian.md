# [Italiano] Debian Almquist Shell (dash) at: Pianificare l'esecuzione di comandi

## Overview
Il comando `at` consente di pianificare l'esecuzione di comandi o script a un orario specificato in futuro. È utile per automatizzare attività che devono essere eseguite una sola volta.

## Usage
La sintassi di base del comando `at` è la seguente:

```bash
at [opzioni] [tempo]
```

## Common Options
- `-f FILE`: Specifica un file contenente i comandi da eseguire.
- `-m`: Invia un'email all'utente anche se non ci sono output.
- `-q QUEUE`: Specifica la coda di esecuzione (a, b, c, ...).
- `-V`: Mostra la versione del comando `at`.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `at`:

### Eseguire un comando a un'ora specifica
Per eseguire un comando alle 15:00:

```bash
echo "echo 'Ciao, mondo!'" | at 15:00
```

### Pianificare un comando per domani
Per eseguire un comando domani alle 10:00:

```bash
echo "backup.sh" | at 10:00 tomorrow
```

### Utilizzare un file di comandi
Se hai un file chiamato `script.sh` che vuoi eseguire:

```bash
at -f script.sh 14:00
```

### Pianificare un comando con un messaggio email
Per ricevere un'email dopo l'esecuzione di un comando:

```bash
echo "echo 'Operazione completata!'" | at -m 17:00
```

## Tips
- Assicurati che il demone `atd` sia in esecuzione sul tuo sistema per poter utilizzare il comando `at`.
- Puoi controllare i lavori pianificati con il comando `atq`.
- Per annullare un lavoro pianificato, usa `atrm [job_number]`, dove `[job_number]` è il numero del lavoro visualizzato con `atq`.