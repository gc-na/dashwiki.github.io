# [Svenska] Debian Almquist Shell (dash) dirname användning: Hämta katalognamn från sökvägar

## Översikt
Kommandot `dirname` används för att extrahera katalognamnet från en given sökväg. Det returnerar den del av sökvägen som representerar katalogen, vilket kan vara användbart för skript och filhantering.

## Användning
Den grundläggande syntaxen för kommandot är:

```
dirname [alternativ] [argument]
```

## Vanliga alternativ
- `-z`: Behandla tomma strängar som en giltig sökväg.
- `--help`: Visa hjälpmeddelande för kommandot.
- `--version`: Visa versionsinformation för `dirname`.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `dirname`:

1. Hämta katalognamnet från en filväg:
   ```sh
   dirname /home/user/documents/file.txt
   ```
   Utdata: `/home/user/documents`

2. Hämta katalognamnet från en relativ sökväg:
   ```sh
   dirname ./folder/subfolder/file.txt
   ```
   Utdata: `./folder/subfolder`

3. Använda `dirname` i ett skript för att få katalognamnet:
   ```sh
   FILE_PATH="/usr/local/bin/script.sh"
   DIR_NAME=$(dirname "$FILE_PATH")
   echo "Katalognamnet är: $DIR_NAME"
   ```
   Utdata: `Katalognamnet är: /usr/local/bin`

## Tips
- Använd `dirname` i kombination med andra kommandon som `basename` för att hantera filvägar mer effektivt.
- Tänk på att `dirname` alltid returnerar en sökväg, även om den är tom, vilket kan vara användbart i vissa skript.
- För att undvika problem med specialtecken i sökvägar, omge alltid dina argument med citattecken.