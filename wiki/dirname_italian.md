# [Italiano] Debian Almquist Shell (dash) dirname Uso: Estrae il nome della directory da un percorso

## Overview
Il comando `dirname` è utilizzato per estrarre il nome della directory da un percorso di file. Questo è utile quando si desidera ottenere solo la parte della directory di un percorso completo, escludendo il nome del file.

## Usage
La sintassi di base del comando `dirname` è la seguente:

```bash
dirname [opzioni] [argomenti]
```

## Common Options
- `-z`: Tratta gli argomenti come stringhe terminate da null.
- `--help`: Mostra un messaggio di aiuto con le opzioni disponibili.
- `--version`: Mostra la versione del comando.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `dirname`:

1. Estrazione del nome della directory da un percorso completo:
   ```bash
   dirname /home/utente/documenti/file.txt
   ```
   Output:
   ```
   /home/utente/documenti
   ```

2. Utilizzo con un percorso relativo:
   ```bash
   dirname ./immagini/foto.jpg
   ```
   Output:
   ```
   ./immagini
   ```

3. Estrazione del nome della directory da un percorso con più livelli:
   ```bash
   dirname /var/log/syslog
   ```
   Output:
   ```
   /var/log
   ```

4. Utilizzo in uno script per ottenere la directory corrente:
   ```bash
   DIR=$(dirname "$0")
   echo "La directory dello script è: $DIR"
   ```

## Tips
- Utilizza `dirname` in combinazione con altri comandi, come `basename`, per manipolare i percorsi dei file in modo più efficace.
- Ricorda che `dirname` restituisce sempre il percorso della directory, anche se il percorso fornito non contiene un file.
- Puoi usare `dirname` all'interno di script per gestire i percorsi in modo dinamico, facilitando la gestione dei file e delle directory.