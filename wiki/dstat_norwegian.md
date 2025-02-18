# [Norsk] Debian Almquist Shell (dash) dstat bruk: overvåke systemytelse

## Oversikt
`dstat` er et kraftig verktøy for overvåking av systemytelse i sanntid. Det gir en omfattende oversikt over systemressurser som CPU, minne, disk og nettverksbruk, noe som gjør det til et nyttig verktøy for systemadministratorer og utviklere.

## Bruk
Grunnleggende syntaks for `dstat` er som følger:

```bash
dstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Vis CPU-bruk.
- `-d`: Vis diskaktivitet.
- `-n`: Vis nettverksaktivitet.
- `-m`: Vis minnebruk.
- `--time`: Vis tidsstempel for hver rad med data.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `dstat`:

1. **Vis CPU- og minnebruk:**
   ```bash
   dstat -c -m
   ```

2. **Vis disk- og nettverksaktivitet:**
   ```bash
   dstat -d -n
   ```

3. **Vis alle ressurser med tidsstempel:**
   ```bash
   dstat --time -cdmn
   ```

4. **Lagre utdata til en fil:**
   ```bash
   dstat -cdmn > dstat_output.txt
   ```

## Tips
- Bruk `dstat` sammen med andre verktøy som `grep` for å filtrere spesifikke data.
- Kjør `dstat` i en terminal som støtter fargede utdata for bedre lesbarhet.
- Vurder å bruke `dstat` med `--full` for å få mer detaljerte rapporter om systemytelsen.