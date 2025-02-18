# [Deutsch] Debian Almquist Shell (dash) cd Verwendung: Wechselt das aktuelle Verzeichnis

## Übersicht
Der `cd`-Befehl (change directory) wird verwendet, um das aktuelle Arbeitsverzeichnis in der Debian Almquist Shell (dash) zu ändern. Mit diesem Befehl können Benutzer zu verschiedenen Verzeichnissen im Dateisystem navigieren.

## Verwendung
Die grundlegende Syntax des `cd`-Befehls lautet:

```bash
cd [Optionen] [Argumente]
```

## Häufige Optionen
- `-P`: Folgt symbolischen Links und zeigt das physische Verzeichnis an.
- `-L`: Folgt symbolischen Links, zeigt jedoch das logische Verzeichnis an (Standardverhalten).

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `cd`-Befehls:

1. **Wechseln zu einem bestimmten Verzeichnis:**
   ```bash
   cd /home/benutzername/Dokumente
   ```

2. **Wechseln zum übergeordneten Verzeichnis:**
   ```bash
   cd ..
   ```

3. **Wechseln zum Heimatverzeichnis des Benutzers:**
   ```bash
   cd ~
   ```

4. **Wechseln zu einem Verzeichnis mit symbolischem Link:**
   ```bash
   cd -P /pfad/zum/symbolischen/link
   ```

## Tipps
- Verwenden Sie `cd -`, um zum vorherigen Verzeichnis zurückzukehren.
- Nutzen Sie die Tab-Taste zur automatischen Vervollständigung von Verzeichnisnamen, um Tippfehler zu vermeiden.
- Um den aktuellen Pfad anzuzeigen, können Sie den Befehl `pwd` (print working directory) verwenden, nachdem Sie mit `cd` gewechselt haben.