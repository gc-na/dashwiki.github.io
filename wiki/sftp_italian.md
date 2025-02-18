# [Italiano] Debian Almquist Shell (dash) sftp utilizzo: trasferire file in modo sicuro

## Overview
Il comando `sftp` (SSH File Transfer Protocol) è utilizzato per trasferire file in modo sicuro tra un client e un server tramite una connessione SSH. È un'alternativa sicura al protocollo FTP e consente di eseguire operazioni di file come il caricamento, il download e la gestione dei file remoti.

## Usage
La sintassi di base del comando `sftp` è la seguente:

```bash
sftp [opzioni] [utente@host]
```

## Common Options
- `-P`: Specifica la porta da utilizzare per la connessione.
- `-o`: Permette di specificare opzioni di configurazione, come `IdentityFile`.
- `-b`: Esegue comandi batch da un file.
- `-v`: Attiva la modalità verbosa per il debug.

## Common Examples
Ecco alcuni esempi pratici di utilizzo del comando `sftp`:

### Connessione a un server SFTP
```bash
sftp user@hostname
```

### Trasferimento di un file dal client al server
```bash
put /percorso/del/file_locale.txt
```

### Trasferimento di un file dal server al client
```bash
get /percorso/del/file_remoto.txt
```

### Elenco dei file nella directory remota
```bash
ls
```

### Creazione di una directory remota
```bash
mkdir nuova_directory
```

### Uscita dalla sessione SFTP
```bash
bye
```

## Tips
- Assicurati di avere le autorizzazioni necessarie per accedere ai file e alle directory sul server remoto.
- Utilizza la modalità verbosa (`-v`) per diagnosticare problemi di connessione.
- Considera di utilizzare chiavi SSH per una connessione più sicura e senza password.