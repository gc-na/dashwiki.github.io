# [Deutsch] Debian Almquist Shell (dash) ss Verwendung: Netzwerkverbindungen anzeigen

## Übersicht
Der Befehl `ss` wird verwendet, um Informationen über Netzwerkverbindungen auf einem Linux-System anzuzeigen. Er ist ein leistungsfähiges Werkzeug zur Überwachung und Analyse von Netzwerkverbindungen und -sockets.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
ss [Optionen] [Argumente]
```

## Häufige Optionen
- `-t`: Zeigt nur TCP-Verbindungen an.
- `-u`: Zeigt nur UDP-Verbindungen an.
- `-l`: Listet nur die Verbindungen auf, die auf eingehende Verbindungen warten.
- `-p`: Zeigt die zugehörigen Prozesse für die Verbindungen an.
- `-n`: Verwendet numerische Adressen anstelle von Namen.

## Häufige Beispiele
Hier sind einige praktische Beispiele zur Verwendung des `ss`-Befehls:

1. **Alle aktiven Verbindungen anzeigen:**
   ```bash
   ss
   ```

2. **Nur TCP-Verbindungen anzeigen:**
   ```bash
   ss -t
   ```

3. **Nur UDP-Verbindungen anzeigen:**
   ```bash
   ss -u
   ```

4. **Liste der wartenden Verbindungen anzeigen:**
   ```bash
   ss -l
   ```

5. **Verbindungen mit zugehörigen Prozessen anzeigen:**
   ```bash
   ss -p
   ```

6. **Numerische Adressen verwenden:**
   ```bash
   ss -n
   ```

## Tipps
- Verwenden Sie die Option `-n`, um die Ausgabe zu beschleunigen, da DNS-Abfragen vermieden werden.
- Kombinieren Sie Optionen, um spezifischere Informationen zu erhalten, z.B. `ss -tunlp`, um alle TCP- und UDP-Verbindungen mit Prozessen anzuzeigen.
- Nutzen Sie `man ss`, um die vollständige Dokumentation und alle verfügbaren Optionen zu lesen.