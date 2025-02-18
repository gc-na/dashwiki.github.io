# [Deutsch] Debian Almquist Shell (dash) netstat Verwendung: Netzwerkverbindungen anzeigen

## Übersicht
Der Befehl `netstat` wird verwendet, um Netzwerkverbindungen, Routing-Tabellen, Schnittstellenstatistiken und andere Netzwerkprotokollinformationen anzuzeigen. Er ist ein nützliches Werkzeug zur Überwachung und Fehlerbehebung von Netzwerkverbindungen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
netstat [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle Verbindungen und Listening-Ports an.
- `-t`: Zeigt nur TCP-Verbindungen an.
- `-u`: Zeigt nur UDP-Verbindungen an.
- `-n`: Zeigt IP-Adressen und Portnummern numerisch an, anstatt sie in Namen aufzulösen.
- `-l`: Zeigt nur die Listening-Ports an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `netstat`:

1. **Alle Verbindungen anzeigen:**
   ```bash
   netstat -a
   ```

2. **Nur aktive TCP-Verbindungen anzeigen:**
   ```bash
   netstat -t
   ```

3. **Nur aktive UDP-Verbindungen anzeigen:**
   ```bash
   netstat -u
   ```

4. **Listening-Ports anzeigen:**
   ```bash
   netstat -l
   ```

5. **Verbindungen mit numerischen Adressen anzeigen:**
   ```bash
   netstat -n
   ```

## Tipps
- Verwenden Sie die Option `-p`, um die PID und den Namen des Prozesses anzuzeigen, der die Verbindung hält.
- Kombinieren Sie Optionen, um spezifischere Informationen zu erhalten, z.B. `netstat -tunlp`, um alle aktiven Verbindungen mit Prozessinformationen anzuzeigen.
- Nutzen Sie `grep`, um die Ausgabe von `netstat` nach bestimmten Ports oder IP-Adressen zu filtern, z.B. `netstat -a | grep 80`.