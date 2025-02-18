# [Norsk] Debian Almquist Shell (dash) sftp bruk: Overfør filer sikkert

## Oversikt
`sftp` (SSH File Transfer Protocol) er en interaktiv filoverføringsprotokoll som gjør det mulig å overføre filer mellom en lokal og en ekstern vert på en sikker måte. Den bruker SSH for å gi en kryptert forbindelse, noe som gjør den tryggere enn tradisjonelle filoverføringsmetoder.

## Bruk
Grunnleggende syntaks for `sftp`-kommandoen er som følger:

```bash
sftp [alternativer] [brukernavn@vert]
```

## Vanlige alternativer
- `-o`: Angi spesifikke SSH-alternativer.
- `-P`: Angi portnummer for tilkoblingen.
- `-b`: Bruk en batch-fil for å kjøre flere kommandoer.
- `-r`: Overfør kataloger rekursivt.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `sftp`:

1. Koble til en ekstern vert:
   ```bash
   sftp bruker@ekstern-vert
   ```

2. Overføre en fil fra lokal til ekstern vert:
   ```bash
   sftp bruker@ekstern-vert:/sti/til/mål
   put lokal_fil.txt
   ```

3. Overføre en fil fra ekstern vert til lokal maskin:
   ```bash
   sftp bruker@ekstern-vert
   get ekstern_fil.txt
   ```

4. Overføre en katalog rekursivt:
   ```bash
   sftp -r bruker@ekstern-vert:/sti/til/mål
   put lokal_katalog
   ```

5. Bruke en batch-fil for å kjøre flere kommandoer:
   ```bash
   sftp -b batchfil.txt bruker@ekstern-vert
   ```

## Tips
- Sørg for at SSH-tjenesten kjører på den eksterne verten for å kunne bruke `sftp`.
- Bruk `-P` for å spesifisere en annen port hvis SSH-serveren kjører på en ikke-standard port.
- For å unngå å måtte skrive passord hver gang, vurder å bruke SSH-nøkkelautentisering.