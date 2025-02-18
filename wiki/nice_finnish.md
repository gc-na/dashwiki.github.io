# [Suomi] Debian Almquist Shell (dash) nice käyttö: Prosessien prioriteetin säätäminen

## Yleiskatsaus
`nice`-komento mahdollistaa prosessien prioriteetin säätämisen Unix-pohjaisissa käyttöjärjestelmissä. Sen avulla voit määrittää, kuinka paljon prosessi saa CPU-aikaa verrattuna muihin prosesseihin. Korkeampi "nice"-arvo tarkoittaa alhaisempaa prioriteettia, mikä voi olla hyödyllistä, kun haluat vähentää tietyn prosessin vaikutusta järjestelmän suorituskykyyn.

## Käyttö
Perussyntaksi `nice`-komennolle on seuraava:
```bash
nice [vaihtoehdot] [argumentit]
```

## Yleiset vaihtoehdot
- `-n, --adjustment=N`: Määrittää prioriteettimuutoksen arvon (N). Positiivinen arvo lisää nice-arvoa ja negatiivinen vähentää sitä.
- `--help`: Näyttää aputiedot `nice`-komennosta.
- `--version`: Näyttää version tiedot.

## Yleiset esimerkit
1. **Suorita prosessi normaalilla nice-arvolla:**
   ```bash
   nice myscript.sh
   ```

2. **Suorita prosessi, jossa nice-arvo on 10:**
   ```bash
   nice -n 10 myscript.sh
   ```

3. **Suorita prosessi, jossa nice-arvo on -5 (vaatii yleensä root-oikeudet):**
   ```bash
   sudo nice -n -5 myscript.sh
   ```

4. **Tarkista prosessin nice-arvo:**
   ```bash
   ps -o pid,nice,cmd
   ```

## Vinkit
- Käytä `nice`-komentoa erityisesti silloin, kun suoritat resursseja vaativia prosesseja, mutta haluat varmistaa, että järjestelmä pysyy responsiivisena.
- Muista, että `nice`-komento ei voi nostaa prosessin prioriteettia ilman root-oikeuksia; se voi vain laskea sitä.
- Voit yhdistää `nice`-komennon muihin komentoihin, kuten `nohup`, jotta prosessi jatkaa toimintaansa myös kirjautuessasi ulos.