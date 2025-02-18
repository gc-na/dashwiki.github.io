# [Český] Debian Almquist Shell (dash) crontab použití: Naplánování úloh

## Přehled
Příkaz `crontab` slouží k plánování automatického spouštění úloh v pravidelných intervalech. Umožňuje uživatelům definovat, kdy a jak často se mají určité příkazy nebo skripty vykonávat.

## Použití
Základní syntaxe příkazu `crontab` je následující:

```
crontab [možnosti] [argumenty]
```

## Běžné možnosti
- `-e`: Otevře aktuální crontab pro úpravy.
- `-l`: Vypíše aktuální crontab.
- `-r`: Odstraní aktuální crontab.
- `-i`: Potvrzení před odstraněním crontabu (používá se s `-r`).

## Běžné příklady
1. **Otevření crontabu pro úpravy:**
   ```sh
   crontab -e
   ```

2. **Zobrazení aktuálního crontabu:**
   ```sh
   crontab -l
   ```

3. **Odstranění aktuálního crontabu:**
   ```sh
   crontab -r
   ```

4. **Naplánování úlohy na každou minutu:**
   ```
   * * * * * /cesta/k/vašemu/skriptu.sh
   ```

5. **Naplánování úlohy na každý den v 5:00:**
   ```
   0 5 * * * /cesta/k/vašemu/skriptu.sh
   ```

## Tipy
- Ujistěte se, že skripty, které plánujete spouštět, mají správná oprávnění pro vykonávání.
- Používejte absolutní cesty k souborům a skriptům, aby se předešlo problémům s cestami.
- Zapisujte výstupy úloh do logů, abyste mohli sledovat, co se děje, například:
  ```
  * * * * * /cesta/k/vašemu/skriptu.sh >> /cesta/k/logu.log 2>&1
  ```