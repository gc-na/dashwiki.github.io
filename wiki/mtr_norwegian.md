# [Norsk] Debian Almquist Shell (dash) mtr bruk: Verktøy for nettverksdiagnostikk

## Oversikt
`mtr` (My Traceroute) er et nettverksdiagnostikkverktøy som kombinerer funksjonaliteten til `ping` og `traceroute`. Det gir en dynamisk visning av ruten som datapakker tar fra en vert til en annen, samt informasjon om nettverksytelsen på hvert hopp.

## Bruk
Grunnleggende syntaks for `mtr`-kommandoen er:

```bash
mtr [alternativer] [mål]
```

## Vanlige alternativer
- `-r`: Kjør i rapportmodus og skriv ut resultatene i et format som kan brukes i skript.
- `-c <antall>`: Angi antall pinger som skal sendes før programmet avsluttes.
- `-i <intervall>`: Angi tidsintervallet mellom pinger i sekunder.
- `-p`: Kjør i "ping"-modus, som bare viser ping-resultater.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `mtr`:

1. Kjør `mtr` mot en spesifikk vert (f.eks. google.com):

    ```bash
    mtr google.com
    ```

2. Kjør `mtr` i rapportmodus og begrens til 10 pinger:

    ```bash
    mtr -r -c 10 google.com
    ```

3. Kjør `mtr` med et spesifisert intervall på 2 sekunder:

    ```bash
    mtr -i 2 google.com
    ```

4. Kjør `mtr` i ping-modus:

    ```bash
    mtr -p google.com
    ```

## Tips
- Bruk `mtr` med `sudo` for å få mer detaljerte resultater, spesielt for nettverksruter som krever administratorrettigheter.
- Kombiner `mtr` med andre verktøy som `grep` for å filtrere ut spesifikke resultater.
- Lagre `mtr`-utdataene til en fil for senere analyse ved å bruke omdirigering:

    ```bash
    mtr google.com > mtr_output.txt
    ```