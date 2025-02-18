# [Deutsch] Debian Almquist Shell (dash) top Verwendung: Systemüberwachung in Echtzeit

## Übersicht
Der Befehl `top` zeigt eine dynamische, Echtzeit-Ansicht der Prozesse, die auf einem Unix-ähnlichen Betriebssystem laufen. Er ermöglicht es Benutzern, die Systemauslastung und die Ressourcennutzung zu überwachen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
top [Optionen]
```

## Häufige Optionen
- `-d <Sekunden>`: Legt das Intervall in Sekunden fest, in dem die Anzeige aktualisiert wird.
- `-n <Anzahl>`: Gibt die Anzahl der Aktualisierungen an, bevor `top` beendet wird.
- `-u <Benutzer>`: Zeigt nur die Prozesse eines bestimmten Benutzers an.
- `-p <PID>`: Überwacht nur den Prozess mit der angegebenen Prozess-ID.

## Häufige Beispiele
Um die Prozesse in Echtzeit anzuzeigen, verwenden Sie einfach:

```bash
top
```

Um die Aktualisierungsrate auf 2 Sekunden zu setzen, verwenden Sie:

```bash
top -d 2
```

Um nur die Prozesse eines bestimmten Benutzers, z.B. `max`, anzuzeigen:

```bash
top -u max
```

Um nur einen spezifischen Prozess mit der PID 1234 zu überwachen:

```bash
top -p 1234
```

## Tipps
- Drücken Sie `h`, um die Hilfe innerhalb von `top` aufzurufen und mehr über die verfügbaren Funktionen zu erfahren.
- Nutzen Sie die Tasten `Shift + M`, um die Prozesse nach Speicherverbrauch zu sortieren.
- Um `top` zu beenden, drücken Sie `q`.