# [Română] Debian Almquist Shell (dash) export utilizare: Setarea variabilelor de mediu

## Overview
Comanda `export` în shell-ul Debian Almquist (dash) este utilizată pentru a seta variabile de mediu, făcându-le disponibile pentru procesele copil. Aceasta permite partajarea informațiilor între diferite sesiuni de shell și aplicații.

## Usage
Sintaxa de bază a comenzii `export` este următoarea:

```sh
export [opțiuni] [argumente]
```

## Common Options
- `-n`: Dezactivează exportul unei variabile de mediu.
- `-p`: Afișează toate variabilele de mediu exportate.

## Common Examples
1. **Exportarea unei variabile simple:**
   ```sh
   MY_VAR="Hello, World!"
   export MY_VAR
   ```

2. **Exportarea și inițializarea unei variabile într-o singură comandă:**
   ```sh
   export MY_VAR="Hello, World!"
   ```

3. **Afișarea variabilelor de mediu exportate:**
   ```sh
   export -p
   ```

4. **Dezactivarea exportului unei variabile:**
   ```sh
   export -n MY_VAR
   ```

## Tips
- Este recomandat să folosești `export` pentru variabilele pe care dorești să le faci disponibile în subprocese, cum ar fi scripturi sau aplicații.
- Verifică întotdeauna variabilele de mediu exportate cu `export -p` pentru a te asigura că sunt setate corect.
- Fii atent la numele variabilelor; este o practică bună să folosești litere mari pentru variabilele de mediu pentru a le distinge de variabilele locale.