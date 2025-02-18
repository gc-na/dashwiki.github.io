# [Danish] Debian Almquist Shell (dash) scp brug: Overfør filer sikkert mellem værter

## Overview
`scp` (Secure Copy Protocol) er et værktøj, der bruges til at overføre filer mellem en lokal og en fjern computer ved hjælp af SSH (Secure Shell). Det sikrer, at dataene overføres sikkert og krypteret.

## Usage
Den grundlæggende syntaks for `scp`-kommandoen er som følger:

```bash
scp [options] [source] [destination]
```

## Common Options
Her er nogle almindelige muligheder for `scp`:

- `-r`: Kopierer mapper rekursivt.
- `-P port`: Angiver en alternativ port for SSH-forbindelsen.
- `-i identity_file`: Angiver en specifik SSH-nøgle til autentificering.
- `-v`: Aktiverer detaljeret output for fejlfinding.

## Common Examples
Her er nogle praktiske eksempler på, hvordan man bruger `scp`:

1. **Kopier en fil fra lokal til fjern server:**
   ```bash
   scp /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

2. **Kopier en fil fra fjern server til lokal maskine:**
   ```bash
   scp user@remote_host:/path/to/remote/file.txt /path/to/local/directory/
   ```

3. **Kopier en hel mappe fra lokal til fjern server:**
   ```bash
   scp -r /path/to/local/directory/ user@remote_host:/path/to/remote/directory/
   ```

4. **Kopier en fil til en specifik port:**
   ```bash
   scp -P 2222 /path/to/local/file.txt user@remote_host:/path/to/remote/directory/
   ```

## Tips
- Sørg for, at SSH-serveren kører på den fjernbetjente maskine, før du bruger `scp`.
- Brug `-v` flaget for at få mere information om forbindelsen, hvis du oplever problemer.
- Overvej at bruge SSH-nøgler til autentificering for at undgå at skulle indtaste adgangskoden hver gang.