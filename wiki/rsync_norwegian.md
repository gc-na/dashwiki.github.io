# [Norsk] Debian Almquist Shell (dash) rsync bruk: Synkroniser filer og kataloger

## Oversikt
`rsync` er et kraftig verktøy for å synkronisere filer og kataloger mellom to steder, enten lokalt eller over nettverket. Det er effektivt og kan overføre bare de endrede delene av filer, noe som sparer tid og båndbredde.

## Bruk
Grunnleggende syntaks for `rsync` er som følger:
```sh
rsync [alternativer] [kilde] [mål]
```

## Vanlige alternativer
- `-a`: Arkivmodus; kopierer filer og kataloger rekursivt og bevarer metadata.
- `-v`: Verbose; viser detaljer om hva som skjer under overføringen.
- `-z`: Komprimerer data under overføring for å spare båndbredde.
- `-r`: Rekursiv; kopierer kataloger og deres innhold.
- `--delete`: Sletter filer i målplasseringen som ikke finnes i kildeplasseringen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `rsync`:

1. **Kopiere en lokal katalog til en annen lokal katalog:**
   ```sh
   rsync -av /sti/til/kilde/ /sti/til/mål/
   ```

2. **Kopiere filer fra en lokal katalog til en ekstern server:**
   ```sh
   rsync -av /sti/til/kilde/ bruker@server:/sti/til/mål/
   ```

3. **Kopiere filer fra en ekstern server til en lokal katalog:**
   ```sh
   rsync -av bruker@server:/sti/til/kilde/ /sti/til/mål/
   ```

4. **Kopiere og komprimere data under overføring:**
   ```sh
   rsync -avz /sti/til/kilde/ bruker@server:/sti/til/mål/
   ```

5. **Synkronisere og slette filer som ikke lenger finnes i kilde:**
   ```sh
   rsync -av --delete /sti/til/kilde/ /sti/til/mål/
   ```

## Tips
- Bruk `-n` (dry run) for å se hva som vil bli gjort uten å faktisk overføre filer.
- Sørg for å avslutte stien med en skråstrek (`/`) for å kopiere innholdet i katalogen i stedet for selve katalogen.
- Vær forsiktig med `--delete` alternativet, da det kan fjerne filer i målplasseringen som ikke er i kildeplasseringen.