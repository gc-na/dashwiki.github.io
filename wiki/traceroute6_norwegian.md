# [Norsk] Debian Almquist Shell (dash) traceroute6 bruk: Spore ruten til IPv6-adresser

## Oversikt
`traceroute6` er et verktøy som brukes til å spore ruten som datapakker tar fra en kilde til en destinasjon over et IPv6-nettverk. Det gir informasjon om hver hopp (router) pakken passerer gjennom, noe som kan være nyttig for feilsøking av nettverksproblemer.

## Bruk
Grunnleggende syntaks for `traceroute6`-kommandoen er som følger:

```bash
traceroute6 [alternativer] [argumenter]
```

## Vanlige alternativer
- `-m <hopp>`: Angir maksimal antall hopp som skal spores.
- `-p <port>`: Angir portnummeret som skal brukes i spørringene.
- `-w <sekunder>`: Angir ventetid i sekunder for å vente på svar fra hver hop.
- `-n`: Bruk IP-adresser i stedet for å forsøke å løse dem til vertsnavn.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `traceroute6`:

1. Spore ruten til en spesifikk IPv6-adresse:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Spore ruten med en spesifisert maksimal antall hopp:
   ```bash
   traceroute6 -m 20 2001:db8::1
   ```

3. Bruke en spesifikk portnummer:
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

4. Bruke `-n` for å unngå navneløsning:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

## Tips
- Når du feilsøker nettverksproblemer, kan det være nyttig å kombinere `traceroute6` med andre verktøy som `ping` for å få en bedre forståelse av nettverksytelsen.
- Vær oppmerksom på at noen nettverksrutere kan blokkere `traceroute`-forespørselen, så det kan hende at ikke alle hoppene vises.
- Bruk `-w` alternativet for å justere ventetiden hvis du opplever langsomme responser fra noen hopp.