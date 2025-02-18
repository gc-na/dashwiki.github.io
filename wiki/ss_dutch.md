# [Nederlands] Debian Almquist Shell (dash) ss gebruik: Netwerkverbindingen bekijken

## Overzicht
De `ss`-opdracht is een hulpmiddel dat wordt gebruikt om netwerkverbindingen te bekijken en te analyseren. Het biedt gedetailleerde informatie over actieve verbindingen, sockets en hun status, wat nuttig kan zijn voor netwerkbeheer en probleemoplossing.

## Gebruik
De basis syntaxis van de `ss`-opdracht is als volgt:

```bash
ss [opties] [argumenten]
```

## Veelvoorkomende opties
- `-t`: Toont alleen TCP-sockets.
- `-u`: Toont alleen UDP-sockets.
- `-l`: Toont alleen luisterende sockets.
- `-p`: Toont het proces dat de socket gebruikt.
- `-n`: Toont IP-adressen en poorten in numerieke vorm, zonder DNS-resolutie.

## Veelvoorkomende voorbeelden

1. **Toon alle actieve verbindingen:**
   ```bash
   ss
   ```

2. **Toon alleen TCP-verbindingen:**
   ```bash
   ss -t
   ```

3. **Toon alleen luisterende sockets:**
   ```bash
   ss -l
   ```

4. **Toon UDP-sockets met procesinformatie:**
   ```bash
   ss -u -p
   ```

5. **Toon verbindingen met numerieke adressen:**
   ```bash
   ss -n
   ```

## Tips
- Gebruik de optie `-s` om een samenvatting van de sockets te krijgen, wat handig kan zijn voor een snel overzicht.
- Combineer opties voor meer gerichte informatie, bijvoorbeeld `ss -t -l` om alleen luisterende TCP-sockets te zien.
- Regelmatig gebruik van `ss` kan helpen bij het monitoren van netwerkactiviteit en het identificeren van ongewenste verbindingen.