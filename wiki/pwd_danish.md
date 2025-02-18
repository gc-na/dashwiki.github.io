# [Danish] Debian Almquist Shell (dash) pwd brug: Viser den aktuelle arbejdsmappe

## Oversigt
`pwd` (print working directory) er en kommando, der viser den aktuelle arbejdsmappe i terminalen. Det er nyttigt, når du vil vide, hvor du befinder dig i filsystemet.

## Brug
Den grundlæggende syntaks for `pwd`-kommandoen er som følger:

```bash
pwd [options] [arguments]
```

## Almindelige muligheder
- `-L`: Viser den logiske sti til den aktuelle arbejdsmappe.
- `-P`: Viser den fysiske sti til den aktuelle arbejdsmappe, hvilket betyder, at den viser den faktiske placering uden symboliske links.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `pwd`:

1. For at vise den aktuelle arbejdsmappe:
   ```bash
   pwd
   ```

2. For at vise den fysiske sti:
   ```bash
   pwd -P
   ```

3. For at vise den logiske sti:
   ```bash
   pwd -L
   ```

## Tips
- Brug `pwd` regelmæssigt for at holde styr på, hvor du er i filsystemet, især når du navigerer gennem flere mapper.
- Kombiner `pwd` med andre kommandoer som `cd` for at sikre, at du altid ved, hvor du arbejder.