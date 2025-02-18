# [Svenska] Debian Almquist Shell (dash) dig användning: Hämta DNS-information

## Översikt
Kommandot `dig` (Domain Information Groper) används för att hämta DNS-information om domäner. Det är ett kraftfullt verktyg för att diagnostisera DNS-problem och få detaljerad information om DNS-poster.

## Användning
Den grundläggande syntaxen för kommandot `dig` är:

```bash
dig [alternativ] [argument]
```

## Vanliga alternativ
- `@server`: Anger en specifik DNS-server att fråga.
- `-t typ`: Anger typen av DNS-post att hämta (t.ex. A, MX, TXT).
- `+short`: Visar en kortare och mer sammanfattad utdata.
- `+trace`: Spårar hela vägen från rot-DNS-servrar till den specifika domänen.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `dig`:

1. Hämta A-poster för en domän:
   ```bash
   dig example.com A
   ```

2. Hämta MX-poster för en domän:
   ```bash
   dig example.com MX
   ```

3. Använda en specifik DNS-server:
   ```bash
   dig @8.8.8.8 example.com
   ```

4. Visa en kort version av A-poster:
   ```bash
   dig example.com A +short
   ```

5. Spåra DNS-resolution:
   ```bash
   dig example.com +trace
   ```

## Tips
- Använd `+short` för att få en mer överskådlig utdata, särskilt när du bara behöver IP-adresser.
- Testa olika DNS-servrar för att jämföra svarstider och resultat.
- Använd `-t ANY` för att hämta alla typer av poster för en domän, men var medveten om att vissa servrar kan begränsa detta.