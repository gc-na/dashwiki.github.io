# [Svenska] Debian Almquist Shell (dash) pidstat användning: Övervaka processstatistik

## Översikt
Kommandot `pidstat` används för att övervaka och rapportera statistik om processer i ett Linux-system. Det ger detaljerad information om CPU-användning, minnesanvändning och andra resurser som används av specifika processer.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
pidstat [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Visar hjälpmeddelande med tillgängliga alternativ.
- `-r`: Visar minnesanvändning för processer.
- `-u`: Visar CPU-användning för processer.
- `-p`: Anger specifika process-ID:n att övervaka.
- `-t`: Visar statistik för trådar i stället för processer.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `pidstat`:

1. Visa CPU-användning för alla processer:
   ```bash
   pidstat -u
   ```

2. Visa minnesanvändning för alla processer:
   ```bash
   pidstat -r
   ```

3. Övervaka en specifik process med process-ID 1234:
   ```bash
   pidstat -p 1234
   ```

4. Visa statistik för alla trådar i en process med process-ID 5678:
   ```bash
   pidstat -t -p 5678
   ```

5. Visa CPU-användning var 2:a sekund:
   ```bash
   pidstat -u 2
   ```

## Tips
- Använd `pidstat` tillsammans med andra kommandon som `grep` för att filtrera specifika processer.
- Kombinera alternativ för att få en mer detaljerad översikt, till exempel `pidstat -u -r`.
- Använd `man pidstat` för att få mer information och en fullständig lista över alternativ.