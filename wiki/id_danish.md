# [Danish] Debian Almquist Shell (dash) id brug: Vis bruger- og gruppeoplysninger

## Oversigt
`id`-kommandoen bruges til at vise brugerens UID (User ID), GID (Group ID) og de grupper, som brugeren tilhører. Det er en nyttig kommando til at få indsigt i brugerens identitet og rettigheder på systemet.

## Brug
Den grundlæggende syntaks for `id`-kommandoen er:

```
id [options] [arguments]
```

## Almindelige muligheder
- `-u`: Viser kun brugerens UID.
- `-g`: Viser kun brugerens GID.
- `-G`: Viser alle grupper, som brugeren tilhører.
- `-n`: Viser navnene i stedet for ID'erne, når det er muligt.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `id`-kommandoen:

1. Vis brugerens UID og GID:
   ```bash
   id
   ```

2. Vis kun brugerens UID:
   ```bash
   id -u
   ```

3. Vis kun brugerens GID:
   ```bash
   id -g
   ```

4. Vis alle grupper, som brugeren tilhører:
   ```bash
   id -G
   ```

5. Vis brugeroplysninger for en specifik bruger (f.eks. "username"):
   ```bash
   id username
   ```

6. Vis brugerens UID og GID med navne:
   ```bash
   id -n
   ```

## Tips
- Brug `id`-kommandoen i scripts for at kontrollere, om en bruger har de nødvendige rettigheder.
- Kombiner `id` med andre kommandoer som `grep` for at filtrere specifikke oplysninger.
- Tjek altid, hvilken bruger du er logget ind som, ved at køre `id` uden argumenter.