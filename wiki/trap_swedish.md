# [Svenska] Debian Almquist Shell (dash) trap användning: Hantera signaler och städa upp

## Översikt
Kommandot `trap` i Debian Almquist Shell (dash) används för att fånga och hantera signaler och händelser i skript. Det gör att du kan utföra specifika åtgärder när ett skript får en viss signal, vilket är användbart för att städa upp resurser eller avsluta processer på ett kontrollerat sätt.

## Användning
Den grundläggande syntaxen för kommandot `trap` är:

```sh
trap [alternativ] [kommandon]
```

## Vanliga alternativ
- `SIGINT`: Fångar avbrottssignalen (Ctrl+C).
- `SIGTERM`: Fångar avslutningssignalen.
- `EXIT`: Kör kommandon när skriptet avslutas.
- `ERR`: Kör kommandon om ett fel inträffar.

## Vanliga exempel

### Fånga avbrottssignal
Detta exempel fångar Ctrl+C och skriver ut ett meddelande innan skriptet avslutas.

```sh
trap 'echo "Avbruten!"; exit' SIGINT
while true; do
    echo "Kör... (tryck Ctrl+C för att avbryta)"
    sleep 1
done
```

### Rensa temporära filer vid avslutning
Detta exempel rensar temporära filer när skriptet avslutas.

```sh
trap 'rm -f /tmp/tempfile' EXIT
echo "Skapar en temporär fil..."
touch /tmp/tempfile
# Gör något med filen
```

### Hantera fel
Detta exempel fångar fel och skriver ut ett meddelande.

```sh
trap 'echo "Ett fel inträffade!"' ERR
# Exempel på ett kommando som kan misslyckas
false
```

## Tips
- Använd `trap` för att säkerställa att resurser alltid städas upp, även om skriptet avbryts oväntat.
- Testa alltid dina skript noggrant för att se till att signalhanteringen fungerar som förväntat.
- Kom ihåg att `trap` kan användas för att fånga flera signaler genom att separera dem med ett mellanslag.