# [Danish] Debian Almquist Shell (dash) umask brug: Indstiller standard tilladelser for nye filer

## Oversigt
`umask`-kommandoen bruges til at indstille standard tilladelser for nye filer og mapper, der oprettes i Unix-lignende systemer. Den bestemmer, hvilke tilladelser der skal fjernes fra de standard tilladelser, som filsystemet normalt tildeler.

## Brug
Den grundlæggende syntaks for `umask`-kommandoen er:

```bash
umask [muligheder] [argumenter]
```

## Almindelige muligheder
- `-S`: Viser umask-værdien i symbolsk form.
- `-p`: Viser den aktuelle umask-værdi i et format, der kan bruges i en shell.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `umask`:

1. **Vis den nuværende umask-værdi:**
   ```bash
   umask
   ```

2. **Indstil umask til 022 (fjerner skriveadgang for gruppe og andre):**
   ```bash
   umask 022
   ```

3. **Vis umask-værdien i symbolsk form:**
   ```bash
   umask -S
   ```

4. **Indstil umask til 007 (fjerner læse- og skriveadgang for gruppe og andre):**
   ```bash
   umask 007
   ```

## Tips
- Det er en god idé at kontrollere din umask-værdi, før du opretter nye filer, især hvis du arbejder med følsomme data.
- Husk, at umask-værdien kun påvirker nye filer og mapper; eksisterende filer påvirkes ikke.
- Du kan tilføje `umask`-kommandoen til din shell-startfil (f.eks. `.bashrc` eller `.profile`) for at sikre, at dine indstillinger anvendes ved hver login.