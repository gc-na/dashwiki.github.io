# [Český] Debian Almquist Shell (dash) shift použití: Posun argumentů v příkazové řádce

## Přehled
Příkaz `shift` se používá k posunutí argumentů v příkazové řádce. Když je tento příkaz proveden, první argument `$1` se odstraní a všechny ostatní argumenty se posunou o jedno místo doleva. To je užitečné, když chcete zpracovat argumenty v cyklu nebo je zpracovávat postupně.

## Použití
Základní syntaxe příkazu je následující:

```sh
shift [n]
```

Kde `n` je volitelný argument, který určuje, kolik pozic se má posunout. Pokud není zadáno, posune se o 1.

## Běžné možnosti
- `n`: Číslo, které určuje, o kolik pozic se mají argumenty posunout. Například `shift 2` posune argumenty o dvě místa.

## Běžné příklady

### Příklad 1: Základní použití
Posunout argumenty o jedno místo:

```sh
set -- a b c d
echo $1  # Výstup: a
shift
echo $1  # Výstup: b
```

### Příklad 2: Posunout více argumentů
Posunout argumenty o dvě místa:

```sh
set -- a b c d
echo $1  # Výstup: a
shift 2
echo $1  # Výstup: c
```

### Příklad 3: Zpracování argumentů v cyklu
Zpracování všech argumentů pomocí cyklu:

```sh
set -- arg1 arg2 arg3 arg4
while [ "$#" -gt 0 ]; do
    echo "Zpracovávám: $1"
    shift
done
```

## Tipy
- Používejte `shift` v cyklech, když potřebujete zpracovat argumenty jeden po druhém.
- Pamatujte, že po použití `shift` se argumenty mění, takže buďte opatrní při jejich dalším použití.
- Pokud potřebujete posunout více než jeden argument, nezapomeňte použít `shift n`, kde `n` je počet pozic, které chcete posunout.