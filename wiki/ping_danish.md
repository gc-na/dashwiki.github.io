# [Danish] Debian Almquist Shell (dash) ping brug: Tester netværksforbindelse

## Overview
`ping`-kommandoen bruges til at teste netværksforbindelsen mellem din computer og en anden enhed på netværket. Den sender ICMP (Internet Control Message Protocol) echo-anmodninger til den angivne adresse og venter på svar. Dette hjælper med at identificere, om en enhed er tilgængelig og måle forsinkelsen i forbindelsen.

## Usage
Den grundlæggende syntaks for `ping`-kommandoen er:

```bash
ping [options] [arguments]
```

## Common Options
- `-c [count]`: Angiver, hvor mange ping-forespørgsler der skal sendes.
- `-i [interval]`: Angiver intervallet mellem hver ping-anmodning i sekunder.
- `-t [ttl]`: Sætter Time To Live (TTL) for pakkerne.
- `-s [size]`: Angiver størrelsen på dataene, der sendes i ping-anmodningen.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge `ping`-kommandoen:

1. **Ping en webadresse:**
   ```bash
   ping www.example.com
   ```

2. **Ping en IP-adresse med et bestemt antal anmodninger:**
   ```bash
   ping -c 4 192.168.1.1
   ```

3. **Ping en adresse med et specifikt interval mellem anmodningerne:**
   ```bash
   ping -i 2 www.example.com
   ```

4. **Ping med en specifik pakke størrelse:**
   ```bash
   ping -s 128 www.example.com
   ```

## Tips
- Brug `-c`-muligheden for at begrænse antallet af anmodninger, så du ikke overbelaster netværket.
- Tjek netværksforbindelsen til en server, før du fejlsøger applikationsproblemer.
- Hvis du ikke får svar, kan det være nyttigt at kontrollere firewall-indstillingerne på både din enhed og den enhed, du prøver at pinge.