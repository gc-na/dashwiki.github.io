# [Svenska] Debian Almquist Shell (dash) ps användning: [visa processinformation]

## Översikt
Kommandot `ps` används för att visa information om aktiva processer i systemet. Det ger en översikt över vilka program som körs, deras process-ID:n (PID), och annan relevant information som minnesanvändning och CPU-användning.

## Användning
Den grundläggande syntaxen för kommandot är:

```
ps [alternativ] [argument]
```

## Vanliga alternativ
- `-e`: Visa alla processer.
- `-f`: Visa fullständig formatinformation.
- `-u [användare]`: Visa processer för en specifik användare.
- `-aux`: Visa alla processer med detaljerad information.
- `--sort [kolumn]`: Sortera utdata baserat på en specifik kolumn.

## Vanliga exempel
Visa alla processer som körs:

```bash
ps -e
```

Visa processer med fullständig information:

```bash
ps -f
```

Visa processer för en specifik användare:

```bash
ps -u användarnamn
```

Visa alla processer med detaljerad information:

```bash
ps aux
```

Sortera processerna efter minnesanvändning:

```bash
ps aux --sort=-%mem
```

## Tips
- Använd `ps aux` för att få en omfattande översikt över alla processer, inklusive de som körs av andra användare.
- Kombinera `ps` med andra kommandon som `grep` för att filtrera resultaten. Till exempel:

```bash
ps aux | grep programnamn
```

- Tänk på att `ps` visar en ögonblicksbild av processerna vid tidpunkten för kommandots körning. Använd `top` för en dynamisk visning av processerna.