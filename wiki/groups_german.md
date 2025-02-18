# [Deutsch] Debian Almquist Shell (dash) groups Verwendung: Gruppenmitgliedschaften anzeigen

## Übersicht
Der Befehl `groups` zeigt die Gruppen an, zu denen ein Benutzer gehört. Dies ist nützlich, um schnell zu überprüfen, welche Berechtigungen und Zugriffsrechte einem Benutzer zugewiesen sind.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
groups [optionen] [benutzer]
```

## Häufige Optionen
- `--help`: Zeigt eine Hilfemeldung mit Informationen zur Verwendung des Befehls an.
- `--version`: Gibt die Versionsnummer des Befehls aus.

## Häufige Beispiele
Um die Gruppenmitgliedschaften des aktuellen Benutzers anzuzeigen, verwenden Sie:

```bash
groups
```

Um die Gruppenmitgliedschaften eines bestimmten Benutzers anzuzeigen, geben Sie den Benutzernamen an:

```bash
groups benutzername
```

Wenn Sie die Gruppen für mehrere Benutzer gleichzeitig abfragen möchten, können Sie dies ebenfalls tun:

```bash
groups benutzer1 benutzer2
```

## Tipps
- Verwenden Sie den Befehl ohne Argumente, um schnell Ihre eigenen Gruppenmitgliedschaften zu überprüfen.
- Nutzen Sie die Option `--help`, wenn Sie sich nicht sicher sind, wie der Befehl verwendet wird oder welche Optionen verfügbar sind.
- Denken Sie daran, dass die Gruppenmitgliedschaften eines Benutzers auch die Berechtigungen für den Zugriff auf Dateien und Verzeichnisse beeinflussen können.