# [Deutsch] Debian Almquist Shell (dash) export Verwendung: Umgebungsvariablen festlegen

## Übersicht
Der Befehl `export` wird in der Debian Almquist Shell (dash) verwendet, um Umgebungsvariablen zu erstellen oder zu ändern. Durch das Exportieren einer Variablen wird sie für alle nachfolgenden Prozesse verfügbar, die aus der aktuellen Shell gestartet werden.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
export [Optionen] [Argumente]
```

## Häufige Optionen
- `-n`: Deaktiviert das Exportieren einer Variablen.
- `-p`: Listet alle exportierten Variablen auf.

## Häufige Beispiele

1. **Eine neue Umgebungsvariable erstellen und exportieren:**
   ```sh
   export MEINE_VAR="Hallo Welt"
   ```

2. **Eine bestehende Umgebungsvariable ändern:**
   ```sh
   export MEINE_VAR="Neue Werte"
   ```

3. **Eine Umgebungsvariable ohne Export erstellen:**
   ```sh
   MEINE_VAR="Nur lokal"
   ```

4. **Exportieren einer Variablen und gleichzeitiges Ausführen eines Befehls:**
   ```sh
   export MEINE_VAR="Wert" && echo $MEINE_VAR
   ```

5. **Alle exportierten Variablen auflisten:**
   ```sh
   export -p
   ```

## Tipps
- Verwenden Sie `export` immer, wenn Sie sicherstellen möchten, dass eine Variable in untergeordneten Prozessen verfügbar ist.
- Um eine Variable zu löschen, verwenden Sie `unset` anstelle von `export`.
- Es ist eine gute Praxis, Umgebungsvariablen in Großbuchstaben zu benennen, um sie von regulären Variablen zu unterscheiden.