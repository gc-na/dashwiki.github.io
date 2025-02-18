# [Svenska] Debian Almquist Shell (dash) expr användning: Utför beräkningar och strängoperationer

## Översikt
`expr` är ett kommando som används för att utföra enkla beräkningar och strängoperationer i shell-skript. Det kan hantera aritmetiska operationer, jämförelser och strängmanipulationer.

## Användning
Den grundläggande syntaxen för `expr` är:

```
expr [alternativ] [argument]
```

## Vanliga alternativ
- `+` : Addition av två tal.
- `-` : Subtraktion av två tal.
- `*` : Multiplikation av två tal (notera att `*` måste omges av backslashes eller citattecken).
- `/` : Division av två tal.
- `%` : Modulus (resten av division).
- `=` : Jämförelse för lika.
- `!=` : Jämförelse för inte lika.
- `>` : Jämförelse för större än.
- `<` : Jämförelse för mindre än.
- `length` : Returnerar längden på en sträng.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `expr`:

### Aritmetiska operationer
Addition av två tal:
```sh
expr 5 + 3
```

Subtraktion av två tal:
```sh
expr 10 - 4
```

Multiplikation av två tal:
```sh
expr 6 \* 7
```

Division av två tal:
```sh
expr 20 / 4
```

Modulus av två tal:
```sh
expr 10 % 3
```

### Strängoperationer
Beräkna längden på en sträng:
```sh
expr length "Hej världen"
```

Jämföra två strängar:
```sh
expr "abc" = "abc"
```

### Använda variabler
Använda `expr` med variabler:
```sh
a=5
b=3
result=$(expr $a + $b)
echo $result
```

## Tips
- Kom ihåg att använda backslashes eller citattecken runt `*` för att undvika att det tolkas som en wildcard.
- Använd `$(...)` för att fånga resultatet av `expr` i en variabel.
- `expr` är begränsat till heltal; för mer avancerade matematiska operationer, överväg att använda `bc` eller `awk`.