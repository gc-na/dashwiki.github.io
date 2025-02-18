# [Deutsch] Debian Almquist Shell (dash) exit Verwendung: Beenden eines Shell-Skripts

## Übersicht
Der Befehl `exit` wird in der Debian Almquist Shell (dash) verwendet, um ein Shell-Skript oder eine Shell-Sitzung zu beenden. Er kann auch einen Statuscode zurückgeben, der den Erfolg oder Misserfolg des Skripts anzeigt.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```
exit [options] [status]
```

## Häufige Optionen
- `status`: Ein optionaler Statuscode, der anzeigt, wie das Skript beendet wurde. Ein Wert von `0` steht für einen erfolgreichen Abschluss, während jeder andere Wert auf einen Fehler hinweist.

## Häufige Beispiele

1. **Ein einfaches Skript beenden:**
   ```sh
   #!/bin/dash
   echo "Das Skript wird jetzt beendet."
   exit
   ```

2. **Mit einem Statuscode beenden:**
   ```sh
   #!/bin/dash
   if [ -f "datei.txt" ]; then
       echo "Datei gefunden."
       exit 0
   else
       echo "Datei nicht gefunden."
       exit 1
   fi
   ```

3. **Beenden einer interaktiven Shell-Sitzung:**
   ```sh
   exit
   ```

## Tipps
- Verwenden Sie den Statuscode `0`, um anzuzeigen, dass Ihr Skript erfolgreich ausgeführt wurde. Dies ist besonders nützlich, wenn Ihr Skript von anderen Skripten oder Programmen aufgerufen wird.
- Dokumentieren Sie die möglichen Statuscodes in Ihren Skripten, um die Fehlersuche zu erleichtern.
- Vermeiden Sie es, `exit` ohne einen Statuscode in komplexen Skripten zu verwenden, da dies zu Verwirrung führen kann, wenn der Grund für das Beenden nicht klar ist.