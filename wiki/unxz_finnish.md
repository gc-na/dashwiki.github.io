# [Suomi] Debian Almquist Shell (dash) unxz käyttö: Purkaa XZ-pakkauksia

## Yleiskatsaus
`unxz` on komento, jota käytetään XZ-muotoon pakattujen tiedostojen purkamiseen. Se poistaa XZ-pakkauksen ja palauttaa alkuperäisen tiedoston.

## Käyttö
Perussyntaksi komennolle on seuraava:
```
unxz [valinnat] [argumentit]
```

## Yleiset Valinnat
- `-k`, `--keep`: Säilyttää alkuperäisen pakatun tiedoston purkamisen jälkeen.
- `-f`, `--force`: Pakottaa purkamisen, vaikka tiedostoja olisi jo olemassa.
- `-v`, `--verbose`: Näyttää yksityiskohtaisempaa tietoa purkamisprosessista.

## Yleiset Esimerkit
1. **Perustiedoston purkaminen:**
   ```
   unxz tiedosto.xz
   ```

2. **Alkuperäisen tiedoston säilyttäminen purkamisen jälkeen:**
   ```
   unxz -k tiedosto.xz
   ```

3. **Purkaminen pakotettuna:**
   ```
   unxz -f tiedosto.xz
   ```

4. **Yksityiskohtaisen tiedon näyttäminen purkamisen aikana:**
   ```
   unxz -v tiedosto.xz
   ```

## Vinkit
- Käytä `-k`-valintaa, jos haluat säilyttää alkuperäisen tiedoston, erityisesti suurten tiedostojen kanssa.
- Tarkista aina, että sinulla on riittävästi levytilaa ennen purkamista, sillä purkaminen voi vaatia enemmän tilaa kuin pakattu tiedosto.
- Voit yhdistää `unxz`-komennon putkistoon muiden komentojen kanssa, kuten `tar`, purkaaksesi ja käsitelläksesi tiedostoja yhdellä kertaa.