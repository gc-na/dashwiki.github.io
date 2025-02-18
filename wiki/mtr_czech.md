# [Český] Debian Almquist Shell (dash) mtr použití: sledování cesty k síťovému cíli

## Přehled
Příkaz `mtr` (My Traceroute) kombinuje funkce příkazů `traceroute` a `ping`. Umožňuje sledovat cestu paketů k cílové IP adrese nebo doméně a zároveň měřit latenci a ztrátu paketů na jednotlivých skocích.

## Použití
Základní syntaxe příkazu `mtr` je následující:

```
mtr [možnosti] [argumenty]
```

## Běžné možnosti
- `-r`: Spustí mtr v režimu reportu, který provede měření a poté ukončí.
- `-c [číslo]`: Určuje počet pingů, které se mají provést.
- `-i [čas]`: Nastavuje interval mezi jednotlivými pings.
- `-p`: Zobrazí porty, které jsou použity pro testování.

## Běžné příklady
1. Základní použití pro sledování cesty k doméně:
   ```bash
   mtr example.com
   ```

2. Spuštění v režimu reportu s 10 pings:
   ```bash
   mtr -r -c 10 example.com
   ```

3. Sledování cesty s nastavením intervalu 1 sekundy mezi pings:
   ```bash
   mtr -i 1 example.com
   ```

4. Zobrazení portů pro konkrétní IP adresu:
   ```bash
   mtr -p 192.168.1.1
   ```

## Tipy
- Používejte `mtr` s volbou `-r`, pokud chcete získat rychlý přehled o cestě a latenci bez neustálého aktualizování.
- Mějte na paměti, že některé sítě mohou blokovat ICMP pakety, což může ovlivnit výsledky.
- Pro podrobnější analýzu můžete kombinovat možnosti, například `-c` a `-i`, abyste získali přesnější měření.