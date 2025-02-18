# [Linux] Debian Almquist Shell (dash) sed utilizare: Modificarea textului în flux

## Overview
Comanda `sed` (stream editor) este un editor de fluxuri care permite manipularea textului în moduri variate. Aceasta poate fi utilizată pentru a modifica, a șterge sau a adăuga text în fișiere sau în fluxuri de date, oferind un instrument puternic pentru procesarea textului.

## Usage
Sintaxa de bază a comenzii `sed` este următoarea:

```bash
sed [opțiuni] [argumente]
```

## Common Options
- `-e`: Permite specificarea unei comenzi `sed` direct în linia de comandă.
- `-i`: Modifică fișierele în loc să le scrie pe stdout. Aceasta este utilizată pentru a face modificări directe în fișiere.
- `-n`: Suprimă ieșirea implicită, permițând utilizarea comenzii `p` pentru a imprima doar liniile selectate.
- `s/pattern/replacement/`: Comandă de substituție care caută un model și îl înlocuiește cu un text specificat.

## Common Examples
1. **Substituirea unui cuvânt într-un fișier:**
   ```bash
   sed -i 's/vechi/nou/g' fisier.txt
   ```
   Aceasta va înlocui toate aparițiile cuvântului "vechi" cu "nou" în `fisier.txt`.

2. **Ștergerea liniilor care conțin un anumit cuvânt:**
   ```bash
   sed -i '/cuvânt_de_șters/d' fisier.txt
   ```
   Aceasta va șterge toate liniile care conțin "cuvânt_de_șters" din `fisier.txt`.

3. **Afișarea liniilor care conțin un anumit cuvânt:**
   ```bash
   sed -n '/cuvânt_de_căutat/p' fisier.txt
   ```
   Aceasta va afișa doar liniile care conțin "cuvânt_de_căutat".

4. **Adăugarea unui text la sfârșitul fiecărei linii:**
   ```bash
   sed 's/$/ text_adăugat/' fisier.txt
   ```
   Aceasta va adăuga "text_adăugat" la sfârșitul fiecărei linii din `fisier.txt`.

## Tips
- Folosiți opțiunea `-i` cu precauție, deoarece modificările sunt permanente. Este recomandat să faceți o copie de rezervă a fișierului înainte de a efectua modificări.
- Testați comenzile `sed` fără `-i` pentru a verifica rezultatele înainte de a aplica modificările directe.
- Utilizați expresii regulate pentru a crea modele mai complexe, permițând manipulări avansate ale textului.