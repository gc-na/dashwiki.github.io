# [Italiano] Debian Almquist Shell (dash) dig Uso: Ottieni informazioni DNS

## Overview
Il comando `dig` (Domain Information Groper) è uno strumento utilizzato per interrogare i server DNS e ottenere informazioni dettagliate sui record DNS. È utile per risolvere nomi di dominio in indirizzi IP e per diagnosticare problemi di rete.

## Usage
La sintassi di base del comando `dig` è la seguente:

```bash
dig [opzioni] [argomenti]
```

## Common Options
Ecco alcune opzioni comuni per il comando `dig`:

- `@server`: specifica un server DNS da interrogare.
- `-t tipo`: definisce il tipo di record DNS da cercare (es. A, MX, TXT).
- `+short`: restituisce solo la risposta breve, senza dettagli aggiuntivi.
- `+trace`: segue la catena di query DNS fino alla risposta finale.

## Common Examples
Ecco alcuni esempi pratici dell'uso del comando `dig`:

1. **Interrogare un record A di un dominio:**

   ```bash
   dig example.com
   ```

2. **Interrogare un record MX (Mail Exchange) di un dominio:**

   ```bash
   dig -t MX example.com
   ```

3. **Utilizzare un server DNS specifico:**

   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Ottenere solo la risposta breve:**

   ```bash
   dig +short example.com
   ```

5. **Eseguire il tracciamento della query DNS:**

   ```bash
   dig +trace example.com
   ```

## Tips
- Utilizza l'opzione `+short` per ottenere risposte più concise, soprattutto quando non hai bisogno di dettagli complessi.
- Se stai diagnosticando problemi di rete, prova a utilizzare diversi server DNS per vedere se il problema persiste.
- Ricorda che il comando `dig` è molto utile per testare la propagazione dei record DNS dopo aver effettuato modifiche.