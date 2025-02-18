# [Svenska] Debian Almquist Shell (dash) tr: [konvertera tecken]

## Översikt
`tr` är ett kommandoradsverktyg som används för att konvertera eller ta bort tecken i textströmmar. Det är särskilt användbart för att manipulera text genom att ersätta eller filtrera specifika tecken.

## Användning
Den grundläggande syntaxen för `tr` är:

```bash
tr [alternativ] [argument]
```

## Vanliga alternativ
- `-d`: Tar bort angivna tecken.
- `-s`: Slår samman upprepade tecken till ett enda tecken.
- `-c`: Anger komplementet av de angivna tecknen.

## Vanliga exempel

### Ersätta tecken
För att ersätta alla små bokstäver med stora bokstäver kan du använda:

```bash
echo "hej världen" | tr 'a-z' 'A-Z'
```

### Ta bort tecken
För att ta bort alla siffror från en sträng:

```bash
echo "abc123def456" | tr -d '0-9'
```

### Slå samman upprepade mellanslag
För att slå samman flera mellanslag till ett enda:

```bash
echo "Det    här   är   ett   test." | tr -s ' '
```

### Använda komplement
För att ersätta alla tecken som inte är bokstäver med ett understreck:

```bash
echo "abc123def" | tr -c 'a-zA-Z' '_'
```

## Tips
- Använd `echo` för att snabbt testa `tr`-kommandon innan du tillämpar dem på filer.
- Kombinera `tr` med andra kommandon som `grep` eller `sed` för mer avancerad textmanipulation.
- Var försiktig med tecken som kan ha speciella betydelser i skalet, som `$` eller `*`, och använd citattecken för att undvika oväntade resultat.