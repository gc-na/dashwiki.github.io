# [Linux] Debian Almquist Shell (dash) strace utilizare: Urmărirea apelurilor de sistem

## Overview
Comanda `strace` este un instrument puternic utilizat pentru a urmări apelurile de sistem și semnalele primite de un proces. Aceasta permite utilizatorilor să observe interacțiunile dintre un program și kernelul sistemului de operare, facilitând diagnosticarea problemelor și înțelegerea comportamentului aplicațiilor.

## Usage
Sintaxa de bază a comenzii `strace` este următoarea:

```bash
strace [opțiuni] [argumente]
```

## Common Options
Iată câteva opțiuni comune pentru `strace`, împreună cu explicații scurte:

- `-o <fișier>`: Scrie ieșirea în fișierul specificat în loc de stdout.
- `-e <expr>`: Filtrează apelurile de sistem pe baza expresiei date.
- `-p <PID>`: Urmărește un proces existent specificat prin PID (ID-ul procesului).
- `-c`: Afișează un rezumat al apelurilor de sistem efectuate.
- `-f`: Urmărește procesele copil create prin apeluri de sistem `fork`.

## Common Examples
Iată câteva exemple practice de utilizare a comenzii `strace`:

1. **Urmărirea unui program simplu**:
   ```bash
   strace ls
   ```

2. **Scrierea ieșirii într-un fișier**:
   ```bash
   strace -o output.txt ls
   ```

3. **Urmărirea unui proces existent**:
   ```bash
   strace -p 1234
   ```

4. **Filtrarea apelurilor de sistem**:
   ```bash
   strace -e trace=open,close ls
   ```

5. **Obținerea unui rezumat al apelurilor de sistem**:
   ```bash
   strace -c ls
   ```

## Tips
- Folosiți opțiunea `-o` pentru a salva ieșirea într-un fișier, astfel încât să puteți analiza datele mai târziu.
- Utilizați `-e` pentru a restricționa ieșirea la apelurile de sistem care vă interesează, ceea ce poate face analiza mai ușoară.
- Când urmăriți un proces existent, asigurați-vă că aveți permisiunile necesare pentru a accesa acel proces.
- Experimentați cu diferite opțiuni pentru a înțelege mai bine comportamentul aplicațiilor pe care le analizați.