# [Český] Debian Almquist Shell (dash) traceroute použití: Sleduje cestu paketů v síti

## Přehled
Příkaz `traceroute` slouží k sledování cesty, kterou pakety procházejí z vašeho počítače na cílovou adresu v síti. Pomocí tohoto nástroje můžete zjistit, jaké servery a směrovače pakety procházejí a jak dlouho trvá, než se dostanou na cílovou destinaci.

## Použití
Základní syntaxe příkazu je následující:

```
traceroute [možnosti] [argumenty]
```

## Běžné možnosti
- `-m <max_hops>`: Určuje maximální počet skoků (hops), které traceroute provede.
- `-w <timeout>`: Nastavuje časový limit pro čekání na odpověď od každého skoku.
- `-n`: Zobrazí IP adresy místo jejich překladu na doménová jména.
- `-p <port>`: Určuje port, který se má použít pro UDP pakety.

## Běžné příklady
1. Základní použití pro sledování cesty k doméně:
   ```bash
   traceroute example.com
   ```

2. Sledování cesty s maximálním počtem skoků nastaveným na 15:
   ```bash
   traceroute -m 15 example.com
   ```

3. Zobrazení pouze IP adres bez překladů na doménová jména:
   ```bash
   traceroute -n example.com
   ```

4. Sledování cesty s nastaveným časovým limitem 2 sekundy:
   ```bash
   traceroute -w 2 example.com
   ```

5. Použití specifického portu pro sledování:
   ```bash
   traceroute -p 80 example.com
   ```

## Tipy
- Při analýze výsledků věnujte pozornost vysokým latencím, které mohou indikovat problémy v síti.
- Používejte možnost `-n`, pokud chcete zrychlit proces sledování, zejména v případě, že DNS překlady trvají příliš dlouho.
- Pokud narazíte na firewall, který blokuje UDP pakety, zkuste použít TCP pakety pomocí příkazu `tcptraceroute`, pokud je k dispozici.