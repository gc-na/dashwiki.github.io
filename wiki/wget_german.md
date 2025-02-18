# [Deutsch] Debian Almquist Shell (dash) wget Verwendung: Dateien aus dem Internet herunterladen

## Übersicht
Der `wget` Befehl ist ein leistungsstarkes Tool, das verwendet wird, um Dateien über das Internet herunterzuladen. Es unterstützt verschiedene Protokolle wie HTTP, HTTPS und FTP und kann sowohl einfache Downloads als auch komplexere Aufgaben wie das Herunterladen von ganzen Webseiten durchführen.

## Verwendung
Die grundlegende Syntax des `wget` Befehls lautet:

```bash
wget [Optionen] [Argumente]
```

## Häufige Optionen
Hier sind einige gängige Optionen für `wget`:

- `-O <Dateiname>`: Speichert die heruntergeladene Datei unter dem angegebenen Namen.
- `-c`: Setzt einen abgebrochenen Download fort.
- `-r`: Aktiviert den rekursiven Download, um ganze Verzeichnisse herunterzuladen.
- `-q`: Führt den Download im "stillen" Modus aus, ohne Ausgaben anzuzeigen.
- `--limit-rate=<Rate>`: Begrenzung der Downloadgeschwindigkeit auf die angegebene Rate.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung von `wget`:

1. **Einzelne Datei herunterladen:**
   ```bash
   wget https://example.com/datei.zip
   ```

2. **Datei unter einem bestimmten Namen speichern:**
   ```bash
   wget -O mein_download.zip https://example.com/datei.zip
   ```

3. **Download fortsetzen:**
   ```bash
   wget -c https://example.com/große_datei.zip
   ```

4. **Rekursiven Download eines gesamten Verzeichnisses:**
   ```bash
   wget -r https://example.com/verzeichnis/
   ```

5. **Download mit Geschwindigkeitsbegrenzung:**
   ```bash
   wget --limit-rate=100k https://example.com/datei.zip
   ```

## Tipps
- Verwenden Sie die Option `-q`, wenn Sie den Download im Hintergrund durchführen möchten, um die Konsole nicht zu überladen.
- Bei großen Downloads kann die Option `-c` nützlich sein, um sicherzustellen, dass Sie nicht von vorne beginnen müssen, falls der Download unterbrochen wird.
- Nutzen Sie die rekursive Download-Option mit Bedacht, um nicht versehentlich große Mengen an Daten herunterzuladen.