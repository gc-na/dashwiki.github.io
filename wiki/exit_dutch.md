# [Nederlands] Debian Almquist Shell (dash) exit gebruik: Beëindig een shell-sessie

## Overzicht
Het `exit` commando in de Debian Almquist Shell (dash) wordt gebruikt om een shell-sessie te beëindigen. Dit kan handig zijn wanneer je klaar bent met je taken in de terminal en de sessie wilt afsluiten.

## Gebruik
De basis syntaxis van het `exit` commando is als volgt:

```
exit [status]
```

Hierbij is `[status]` een optionele parameter die de exitstatus aangeeft. Een status van 0 betekent meestal dat het programma succesvol is uitgevoerd, terwijl een andere waarde een fout of een andere status kan aanduiden.

## Veelvoorkomende opties
- `status`: Een geheel getal dat de exitstatus aangeeft. Standaard is dit 0 als er geen status wordt opgegeven.

## Veelvoorkomende voorbeelden

- **Sessie beëindigen zonder status op te geven:**
  ```sh
  exit
  ```

- **Sessie beëindigen met een specifieke exitstatus:**
  ```sh
  exit 1
  ```

- **Sessie beëindigen na het uitvoeren van een script:**
  ```sh
  ./script.sh
  exit $?
  ```

- **Sessie beëindigen in een subshell:**
  ```sh
  (exit 0)
  ```

## Tips
- Gebruik `exit 0` om aan te geven dat je sessie zonder fouten is beëindigd.
- Vergeet niet dat als je `exit` aanroept vanuit een subshell, dit alleen die specifieke subshell beëindigt.
- Het is een goede gewoonte om altijd een exitstatus op te geven bij het beëindigen van scripts, zodat andere scripts of programma's weten hoe het is afgelopen.