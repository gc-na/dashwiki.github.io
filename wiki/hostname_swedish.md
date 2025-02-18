# [Svenska] Debian Almquist Shell (dash) hostname användning: [visa eller ställa in värdnamn]

## Översikt
Kommandot `hostname` används för att visa eller ställa in systemets värdnamn. Värdnamnet är den identifierare som används för att referera till en dator i ett nätverk.

## Användning
Den grundläggande syntaxen för kommandot är:

```
hostname [alternativ] [argument]
```

## Vanliga alternativ
- `-f`, `--fqdn`: Visar det fullständiga kvalificerade domännamnet (FQDN) för systemet.
- `-i`, `--ip-address`: Visar IP-adressen för värdnamnet.
- `-s`, `--short`: Visar det korta värdnamnet utan domännamn.
- `--help`: Visar hjälpinformation för kommandot.
- `--version`: Visar versionsinformation för kommandot.

## Vanliga exempel
Visa det aktuella värdnamnet:
```bash
hostname
```

Visa det fullständiga kvalificerade domännamnet:
```bash
hostname -f
```

Visa IP-adressen för värdnamnet:
```bash
hostname -i
```

Ställ in ett nytt kort värdnamn:
```bash
sudo hostname new-hostname
```

Visa det korta värdnamnet:
```bash
hostname -s
```

## Tips
- Använd `sudo` för att ställa in ett nytt värdnamn, eftersom det kräver administrativa rättigheter.
- Kontrollera att det nya värdnamnet är korrekt genom att köra `hostname` efter att du har ställt in det.
- Tänk på att ändringar av värdnamnet kan påverka nätverkskonfigurationen och tjänster som är beroende av det.