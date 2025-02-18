# [Deutsch] Debian Almquist Shell (dash) uname Verwendung: Systeminformationen anzeigen

## Übersicht
Der Befehl `uname` wird verwendet, um Informationen über das aktuelle System anzuzeigen. Er liefert grundlegende Details wie den Namen des Betriebssystems, den Kernel und die Architektur.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
uname [Optionen] [Argumente]
```

## Häufige Optionen
- `-a`: Zeigt alle verfügbaren Informationen über das System an.
- `-s`: Gibt den Namen des Betriebssystems aus.
- `-n`: Zeigt den Netzwerk-Hostnamen des Systems an.
- `-r`: Gibt die Kernel-Version aus.
- `-m`: Zeigt die Maschinenarchitektur an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `uname`-Befehls:

1. **Alle Informationen anzeigen:**
   ```bash
   uname -a
   ```

2. **Nur den Namen des Betriebssystems anzeigen:**
   ```bash
   uname -s
   ```

3. **Kernel-Version anzeigen:**
   ```bash
   uname -r
   ```

4. **Architektur des Systems anzeigen:**
   ```bash
   uname -m
   ```

5. **Netzwerk-Hostnamen anzeigen:**
   ```bash
   uname -n
   ```

## Tipps
- Verwenden Sie die Option `-a`, um eine umfassende Übersicht über Ihr System zu erhalten.
- Kombinieren Sie `uname` mit anderen Befehlen wie `grep`, um spezifische Informationen herauszufiltern.
- Nutzen Sie `man uname`, um die vollständige Dokumentation und weitere Optionen zu lesen.