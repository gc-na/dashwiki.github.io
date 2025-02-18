# [Danish] Debian Almquist Shell (dash) ssh brug: Opretter sikre forbindelser til fjernmaskiner

## Oversigt
`ssh` (Secure Shell) er et netværksprotokol, der bruges til at oprette sikre forbindelser til en fjernmaskine. Det giver brugerne mulighed for at logge ind på en anden computer over et usikkert netværk og udføre kommandoer sikkert.

## Brug
Den grundlæggende syntaks for `ssh`-kommandoen er som følger:

```bash
ssh [muligheder] [bruger@]værtsnavn
```

## Almindelige muligheder
- `-p [port]`: Angiver en alternativ port til at oprette forbindelse (standard er 22).
- `-i [fil]`: Angiver en privat nøglefil til autentificering.
- `-v`: Aktiverer detaljeret output for fejlfinding.
- `-X`: Aktiverer X11 forwarding, så grafiske programmer kan køres over SSH.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `ssh`:

1. Opret forbindelse til en fjernmaskine med standardport:
   ```bash
   ssh bruger@eksempel.com
   ```

2. Opret forbindelse til en fjernmaskine på en alternativ port:
   ```bash
   ssh -p 2222 bruger@eksempel.com
   ```

3. Brug en specifik privat nøgle til autentificering:
   ```bash
   ssh -i ~/.ssh/id_rsa bruger@eksempel.com
   ```

4. Kør en kommando på den fjernmaskine:
   ```bash
   ssh bruger@eksempel.com 'ls -l /home/bruger'
   ```

5. Aktivér X11 forwarding:
   ```bash
   ssh -X bruger@eksempel.com
   ```

## Tips
- Sørg for at have din offentlige nøgle tilføjet til `~/.ssh/authorized_keys` på den fjernmaskine, du vil oprette forbindelse til, for at undgå at skulle indtaste din adgangskode hver gang.
- Brug `-v` muligheden for at få mere information, hvis du oplever problemer med at oprette forbindelse.
- Overvej at bruge en SSH-agent til at håndtere dine nøgler, så du ikke behøver at indtaste din adgangskode hver gang.