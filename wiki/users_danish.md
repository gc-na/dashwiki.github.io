# [Danish] Debian Almquist Shell (dash) brugere: Vis brugerkonti

## Oversigt
`users`-kommandoen viser en liste over brugernavne, der i øjeblikket er logget ind på systemet. Det er en nyttig kommando til hurtigt at få indsigt i, hvilke brugere der er aktive.

## Brug
Den grundlæggende syntaks for `users`-kommandoen er:

```bash
users [options]
```

## Almindelige muligheder
`users`-kommandoen har ikke mange muligheder, men her er nogle, der kan være nyttige:

- `-n` : Viser kun brugernavne uden duplikater.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `users`-kommandoen:

1. For at vise alle brugere, der er logget ind på systemet:
   ```bash
   users
   ```

2. For at vise brugernavne uden duplikater:
   ```bash
   users -n
   ```

## Tips
- Brug `users` i kombination med andre kommandoer som `who` eller `w` for at få mere detaljerede oplysninger om de aktive brugere.
- Hvis du vil have en mere struktureret visning, kan du overveje at bruge `who`-kommandoen, som giver flere oplysninger om hver bruger.