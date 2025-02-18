# [Český] Debian Almquist Shell (dash) rsync použití: Synchronizace souborů a adresářů

## Přehled
Příkaz `rsync` slouží k efektivní synchronizaci souborů a adresářů mezi různými místy. Umožňuje kopírovat a synchronizovat soubory lokálně nebo přes síť, přičemž používá minimální množství dat díky své schopnosti přenášet pouze změněné části souborů.

## Použití
Základní syntaxe příkazu `rsync` je následující:

```bash
rsync [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Archivní režim, který zahrnuje rekursivní kopírování a zachování atributů souborů.
- `-v`: Verbózní výstup, který zobrazuje podrobnosti o přenášených souborech.
- `-z`: Komprese dat během přenosu, což zrychluje přenos velkých souborů.
- `-r`: Rekursivní kopírování adresářů.
- `--delete`: Odstraní soubory v cílovém umístění, které nejsou v zdrojovém umístění.

## Běžné příklady
1. **Kopírování souboru do jiného adresáře:**
   ```bash
   rsync -av /cesta/k/souboru.txt /cesta/k/cilovemu/adresari/
   ```

2. **Synchronizace celého adresáře:**
   ```bash
   rsync -av /cesta/k/adresari/ /cesta/k/cilovemu/adresari/
   ```

3. **Kopírování souborů přes SSH:**
   ```bash
   rsync -avz -e ssh /cesta/k/souboru.txt uzivatel@server:/cesta/k/cilovemu/adresari/
   ```

4. **Synchronizace s odstraněním přebytečných souborů:**
   ```bash
   rsync -av --delete /cesta/k/adresari/ /cesta/k/cilovemu/adresari/
   ```

## Tipy
- Před provedením příkazu `rsync` s možností `--delete` doporučujeme provést testovací běh s možností `-n` (suchý běh), abyste viděli, co by se změnilo.
- Používejte `-z` pro kompresi, pokud přenášíte velké soubory přes pomalé připojení.
- Vždy zkontrolujte, zda máte správně nastavené cesty k souborům a adresářům, abyste se vyhnuli nechtěným ztrátám dat.