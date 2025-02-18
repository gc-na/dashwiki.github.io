# [Italiano] Debian Almquist Shell (dash) nslookup utilizzo: Strumento per interrogare server DNS

## Overview
Il comando `nslookup` è utilizzato per interrogare i server DNS al fine di ottenere informazioni sui nomi di dominio, come gli indirizzi IP associati. È uno strumento utile per la risoluzione dei problemi di rete e per verificare la configurazione DNS.

## Usage
La sintassi di base del comando è la seguente:

```
nslookup [opzioni] [argomenti]
```

## Common Options
- `-type=tipo`: Specifica il tipo di record DNS da cercare (ad esempio, A, MX, CNAME).
- `-timeout=secondi`: Imposta il tempo di attesa per la risposta del server DNS.
- `-retry=numero`: Definisce il numero di tentativi di richiesta in caso di mancata risposta.

## Common Examples
Ecco alcuni esempi pratici dell'uso di `nslookup`:

### Esempio 1: Ottenere l'indirizzo IP di un dominio
```bash
nslookup www.example.com
```

### Esempio 2: Cercare un record MX per un dominio
```bash
nslookup -type=MX example.com
```

### Esempio 3: Specificare un server DNS diverso
```bash
nslookup www.example.com 8.8.8.8
```

### Esempio 4: Controllare il tipo di record CNAME
```bash
nslookup -type=CNAME www.example.com
```

## Tips
- Utilizza `nslookup` in modalità interattiva per eseguire più query senza dover digitare il comando ogni volta.
- Verifica sempre di avere una connessione a Internet attiva quando utilizzi `nslookup`, poiché richiede l'accesso ai server DNS.
- Ricorda che i risultati possono variare a seconda del server DNS utilizzato, quindi prova a cambiare server se ottieni risultati inattesi.