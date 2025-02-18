# [Danish] Debian Almquist Shell (dash) du: [vis størrelsen af filer og mapper]

## Oversigt
`du` (disk usage) er et kommandolinjeværktøj, der bruges til at vise størrelsen af filer og mapper i et filsystem. Det giver brugerne mulighed for at se, hvor meget diskplads der bruges af specifikke filer og mapper, hvilket kan være nyttigt til at identificere pladskrævende elementer.

## Brug
Den grundlæggende syntaks for `du`-kommandoen er som følger:

```bash
du [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h`: Viser størrelser i et menneskeligt læsbart format (f.eks. KB, MB).
- `-s`: Viser kun den samlede størrelse for hver angivet mappe.
- `-a`: Viser størrelsen for både filer og mapper.
- `-c`: Tilføjer en total til slutningen af outputtet.
- `--max-depth=N`: Begrænser outputtet til N niveauer af undermapper.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `du` kan bruges:

1. Vis størrelsen af den aktuelle mappe og dens undermapper:
   ```bash
   du -h
   ```

2. Vis den samlede størrelse af en specifik mappe:
   ```bash
   du -sh /sti/til/mappe
   ```

3. Vis størrelsen af alle filer og mapper i den aktuelle mappe:
   ```bash
   du -ah
   ```

4. Vis størrelsen af mapper op til et bestemt niveau:
   ```bash
   du --max-depth=1 -h
   ```

5. Vis størrelsen af mapper og tilføj en total:
   ```bash
   du -ch
   ```

## Tips
- Brug `-h` muligheden for at gøre output mere læsbart, især når du arbejder med store mængder data.
- Kombiner `du` med `sort` for at finde de største mapper:
  ```bash
  du -h | sort -hr
  ```
- Overvej at bruge `-s` for at få et hurtigt overblik over størrelsen af specifikke mapper uden at se på hver enkelt undermappe.