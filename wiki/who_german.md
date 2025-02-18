# [Deutsch] Debian Almquist Shell (dash) who: Zeigt angemeldete Benutzer an

## Übersicht
Der Befehl `who` zeigt eine Liste der aktuell angemeldeten Benutzer auf dem System an. Er liefert Informationen wie den Benutzernamen, das Terminal, die Anmeldezeit und die Herkunft des Benutzers.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
who [Optionen] [Argumente]
```

## Häufige Optionen
- `-b`: Zeigt die letzte Systemstartzeit an.
- `-q`: Gibt nur die Benutzernamen und die Anzahl der angemeldeten Benutzer aus.
- `-H`: Fügt eine Kopfzeile zu den Ausgaben hinzu, die die Spaltenüberschriften beschreibt.

## Häufige Beispiele
Um die aktuell angemeldeten Benutzer anzuzeigen, verwenden Sie einfach:

```bash
who
```

Um die letzte Systemstartzeit anzuzeigen, verwenden Sie die Option `-b`:

```bash
who -b
```

Um nur die Benutzernamen und die Anzahl der angemeldeten Benutzer zu sehen, verwenden Sie die Option `-q`:

```bash
who -q
```

Wenn Sie eine Kopfzeile zu den Ausgaben hinzufügen möchten, verwenden Sie die Option `-H`:

```bash
who -H
```

## Tipps
- Verwenden Sie `who` regelmäßig, um einen Überblick über die aktiven Benutzer auf Ihrem System zu erhalten.
- Kombinieren Sie `who` mit anderen Befehlen wie `grep`, um spezifische Benutzer zu finden.
- Nutzen Sie die Optionen, um die Ausgabe nach Ihren Bedürfnissen anzupassen und nur die benötigten Informationen anzuzeigen.