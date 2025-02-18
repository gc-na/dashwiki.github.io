# [Danish] Debian Almquist Shell (dash) traceroute6 brug: Spore IPv6-netværksruter

## Overview
`traceroute6` er et værktøj, der bruges til at spore ruten, som IPv6-pakker tager fra en kilde til en destination. Det viser hver hop, som pakken passerer igennem, hvilket kan være nyttigt til fejlfinding af netværksproblemer.

## Usage
Den grundlæggende syntaks for `traceroute6`-kommandoen er:

```bash
traceroute6 [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `traceroute6`:

- `-n`: Vis IP-adresser i stedet for at forsøge at opnå værtsnavne.
- `-m <hops>`: Angiv det maksimale antal hop, der skal spores.
- `-w <seconds>`: Angiv ventetid for hver svarpakke.
- `-p <port>`: Angiv portnummeret, der skal bruges til at sende pakkerne.

## Common Examples
Her er nogle praktiske eksempler på brugen af `traceroute6`:

1. Spore ruten til en specifik IPv6-adresse:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Spore ruten uden at vise værtsnavne:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

3. Angive et maksimalt antal hop til 15:
   ```bash
   traceroute6 -m 15 2001:db8::1
   ```

4. Angive en ventetid på 2 sekunder for hver pakke:
   ```bash
   traceroute6 -w 2 2001:db8::1
   ```

## Tips
- Brug `-n` for at fremskynde output, især hvis DNS-opslag er langsomme.
- Vær opmærksom på, at nogle netværk kan blokere `traceroute`-pakker, hvilket kan føre til ufuldstændige resultater.
- Test altid med forskellige destinationer for at få en bedre forståelse af netværksstrukturen.