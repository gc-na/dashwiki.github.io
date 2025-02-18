# [Italiano] Debian Almquist Shell (dash) cd uso: Cambiare directory

## Overview
Il comando `cd` (change directory) è utilizzato per cambiare la directory di lavoro corrente nel terminale. Questo comando è fondamentale per navigare tra le diverse cartelle del file system.

## Usage
La sintassi di base del comando `cd` è la seguente:

```bash
cd [opzioni] [argomenti]
```

## Common Options
- `..` : Torna alla directory padre.
- `-` : Torna all'ultima directory visitata.
- `~` : Passa alla home directory dell'utente corrente.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `cd`:

1. **Cambiare alla directory principale dell'utente:**
   ```bash
   cd ~
   ```

2. **Tornare alla directory padre:**
   ```bash
   cd ..
   ```

3. **Tornare all'ultima directory visitata:**
   ```bash
   cd -
   ```

4. **Cambiare a una directory specifica:**
   ```bash
   cd /path/to/directory
   ```

5. **Navigare in una sottodirectory:**
   ```bash
   cd Documents
   ```

## Tips
- Utilizza `cd -` per tornare rapidamente all'ultima directory in cui ti trovavi.
- Ricorda che il percorso può essere assoluto (inizia con `/`) o relativo (senza `/`).
- Usa `tab` per completare automaticamente i nomi delle directory e ridurre gli errori di battitura.