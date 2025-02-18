# [Danish] Debian Almquist Shell (dash) rsync brug: Synkronisering af filer

## Oversigt
`rsync` er et kraftfuldt værktøj til at synkronisere filer og mapper mellem to placeringer. Det kan bruges til at kopiere filer lokalt eller til at overføre dem over et netværk. `rsync` er kendt for sin effektivitet, da det kun overfører de ændrede dele af filer, hvilket sparer båndbredde og tid.

## Brug
Den grundlæggende syntaks for `rsync` er som følger:

```bash
rsync [muligheder] [kilde] [destination]
```

## Almindelige muligheder
- `-a`: Aktiverer arkivtilstand, som bevarer filrettigheder, tidsstempler og symlinks.
- `-v`: Viser detaljeret output under overførslen (verbose).
- `-z`: Komprimerer data under overførslen for at spare båndbredde.
- `-r`: Rekursiv kopiering af mapper.
- `--delete`: Sletter filer i destinationsmappen, der ikke længere findes i kilde-mappen.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `rsync` kan bruges:

1. **Kopiere en lokal mappe til en anden lokal mappe:**
   ```bash
   rsync -av /sti/til/kilde/ /sti/til/destination/
   ```

2. **Kopiere filer fra en lokal mappe til en fjernserver:**
   ```bash
   rsync -avz /sti/til/kilde/ bruger@server:/sti/til/destination/
   ```

3. **Synkronisere en lokal mappe med en fjernmappe og slette filer, der ikke længere findes i kilden:**
   ```bash
   rsync -av --delete /sti/til/kilde/ bruger@server:/sti/til/destination/
   ```

4. **Kopiere filer fra en fjernserver til en lokal mappe:**
   ```bash
   rsync -avz bruger@server:/sti/til/kilde/ /sti/til/destination/
   ```

## Tips
- Brug `-n` (dry run) muligheden for at se, hvad der ville blive gjort, uden faktisk at udføre overførslen.
- Overvej at bruge SSH til sikre overførsler ved at tilføje `-e ssh` til din kommando.
- Tjek altid destinationen efter en synkronisering for at sikre, at alt er overført korrekt.