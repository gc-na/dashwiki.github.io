# [Italiano] Debian Almquist Shell (dash) export utilizzo: Imposta variabili d'ambiente

## Overview
Il comando `export` in dash è utilizzato per impostare variabili d'ambiente, rendendole disponibili per i processi figli. Questo è utile quando si desidera che le variabili siano accessibili in altri script o programmi eseguiti nella stessa sessione.

## Usage
La sintassi di base del comando è la seguente:

```bash
export [options] [arguments]
```

## Common Options
- `-n`: Rimuove l'esportazione della variabile, rendendola locale.
- `-p`: Mostra tutte le variabili d'ambiente attualmente esportate.

## Common Examples

### Esempio 1: Esportare una variabile
Per esportare una variabile chiamata `MY_VAR` con il valore `Hello World`, puoi usare il seguente comando:

```bash
MY_VAR="Hello World"
export MY_VAR
```

### Esempio 2: Esportare più variabili
Puoi esportare più variabili in un singolo comando:

```bash
export VAR1="Value1" VAR2="Value2"
```

### Esempio 3: Visualizzare variabili esportate
Per visualizzare tutte le variabili d'ambiente attualmente esportate, utilizza:

```bash
export -p
```

### Esempio 4: Rimuovere l'esportazione di una variabile
Se desideri rimuovere l'esportazione di una variabile, puoi usare l'opzione `-n`:

```bash
export -n MY_VAR
```

## Tips
- Assicurati di esportare le variabili prima di eseguire uno script che ne fa uso.
- Usa nomi di variabili chiari e descrittivi per facilitare la comprensione del codice.
- Ricorda che le variabili d'ambiente sono sensibili al maiuscolo e al minuscolo; `MY_VAR` e `my_var` sono considerate variabili diverse.