# [Debian] Debian Almquist Shell (dash) basename utilizare: Extrage numele fișierului dintr-un path

## Overview
Comanda `basename` este utilizată pentru a extrage numele fișierului dintr-un path complet. Aceasta elimină toate componentele de director dintr-un path, lăsând doar numele fișierului.

## Usage
Sintaxa de bază a comenzii `basename` este următoarea:

```bash
basename [opțiuni] [argumente]
```

## Common Options
- `-a`: Procesează toate argumentele date și returnează numele de bază pentru fiecare.
- `-s`: Specifică o extensie care va fi eliminată din numele fișierului.
- `--help`: Afișează ajutorul pentru utilizarea comenzii.
- `--version`: Afișează informații despre versiunea comenzii.

## Common Examples
1. **Extrage numele fișierului dintr-un path:**

```bash
basename /usr/local/bin/script.sh
```
*Rezultatul va fi: `script.sh`*

2. **Elimină extensia din numele fișierului:**

```bash
basename /usr/local/bin/script.sh .sh
```
*Rezultatul va fi: `script`*

3. **Procesează mai multe argumente:**

```bash
basename -a /usr/local/bin/script.sh /home/user/document.txt
```
*Rezultatul va fi: `script.sh` și `document.txt`*

4. **Obține numele fișierului fără extensie:**

```bash
basename /path/to/file.tar.gz .tar.gz
```
*Rezultatul va fi: `file`*

## Tips
- Folosește opțiunea `-a` pentru a procesa mai multe fișiere simultan, economisind timp.
- Când lucrezi cu fișiere care au extensii, asigură-te că specifici corect extensia pe care dorești să o elimini.
- `basename` este util în scripturi pentru a obține numele fișierelor fără a include căile complete, facilitând manipularea acestora.