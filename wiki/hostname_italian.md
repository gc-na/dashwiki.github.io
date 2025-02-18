# [Italiano] Debian Almquist Shell (dash) hostname uso: [visualizzare o impostare il nome dell'host]

## Overview
Il comando `hostname` in dash viene utilizzato per visualizzare o impostare il nome dell'host del sistema. Il nome dell'host è l'identificatore del computer sulla rete e può essere importante per la configurazione di rete e per l'identificazione del sistema.

## Usage
La sintassi di base del comando è la seguente:

```bash
hostname [opzioni] [argomenti]
```

## Common Options
- `-f`, `--fqdn`: Mostra il nome di dominio completamente qualificato (FQDN) dell'host.
- `-s`, `--short`: Mostra solo il nome host breve.
- `-i`, `--ip-address`: Mostra l'indirizzo IP associato al nome dell'host.
- `-V`, `--version`: Mostra la versione del comando `hostname`.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `hostname`:

1. **Visualizzare il nome dell'host attuale:**
   ```bash
   hostname
   ```

2. **Visualizzare il nome di dominio completamente qualificato:**
   ```bash
   hostname -f
   ```

3. **Visualizzare solo il nome host breve:**
   ```bash
   hostname -s
   ```

4. **Visualizzare l'indirizzo IP associato al nome dell'host:**
   ```bash
   hostname -i
   ```

5. **Impostare un nuovo nome dell'host:**
   ```bash
   sudo hostname nuovo-nome-host
   ```

## Tips
- Ricorda che per modificare il nome dell'host è necessario avere i privilegi di superutente.
- Dopo aver cambiato il nome dell'host, potrebbe essere necessario riavviare il sistema o riavviare i servizi di rete per applicare le modifiche.
- È buona pratica mantenere il nome dell'host breve e significativo, per facilitare l'identificazione del sistema nella rete.