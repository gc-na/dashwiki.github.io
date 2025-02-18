# [Deutsch] Debian Almquist Shell (dash) traceroute6 Verwendung: Netzwerkpfade verfolgen

## Übersicht
Der Befehl `traceroute6` wird verwendet, um den Pfad zu verfolgen, den Pakete über ein IPv6-Netzwerk zu einem bestimmten Ziel nehmen. Er zeigt die verschiedenen Router (Hops), die die Daten durchlaufen, sowie die Zeit, die benötigt wird, um jeden Hop zu erreichen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
traceroute6 [Optionen] [Ziel]
```

## Häufige Optionen
- `-m <max_hops>`: Legt die maximale Anzahl der Hops fest, die verfolgt werden sollen.
- `-w <timeout>`: Setzt die Wartezeit für jede Antwort in Sekunden.
- `-q <Anzahl>`: Bestimmt die Anzahl der Anfragen, die pro Hop gesendet werden.
- `-n`: Verwendet IP-Adressen anstelle von Hostnamen.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `traceroute6`:

1. **Einfaches Traceroute zu einer IPv6-Adresse:**
   ```bash
   traceroute6 2001:db8::1
   ```

2. **Traceroute mit maximal 10 Hops:**
   ```bash
   traceroute6 -m 10 2001:db8::1
   ```

3. **Traceroute mit einer spezifischen Wartezeit von 2 Sekunden:**
   ```bash
   traceroute6 -w 2 2001:db8::1
   ```

4. **Traceroute ohne Auflösung der Hostnamen:**
   ```bash
   traceroute6 -n 2001:db8::1
   ```

## Tipps
- Verwenden Sie die Option `-n`, um die Ausführung zu beschleunigen, da die DNS-Auflösung umgangen wird.
- Experimentieren Sie mit der Anzahl der Anfragen pro Hop (`-q`), um genauere Ergebnisse zu erhalten.
- Achten Sie darauf, dass einige Netzwerke ICMP-Pakete blockieren können, was die Ergebnisse von `traceroute6` beeinflussen kann.