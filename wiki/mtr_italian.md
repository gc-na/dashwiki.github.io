# [Italiano] Debian Almquist Shell (dash) mtr uso: tracciare la rete

## Overview
Il comando `mtr` (My Traceroute) combina le funzionalità di `ping` e `traceroute` per fornire informazioni dettagliate sul percorso che i pacchetti prendono per raggiungere un host di rete. È utile per diagnosticare problemi di connettività e per analizzare le prestazioni della rete.

## Usage
La sintassi di base del comando è la seguente:

```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: Esegue un report e termina.
- `-c <count>`: Specifica il numero di pacchetti da inviare.
- `-i <interval>`: Imposta l'intervallo tra i pacchetti inviati.
- `-p`: Mostra le porte utilizzate.
- `-n`: Non risolvere i nomi degli host, mostra solo gli indirizzi IP.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `mtr`:

1. Tracciare il percorso verso un host specifico:
   ```bash
   mtr example.com
   ```

2. Eseguire un report e terminare dopo un certo numero di pacchetti:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Tracciare un host senza risolvere i nomi:
   ```bash
   mtr -n example.com
   ```

4. Impostare un intervallo di 1 secondo tra i pacchetti:
   ```bash
   mtr -i 1 example.com
   ```

## Tips
- Utilizza l'opzione `-r` per ottenere un report finale, utile per la registrazione dei risultati.
- Se stai diagnosticando problemi di rete, prova a combinare `mtr` con altre utilità come `ping` e `traceroute` per avere una visione più completa.
- Ricorda che l'utilizzo di `mtr` può generare un carico sulla rete, quindi usalo con cautela in ambienti di produzione.