# [Nederlands] Debian Almquist Shell (dash) logout gebruik: Sluit de huidige shell-sessie af

## Overzicht
De `logout`-opdracht wordt gebruikt om de huidige shell-sessie af te sluiten. Dit is vooral nuttig wanneer je werkt in een interactieve shell en je deze wilt beëindigen zonder de terminal volledig te sluiten.

## Gebruik
De basis syntaxis van de `logout`-opdracht is als volgt:

```sh
logout [opties]
```

## Veelvoorkomende Opties
De `logout`-opdracht heeft geen specifieke opties, maar het kan in verschillende contexten worden gebruikt, zoals in een subshell. In dat geval sluit het de subshell af en keert het terug naar de bovenliggende shell.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudig afmelden
Om je huidige shell-sessie af te sluiten, typ je gewoon:

```sh
logout
```

### Voorbeeld 2: Afmelden vanuit een subshell
Als je in een subshell werkt (bijvoorbeeld na het uitvoeren van een script), kun je de `logout`-opdracht gebruiken om terug te keren naar de bovenliggende shell:

```sh
sh
# Voer hier enkele opdrachten uit
logout
```

## Tips
- Zorg ervoor dat je al je werk hebt opgeslagen voordat je `logout` uitvoert, omdat het je sessie onmiddellijk beëindigt.
- Gebruik `exit` in plaats van `logout` als je niet zeker weet of je in een subshell bent; `exit` werkt in zowel subshells als de hoofd-shell.
- Het gebruik van `logout` is alleen effectief in een interactieve shell; in niet-interactieve shells heeft het geen effect.