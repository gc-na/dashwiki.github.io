# [Danish] Debian Almquist Shell (dash) env brug: Håndtering af miljøvariabler

## Oversigt
`env`-kommandoen bruges til at vise eller ændre miljøvariabler i et shell-miljø. Den kan også anvendes til at køre et program med et ændret miljø.

## Brug
Den grundlæggende syntaks for `env`-kommandoen er:

```bash
env [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`: Start et nyt miljø uden eksisterende variabler.
- `-u VARIABEL`: Fjern en specifik miljøvariabel.
- `VARIABEL=værdi`: Sæt en ny miljøvariabel til en bestemt værdi.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `env`:

1. **Vis alle miljøvariabler**:
   ```bash
   env
   ```

2. **Kør et program med et ændret miljø**:
   ```bash
   env VARIABEL=værdi programnavn
   ```

3. **Fjern en miljøvariabel**:
   ```bash
   env -u VARIABEL programnavn
   ```

4. **Start et program uden eksisterende miljøvariabler**:
   ```bash
   env -i programnavn
   ```

## Tips
- Brug `env` til at teste, hvordan et program opfører sig under forskellige miljøforhold.
- Vær forsigtig med at fjerne miljøvariabler, da det kan påvirke, hvordan programmer kører.
- Du kan kombinere flere `VARIABEL=værdi` indstillinger i én `env`-kommando for at sætte flere variabler på én gang.