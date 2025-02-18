# [Nederlands] Debian Almquist Shell (dash) umask gebruik: Beheer van bestandspermissies

## Overzicht
De `umask`-opdracht in de Debian Almquist Shell (dash) wordt gebruikt om de standaard bestandspermissies in te stellen voor nieuwe bestanden en mappen. Het bepaalt welke rechten niet worden toegewezen aan nieuwe bestanden die door de gebruiker worden gemaakt.

## Gebruik
De basis syntaxis van de `umask`-opdracht is als volgt:

```bash
umask [opties] [argumenten]
```

## Veelvoorkomende opties
- `-S`: Toont de huidige umask in symbolische notatie.
- `-p`: Toont de umask-instelling voor de huidige shell.

## Veelvoorkomende voorbeelden

### Huidige umask weergeven
Om de huidige umask-waarde te bekijken, gebruik je simpelweg:

```bash
umask
```

### Umask instellen
Om de umask in te stellen op een specifieke waarde, bijvoorbeeld `022`, gebruik je:

```bash
umask 022
```

### Umask in symbolische notatie weergeven
Om de huidige umask in symbolische notatie te zien, gebruik je:

```bash
umask -S
```

### Umask instellen voor de huidige shell
Als je de umask voor de huidige shell wilt instellen en deze wilt behouden voor de sessie, gebruik je:

```bash
umask 027
```

## Tips
- Het is een goede gewoonte om de umask in je shell-configuratiebestand (zoals `.bashrc` of `.profile`) in te stellen, zodat deze automatisch wordt toegepast bij het starten van een nieuwe sessie.
- Wees voorzichtig bij het instellen van een te permissieve umask, zoals `000`, omdat dit kan leiden tot beveiligingsrisico's door ongewenste toegang tot bestanden.
- Controleer regelmatig je umask-instellingen, vooral op servers of gedeelde systemen, om ervoor te zorgen dat de bestandspermissies veilig zijn.