# [Deutsch] Debian Almquist Shell (dash) hostname Verwendung: Zeigt oder ändert den Hostnamen des Systems

## Übersicht
Der Befehl `hostname` wird verwendet, um den aktuellen Hostnamen des Systems anzuzeigen oder ihn zu ändern. Der Hostname ist der Name, der einem Computer in einem Netzwerk zugewiesen ist und dient zur Identifizierung des Systems.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
hostname [Optionen] [Argumente]
```

## Häufige Optionen
- `-f`, `--fqdn`: Zeigt den vollqualifizierten Domainnamen (FQDN) des Systems an.
- `-i`, `--ip-address`: Gibt die IP-Adresse des Hostnamens zurück.
- `-s`, `--short`: Zeigt nur den kurzen Hostnamen an.
- `--help`: Zeigt eine Hilfeseite mit verfügbaren Optionen an.
- `--version`: Gibt die Versionsnummer des Befehls aus.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `hostname`:

1. **Aktuellen Hostnamen anzeigen:**
   ```bash
   hostname
   ```

2. **Vollqualifizierten Domainnamen anzeigen:**
   ```bash
   hostname -f
   ```

3. **Kurzen Hostnamen anzeigen:**
   ```bash
   hostname -s
   ```

4. **IP-Adresse des Hostnamens anzeigen:**
   ```bash
   hostname -i
   ```

5. **Hostnamen ändern:**
   Um den Hostnamen temporär zu ändern, können Sie den Befehl wie folgt verwenden:
   ```bash
   hostname neuer-hostname
   ```

## Tipps
- Um sicherzustellen, dass der neue Hostname nach einem Neustart beibehalten wird, sollten Sie die Datei `/etc/hostname` bearbeiten und den gewünschten Hostnamen dort eintragen.
- Verwenden Sie den Befehl `hostnamectl`, wenn Sie auf Systemen mit systemd arbeiten, um den Hostnamen dauerhaft zu ändern.
- Überprüfen Sie nach der Änderung des Hostnamens, ob die Änderung erfolgreich war, indem Sie den Befehl `hostname` erneut ausführen.