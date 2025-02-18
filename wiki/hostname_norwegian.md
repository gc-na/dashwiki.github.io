# [Norsk] Debian Almquist Shell (dash) hostname bruk: Hente og sette vertsnavn

## Oversikt
`hostname`-kommandoen brukes til å vise eller sette vertsnavnet til systemet. Vertsnavnet er det navnet som identifiserer en datamaskin i et nettverk.

## Bruk
Den grunnleggende syntaksen for `hostname`-kommandoen er:

```bash
hostname [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f`, `--fqdn`: Viser det fullstendige kvalifiserte vertsnavnet (FQDN).
- `-s`, `--short`: Viser bare det korte vertsnavnet.
- `-i`, `--ip-address`: Viser IP-adressen til vertsnavnet.
- `-V`, `--version`: Viser versjonsinformasjon om `hostname`-kommandoen.

## Vanlige eksempler
For å vise det nåværende vertsnavnet:

```bash
hostname
```

For å vise det fullstendige kvalifiserte vertsnavnet:

```bash
hostname -f
```

For å vise det korte vertsnavnet:

```bash
hostname -s
```

For å vise IP-adressen til vertsnavnet:

```bash
hostname -i
```

For å sette et nytt vertsnavn:

```bash
sudo hostname nytt-vertsnavn
```

## Tips
- Husk at endring av vertsnavn kan kreve at du oppdaterer konfigurasjonsfiler som `/etc/hosts` for å unngå nettverksproblemer.
- For permanente endringer, vurder å oppdatere `/etc/hostname`-filen.
- Bruk `hostnamectl`-kommandoen på systemer med systemd for mer avansert vertsnavnshåndtering.