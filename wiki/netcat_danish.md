# [Danish] Debian Almquist Shell (dash) netcat brug: Netværkskommunikation og fejlfinding

## Oversigt
Netcat, ofte kaldet "netværkets schweizerkniv", er et alsidigt værktøj til netværkskommunikation. Det kan bruges til at oprette forbindelser mellem computere, sende og modtage data, samt til fejlfinding af netværksproblemer.

## Brug
Den grundlæggende syntaks for netcat-kommandoen er:

```
netcat [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Lyt på en port for indkommende forbindelser.
- `-p`: Angiv portnummeret, der skal bruges.
- `-u`: Brug UDP i stedet for TCP.
- `-v`: Aktivér detaljeret (verbose) output.
- `-z`: Scan for åbne porte uden at sende data.

## Almindelige eksempler

1. **Oprette en TCP-forbindelse til en server:**
   ```bash
   netcat example.com 80
   ```

2. **Lytte på en port for indkommende forbindelser:**
   ```bash
   netcat -l -p 1234
   ```

3. **Sende en tekstfil til en server:**
   ```bash
   netcat example.com 1234 < fil.txt
   ```

4. **Modtage data og gemme det i en fil:**
   ```bash
   netcat -l -p 1234 > modtaget.txt
   ```

5. **Scanne for åbne porte på en vært:**
   ```bash
   netcat -z -v example.com 1-1000
   ```

## Tips
- Brug `-v` for at få mere information om forbindelsen, hvilket kan være nyttigt til fejlfinding.
- Vær opmærksom på firewall-indstillinger, da de kan blokere forbindelser.
- Netcat kan bruges til at oprette simple chat-applikationer ved at forbinde to terminaler sammen.