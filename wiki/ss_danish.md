# [Danish] Debian Almquist Shell (dash) ss brug: Vis netværksforbindelser

## Oversigt
`ss` (socket statistics) er et værktøj, der bruges til at vise information om netværksforbindelser, herunder aktive forbindelser, lytte sockets og statistikker om netværksprotokoller. Det er et effektivt alternativ til `netstat` og giver detaljerede oplysninger om netværkssockets.

## Brug
Den grundlæggende syntaks for `ss`-kommandoen er:

```bash
ss [muligheder] [argumenter]
```

## Almindelige muligheder
- `-t`: Vis kun TCP-forbindelser.
- `-u`: Vis kun UDP-forbindelser.
- `-l`: Vis kun lytte sockets.
- `-p`: Vis procesinformation for hver socket.
- `-n`: Vis numeriske adresser i stedet for at forsøge at løse dem til navne.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan du bruger `ss`:

### Vis alle aktive TCP-forbindelser
```bash
ss -t
```

### Vis alle lytte sockets
```bash
ss -l
```

### Vis UDP-forbindelser med procesinformation
```bash
ss -u -p
```

### Vis alle forbindelser med numeriske adresser
```bash
ss -n
```

### Vis detaljer om en specifik port (f.eks. port 80)
```bash
ss -t -a | grep ':80'
```

## Tips
- Brug `ss` sammen med `grep` for at filtrere resultaterne og finde specifikke forbindelser.
- Kombiner flere muligheder for at få mere præcise oplysninger, f.eks. `ss -tunlp` for at se både TCP og UDP forbindelser med procesinformation.
- `ss` kan være hurtigere end `netstat`, så det er en god idé at bruge det til fejlfinding af netværksproblemer.