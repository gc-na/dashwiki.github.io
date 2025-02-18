# [Svenska] Debian Almquist Shell (dash) scp användning: Överför filer säkert mellan värdar

## Översikt
`scp` (Secure Copy Protocol) är ett kommandoradsverktyg som används för att överföra filer mellan en lokal och en fjärrdator eller mellan två fjärrdatorer. Det använder SSH-protokollet för att säkerställa att överföringen är säker.

## Användning
Den grundläggande syntaxen för `scp` ser ut så här:

```bash
scp [alternativ] [källfil] [mål]
```

## Vanliga alternativ
- `-r`: Kopiera kataloger rekursivt.
- `-P port`: Specifiera en port om SSH-servern använder en annan port än standardporten (22).
- `-i fil`: Använd en specifik privat nyckel för autentisering.
- `-v`: Aktivera detaljerad utdata för felsökning.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `scp`:

1. **Kopiera en fil från lokal dator till en fjärrdator:**
   ```bash
   scp /lokal/sökväg/till/fil.txt användare@fjärrdator:/fjärr/sökväg/
   ```

2. **Kopiera en fil från en fjärrdator till lokal dator:**
   ```bash
   scp användare@fjärrdator:/fjärr/sökväg/fil.txt /lokal/sökväg/
   ```

3. **Kopiera en katalog rekursivt till en fjärrdator:**
   ```bash
   scp -r /lokal/sökväg/till/katalog användare@fjärrdator:/fjärr/sökväg/
   ```

4. **Kopiera en fil mellan två fjärrdatorer:**
   ```bash
   scp användare1@fjärrdator1:/fjärr/sökväg/fil.txt användare2@fjärrdator2:/fjärr/sökväg/
   ```

## Tips
- Kontrollera alltid att du har rätt behörigheter på både lokal och fjärrdator för att undvika problem vid överföring.
- Använd `-v` alternativet för att få mer information om vad som händer under överföringen, vilket kan hjälpa vid felsökning.
- Tänk på att använda SSH-nycklar för autentisering istället för lösenord för att öka säkerheten och förenkla processen.