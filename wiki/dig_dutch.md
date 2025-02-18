# [Nederlands] Debian Almquist Shell (dash) dig gebruik: DNS-query's uitvoeren

## Overzicht
Het `dig`-commando, wat staat voor "Domain Information Groper", is een netwerkhulpmiddel dat wordt gebruikt om DNS-informatie op te vragen. Het stelt gebruikers in staat om de naamservers te raadplegen en gedetailleerde informatie over domeinen te verkrijgen, zoals IP-adressen en andere DNS-records.

## Gebruik
De basis syntaxis van het `dig`-commando is als volgt:

```bash
dig [opties] [argumenten]
```

## Veelvoorkomende Opties
- `@server`: Specificeert een andere DNS-server om de query naar te sturen.
- `-t type`: Bepaalt het type DNS-record dat je wilt opvragen (bijvoorbeeld A, MX, TXT).
- `+short`: Geeft een verkorte weergave van de resultaten.
- `+trace`: Volgt de route van de DNS-query vanaf de rootservers.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `dig`:

1. **Basis DNS-query voor een A-record:**
   ```bash
   dig example.com
   ```

2. **Opvragen van een specifiek type record (bijvoorbeeld MX-records):**
   ```bash
   dig -t MX example.com
   ```

3. **Gebruik maken van een specifieke DNS-server:**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Verkorte weergave van het A-record:**
   ```bash
   dig +short example.com
   ```

5. **Volgen van de DNS-query-route:**
   ```bash
   dig +trace example.com
   ```

## Tips
- Gebruik de `+short` optie voor een snellere en eenvoudigere weergave van de resultaten, vooral als je alleen het IP-adres nodig hebt.
- Experimenteer met verschillende recordtypes om meer inzicht te krijgen in de DNS-configuratie van een domein.
- Houd er rekening mee dat sommige DNS-servers mogelijk niet alle recordtypes ondersteunen, dus het kan nuttig zijn om verschillende servers te proberen.