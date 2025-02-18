# [Danish] Debian Almquist Shell (dash) socat brug: [forbinder to datakanaler]

## Oversigt
`socat` er et kraftfuldt værktøj til at oprette forbindelser mellem to datakanaler. Det kan bruges til at videresende data mellem netværksforbindelser, filer, terminaler og meget mere. Det er særligt nyttigt til debugging og netværksadministration.

## Brug
Den grundlæggende syntaks for `socat`-kommandoen er:

```bash
socat [muligheder] [argumenter]
```

## Almindelige muligheder
- `-u`: Angiver, at forbindelsen skal være uretfærdig (unidirectional).
- `-v`: Aktiverer verbose output, så du kan se, hvad der sker.
- `TCP:<adresse>:<port>`: Opretter en TCP-forbindelse til den angivne adresse og port.
- `UDP:<adresse>:<port>`: Opretter en UDP-forbindelse til den angivne adresse og port.
- `FILE:<filnavn>`: Bruger en fil som datakanal.

## Almindelige eksempler

1. **Oprette en TCP-forbindelse til en server:**
   ```bash
   socat - TCP:example.com:80
   ```

2. **Oprette en UDP-forbindelse:**
   ```bash
   socat - UDP:example.com:12345
   ```

3. **Videresende data mellem to filer:**
   ```bash
   socat FILE:input.txt FILE:output.txt
   ```

4. **Oprette en lokal TCP-server, der lytter på port 8080:**
   ```bash
   socat TCP-LISTEN:8080,fork EXEC:/path/to/script.sh
   ```

5. **Forbindelse mellem en terminal og en TCP-server:**
   ```bash
   socat - TCP:localhost:8080
   ```

## Tips
- Brug `-v` for at få mere information om, hvad `socat` laver, når du fejlsøger.
- Vær opmærksom på firewall-indstillinger, som kan blokere forbindelser.
- Test altid dine forbindelser lokalt, før du implementerer dem i produktion.