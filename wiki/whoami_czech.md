# [Debian] Debian Almquist Shell (dash) whoami použití: Zjistit uživatelské jméno

## Přehled
Příkaz `whoami` v shellu dash slouží k zobrazení uživatelského jména aktuálně přihlášeného uživatele. Je to užitečný nástroj pro ověření, pod jakým uživatelským účtem právě pracujete.

## Použití
Základní syntaxe příkazu `whoami` je následující:

```
whoami [možnosti] [argumenty]
```

## Běžné možnosti
Příkaz `whoami` obvykle nemá žádné specifické možnosti, ale můžete jej použít v různých kontextech s dalšími příkazy.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `whoami`:

1. Základní použití pro zobrazení uživatelského jména:
   ```bash
   whoami
   ```

2. Použití v kombinaci s příkazem `sudo` pro ověření uživatelského jména po získání administrativních práv:
   ```bash
   sudo whoami
   ```

3. Zobrazení uživatelského jména v skriptu:
   ```bash
   echo "Aktuální uživatel je: $(whoami)"
   ```

## Tipy
- Používejte `whoami` v skriptech pro dynamické přizpůsobení chování na základě aktuálního uživatelského jména.
- Příkaz `whoami` je velmi rychlý a efektivní, takže jej můžete použít i v situacích, kdy potřebujete rychle ověřit, pod jakým účtem pracujete.
- Pokud pracujete s více uživatelskými účty, můžete `whoami` použít k ověření, zda jste přepnuli na správný účet.