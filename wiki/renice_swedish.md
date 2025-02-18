# [Svenska] Debian Almquist Shell (dash) renice användning: Ändra prioritet för processer

## Översikt
Kommandot `renice` används för att ändra prioriteten på en eller flera processer som körs på systemet. Genom att justera prioriteten kan användare optimera systemets prestanda och resurser, vilket är särskilt användbart när vissa processer behöver mer eller mindre CPU-tid.

## Användning
Den grundläggande syntaxen för `renice` är:

```bash
renice [alternativ] [argument]
```

## Vanliga alternativ
- `-n, --priority <värde>`: Ange den nya prioriteten (ett heltal mellan -20 och 19, där -20 är högsta prioritet).
- `-p, --pid <pid>`: Specifika process-ID:n för de processer vars prioritet ska ändras.
- `-g, --pgrp <pgrp>`: Ändra prioriteten för alla processer i en specifik processgrupp.
- `-u, --user <användare>`: Ändra prioriteten för alla processer som körs av en specifik användare.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `renice`:

1. Ändra prioriteten för en specifik process med PID 1234 till 10:
   ```bash
   renice -n 10 -p 1234
   ```

2. Ändra prioriteten för alla processer som tillhör användaren "user1" till 5:
   ```bash
   renice -n 5 -u user1
   ```

3. Ändra prioriteten för en processgrupp med grupp-ID 5678 till -5:
   ```bash
   renice -n -5 -g 5678
   ```

4. Kontrollera nuvarande prioritet för en process med PID 1234:
   ```bash
   ps -o pid,ni,cmd -p 1234
   ```

## Tips
- Använd `renice` med försiktighet, eftersom att ge en process högre prioritet kan påverka systemets stabilitet och prestanda.
- Kontrollera alltid nuvarande prioritet för en process innan du gör ändringar för att undvika oönskade effekter.
- För att se alla processer som körs av en specifik användare kan du använda kommandot `ps -u <användare>`.