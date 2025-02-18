# [Dansk] Debian Almquist Shell (dash) bg: [sætte job i baggrunden]

## Oversigt
`bg`-kommandoen bruges til at fortsætte et job, der er blevet sat på pause (suspenderet), i baggrunden. Dette gør det muligt for brugeren at køre flere processer samtidigt uden at blokere terminalen.

## Brug
Den grundlæggende syntaks for `bg`-kommandoen er:

```bash
bg [options] [arguments]
```

## Almindelige muligheder
- **%job_id**: Angiver det specifikke job, der skal sendes til baggrunden. Job-ID'et kan findes ved at bruge `jobs`-kommandoen.
- **-n**: Kører jobbet i baggrunden uden at sende output til terminalen.

## Almindelige eksempler

1. **Sætte et job i baggrunden**
   Hvis du har et job, der er blevet sat på pause (f.eks. ved at trykke `Ctrl+Z`), kan du sende det til baggrunden med:

   ```bash
   bg %1
   ```

   Her antager vi, at jobbet har ID 1.

2. **Sætte det seneste job i baggrunden**
   Du kan også sende det seneste job til baggrunden uden at angive job-ID:

   ```bash
   bg
   ```

3. **Køre et job i baggrunden fra starten**
   Du kan starte et job direkte i baggrunden ved at tilføje `&` i slutningen af kommandoen:

   ```bash
   long_running_command &
   ```

## Tips
- Brug `jobs`-kommandoen for at se en liste over alle aktive jobs og deres status.
- Husk at du kan bringe et job tilbage til forgrunden ved at bruge `fg %job_id`.
- Vær opmærksom på, at output fra baggrundsjob kan oversvømme terminalen, så overvej at bruge `nohup` eller omdirigere output til en fil, hvis det er nødvendigt.