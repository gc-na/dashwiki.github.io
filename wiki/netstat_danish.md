# [Danish] Debian Almquist Shell (dash) netstat brug: Viser netværksforbindelser og statistikker

## Oversigt
`netstat` er et kommandolinjeværktøj, der bruges til at vise netværksforbindelser, routing-tabeller, interface-statistikker og meget mere. Det er nyttigt til fejlfinding af netværksproblemer og overvågning af netværksaktivitet.

## Brug
Den grundlæggende syntaks for `netstat`-kommandoen er:

```bash
netstat [options] [arguments]
```

## Almindelige muligheder
- `-a`: Viser alle forbindelser og lytteporte.
- `-n`: Viser adresser og portnumre i numerisk format.
- `-t`: Viser TCP-forbindelser.
- `-u`: Viser UDP-forbindelser.
- `-l`: Viser kun lytteporte.
- `-p`: Viser process-id og programnavn, der bruger forbindelsen.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `netstat`:

1. **Vis alle aktive forbindelser:**

   ```bash
   netstat -a
   ```

2. **Vis TCP-forbindelser i numerisk format:**

   ```bash
   netstat -tn
   ```

3. **Vis lytteporte for både TCP og UDP:**

   ```bash
   netstat -tuln
   ```

4. **Vis netværksstatistikker for hver interface:**

   ```bash
   netstat -i
   ```

5. **Vis forbindelser med tilknyttede processer:**

   ```bash
   netstat -p
   ```

## Tips
- Brug `netstat -an` for at få en hurtig oversigt over alle forbindelser uden at vise procesinformation.
- Kombiner `netstat` med `grep` for at filtrere resultaterne, f.eks. `netstat -a | grep LISTEN` for kun at vise lytteporte.
- Overvej at bruge `ss`-kommandoen som et alternativ til `netstat`, da den kan give mere detaljerede oplysninger og er hurtigere i moderne systemer.