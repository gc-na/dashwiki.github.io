# [Svenska] Debian Almquist Shell (dash) diff användning: Jämför filer rad för rad

## Översikt
Kommandot `diff` används för att jämföra innehållet i två filer rad för rad. Det visar skillnaderna mellan filerna, vilket gör det enkelt att se vad som har ändrats, lagts till eller tagits bort.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
diff [alternativ] [fil1] [fil2]
```

## Vanliga alternativ
- `-u`: Visar skillnaderna i ett sammanfattat format (unified).
- `-c`: Visar skillnaderna i ett kontextformat.
- `-i`: Ignorerar skillnader i versaler och gemener.
- `-w`: Ignorerar alla blanksteg.
- `-r`: Jämför kataloger rekursivt.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `diff`:

1. Jämför två textfiler:
   ```bash
   diff fil1.txt fil2.txt
   ```

2. Använda unified format för att visa skillnader:
   ```bash
   diff -u fil1.txt fil2.txt
   ```

3. Jämför två kataloger rekursivt:
   ```bash
   diff -r katalog1/ katalog2/
   ```

4. Ignorera skillnader i blanksteg:
   ```bash
   diff -w fil1.txt fil2.txt
   ```

## Tips
- Använd `diff -u` för att få en mer läsbar översikt av skillnaderna, särskilt när du arbetar med kod.
- Om du ofta jämför samma filer kan det vara bra att skapa ett skript som automatiserar processen.
- Tänk på att `diff` kan användas tillsammans med andra verktyg som `patch` för att tillämpa ändringar från en fil till en annan.