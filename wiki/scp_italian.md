# [Italiano] Debian Almquist Shell (dash) scp uso: Copiare file in modo sicuro tra host

## Overview
Il comando `scp` (Secure Copy Protocol) è utilizzato per copiare file e directory in modo sicuro tra host su una rete. Utilizza il protocollo SSH per garantire la sicurezza durante il trasferimento dei dati.

## Usage
La sintassi di base del comando `scp` è la seguente:

```bash
scp [opzioni] [origine] [destinazione]
```

## Common Options
- `-r`: Copia ricorsivamente directory e il loro contenuto.
- `-P`: Specifica la porta da utilizzare per la connessione SSH (la "P" maiuscola è importante).
- `-i`: Specifica un file di chiave privata da utilizzare per l'autenticazione.
- `-v`: Abilita la modalità verbose, utile per il debug.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `scp`:

1. **Copiare un file locale su un host remoto:**
   ```bash
   scp /percorso/del/file.txt utente@host_remoto:/percorso/destinazione/
   ```

2. **Copiare un file da un host remoto a locale:**
   ```bash
   scp utente@host_remoto:/percorso/del/file.txt /percorso/destinazione/
   ```

3. **Copiare una directory in modo ricorsivo su un host remoto:**
   ```bash
   scp -r /percorso/della/directory utente@host_remoto:/percorso/destinazione/
   ```

4. **Copiare un file utilizzando una porta SSH specifica:**
   ```bash
   scp -P 2222 /percorso/del/file.txt utente@host_remoto:/percorso/destinazione/
   ```

## Tips
- Assicurati di avere i permessi necessari per accedere ai file e alle directory sia sul tuo sistema che su quello remoto.
- Utilizza l'opzione `-v` per diagnosticare eventuali problemi di connessione o trasferimento.
- Considera di utilizzare chiavi SSH per un'autenticazione più sicura e per evitare di dover inserire la password ogni volta.