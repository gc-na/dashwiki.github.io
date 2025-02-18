# [Nederlands] Debian Almquist Shell (dash) export gebruik: Omgevingsvariabelen instellen

## Overzicht
Het `export` commando in de Debian Almquist Shell (dash) wordt gebruikt om omgevingsvariabelen in te stellen. Wanneer een variabele wordt geëxporteerd, is deze beschikbaar voor alle subprocessen die vanuit de huidige shell worden gestart.

## Gebruik
De basis syntaxis van het `export` commando is als volgt:

```sh
export [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-p`: Toont alle geëxporteerde variabelen en hun waarden.
- `-n`: Verwijdert de exportstatus van een variabele, waardoor deze niet langer beschikbaar is voor subprocessen.

## Veelvoorkomende Voorbeelden

### Een variabele exporteren
Om een variabele te exporteren, gebruik je het volgende commando:

```sh
export VARIABEL=waarde
```

### Meerdere variabelen exporteren
Je kunt ook meerdere variabelen in één commando exporteren:

```sh
export VAR1=waarde1 VAR2=waarde2
```

### Een variabele bekijken
Om te controleren of een variabele is geëxporteerd, kun je het `env` commando gebruiken:

```sh
env | grep VARIABEL
```

### Exporteren van een bestaande variabele
Als je een bestaande variabele wilt exporteren, gebruik je:

```sh
VARIABEL=waarde
export VARIABEL
```

### Exporteren zonder een waarde toe te wijzen
Je kunt ook een variabele exporteren zonder deze een waarde toe te wijzen:

```sh
export VARIABEL
```

## Tips
- Zorg ervoor dat je variabelen een duidelijke naam hebben om verwarring te voorkomen.
- Gebruik het `-p` argument om een lijst van alle geëxporteerde variabelen te bekijken, wat handig kan zijn voor foutopsporing.
- Vergeet niet dat geëxporteerde variabelen alleen beschikbaar zijn voor subprocessen, niet voor de huidige shell.