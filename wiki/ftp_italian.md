# [Italiano] Debian Almquist Shell (dash) ftp uso: Trasferire file tramite il protocollo FTP

## Overview
Il comando `ftp` è utilizzato per trasferire file tra un client e un server utilizzando il protocollo File Transfer Protocol (FTP). Consente di connettersi a un server FTP, caricare e scaricare file, e gestire directory.

## Usage
La sintassi di base del comando è la seguente:

```bash
ftp [options] [arguments]
```

## Common Options
- `-v`: Modalità verbosa; mostra informazioni dettagliate sulle operazioni in corso.
- `-n`: Disabilita l'autenticazione automatica; utile per script.
- `-i`: Disabilita il prompt per la conferma durante il trasferimento di file in modalità binaria.
- `-p`: Usa una connessione passiva; utile per superare firewall.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `ftp`:

### Connessione a un server FTP
```bash
ftp ftp.example.com
```

### Scaricare un file dal server
```bash
get nomefile.txt
```

### Caricare un file sul server
```bash
put nomefile.txt
```

### Visualizzare il contenuto di una directory
```bash
ls
```

### Cambiare directory sul server
```bash
cd nome_directory
```

### Uscire dalla sessione FTP
```bash
bye
```

## Tips
- Assicurati di avere le credenziali corrette per connetterti al server FTP.
- Utilizza l'opzione `-i` quando trasferisci file di grandi dimensioni per evitare conferme ripetute.
- Se hai problemi di connessione, prova a utilizzare l'opzione `-p` per una connessione passiva.