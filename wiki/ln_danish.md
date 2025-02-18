# [Danish] Debian Almquist Shell (dash) ln brug: Oprette links til filer

## Oversigt
`ln`-kommandoen bruges til at oprette links til filer i Unix-lignende operativsystemer. Der er to typer links: hårde links og bløde links (symboliske links). Hårde links refererer direkte til filens inode, mens symboliske links fungerer som genveje til en anden fil.

## Brug
Den grundlæggende syntaks for `ln`-kommandoen er:

```bash
ln [muligheder] [argumenter]
```

## Almindelige muligheder
- `-s`: Opretter et symbolsk link i stedet for et hårdt link.
- `-f`: Tvinger oprettelsen af linket, hvis destinationen allerede eksisterer.
- `-n`: Behandler mål som et almindeligt filnavn, hvis det allerede er en symbolsk link.
- `-v`: Viser detaljerede oplysninger om, hvad der sker under oprettelsen af linket.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `ln`-kommandoen:

1. Opret et hårdt link:
   ```bash
   ln fil.txt link_til_fil.txt
   ```

2. Opret et symbolsk link:
   ```bash
   ln -s fil.txt symbolsk_link_til_fil.txt
   ```

3. Tving oprettelsen af et link, hvis det allerede eksisterer:
   ```bash
   ln -f fil.txt link_til_fil.txt
   ```

4. Opret et symbolsk link til en mappe:
   ```bash
   ln -s /sti/til/mappe/ symbolsk_link_til_mappe
   ```

## Tips
- Brug symboliske links, når du vil have fleksibilitet til at pege på filer eller mapper, der kan ændre sig.
- Vær opmærksom på, at hårde links ikke kan oprettes på tværs af filsystemer.
- Tjek altid, om et link allerede eksisterer, før du opretter et nyt, for at undgå utilsigtede overskrivninger.