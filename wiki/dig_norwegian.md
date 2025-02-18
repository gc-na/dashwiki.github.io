# [Norsk] Debian Almquist Shell (dash) dig bruken: Hente DNS-informasjon

## Oversikt
`dig` (Domain Information Groper) er et kommandolinjeverktøy som brukes til å hente DNS-informasjon om domener. Det gir detaljerte svar fra DNS-servere og er nyttig for feilsøking av nettverksproblemer relatert til domenenavn.

## Bruk
Den grunnleggende syntaksen for `dig`-kommandoen er:

```bash
dig [alternativer] [argumenter]
```

## Vanlige alternativer
- `@server`: Angir hvilken DNS-server som skal brukes.
- `-t type`: Spesifiserer typen DNS-post (f.eks. A, MX, TXT).
- `+short`: Viser en kortere og mer konsis utdata.
- `+trace`: Følger DNS-oppslag fra roten til det spesifikke domenet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `dig`:

### Hente A-post for et domene
```bash
dig example.com
```

### Hente MX-poster for et domene
```bash
dig -t MX example.com
```

### Bruke en spesifikk DNS-server
```bash
dig @8.8.8.8 example.com
```

### Vise kortfattet utdata
```bash
dig +short example.com
```

### Følge DNS-oppslag
```bash
dig +trace example.com
```

## Tips
- Bruk `+short` for å få en rask oversikt over IP-adresser uten unødvendig informasjon.
- Når du feilsøker DNS-problemer, kan `+trace` være nyttig for å se hvor oppslaget feiler.
- Test alltid med forskjellige DNS-servere for å bekrefte at problemet ikke ligger hos en spesifikk server.