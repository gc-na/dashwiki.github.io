# [Danish] Debian Almquist Shell (dash) hostname brug: [vis værtsnavn]

## Oversigt
`hostname`-kommandoen bruges til at vise eller ændre systemets værtsnavn. Værtsnavnet er det navn, der identificerer en enhed på et netværk, og det er vigtigt for netværkskommunikation.

## Brug
Den grundlæggende syntaks for `hostname`-kommandoen er:

```bash
hostname [muligheder] [argumenter]
```

## Almindelige muligheder
- `-f`, `--fqdn`: Viser det fuldt kvalificerede domænenavn (FQDN).
- `-i`, `--ip-address`: Viser IP-adressen for værtsnavnet.
- `-s`, `--short`: Viser det korte værtsnavn.
- `-V`, `--version`: Viser versionsoplysninger for `hostname`.

## Almindelige eksempler
For at vise det aktuelle værtsnavn, kan du bruge:

```bash
hostname
```

For at vise det fuldt kvalificerede domænenavn:

```bash
hostname -f
```

For at vise IP-adressen for værtsnavnet:

```bash
hostname -i
```

For at ændre værtsnavnet til "ny-vært":

```bash
hostname ny-vært
```

For at vise det korte værtsnavn:

```bash
hostname -s
```

## Tips
- Husk at ændre værtsnavnet kræver administrative rettigheder, så du skal muligvis bruge `sudo`.
- Det er en god idé at opdatere `/etc/hosts`-filen, når du ændrer værtsnavnet, for at sikre korrekt netværkskommunikation.
- Brug `hostnamectl` i nyere systemer for mere avancerede indstillinger, hvis det er tilgængeligt.