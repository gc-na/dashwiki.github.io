# [Deutsch] Debian Almquist Shell (dash) Benutzerbefehl: Zeigt Informationen über Benutzer an

## Übersicht
Der Befehl `users` zeigt die aktuell angemeldeten Benutzer im System an. Er gibt eine einfache Liste der Benutzernamen zurück, die zurzeit aktiv sind.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
users [Optionen]
```

## Häufige Optionen
Der Befehl `users` hat keine speziellen Optionen. Er wird in der Regel ohne zusätzliche Parameter verwendet.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des Befehls `users`:

1. **Aktuell angemeldete Benutzer anzeigen:**
   ```bash
   users
   ```

2. **In einem Skript verwenden:**
   Um die Liste der Benutzer in einer Variablen zu speichern, können Sie Folgendes tun:
   ```bash
   angemeldete_benutzer=$(users)
   echo "Aktuell angemeldete Benutzer: $angemeldete_benutzer"
   ```

3. **Benutzer in einer Schleife durchlaufen:**
   Um jeden Benutzer einzeln zu verarbeiten, können Sie eine Schleife verwenden:
   ```bash
   for benutzer in $(users); do
       echo "Benutzer: $benutzer"
   done
   ```

## Tipps
- Verwenden Sie den Befehl `who`, um detailliertere Informationen über die angemeldeten Benutzer zu erhalten, einschließlich Anmeldezeiten und Terminal-Informationen.
- Der Befehl `users` ist nützlich in Skripten, um schnell zu überprüfen, ob Benutzer im System aktiv sind.
- Kombinieren Sie `users` mit anderen Befehlen wie `wc -w`, um die Anzahl der angemeldeten Benutzer zu zählen:
  ```bash
  anzahl_benutzer=$(users | wc -w)
  echo "Anzahl der angemeldeten Benutzer: $anzahl_benutzer"
  ```