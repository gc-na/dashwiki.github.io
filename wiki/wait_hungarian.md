# [Debian] Debian Almquist Shell (dash) wait használata: A folyamatok várakoztatása

## Áttekintés
A `wait` parancs a shellben arra szolgál, hogy megvárja a háttérben futó folyamatok befejeződését. Ez hasznos lehet, ha egy szkriptben szeretnénk biztosítani, hogy egy vagy több háttérfolyamat befejeződjön, mielőtt további utasításokat hajtanánk végre.

## Használat
A `wait` parancs alapvető szintaxisa a következő:

```bash
wait [opciók] [argumentumok]
```

## Gyakori Opciók
- `-n`: Várakozik az első befejeződő háttérfolyatra.
- `PID`: Megadja a konkrét folyamat azonosítóját, amelynek befejeződésére várni szeretnénk.

## Gyakori Példák
1. Várakozás minden háttérfolyamat befejeződésére:

```bash
sleep 5 &
sleep 3 &
wait
echo "Minden háttérfolyamat befejeződött."
```

2. Várakozás egy konkrét folyamatra PID alapján:

```bash
sleep 10 &
pid=$!
wait $pid
echo "A folyamat befejeződött."
```

3. Várakozás az első háttérfolyatra:

```bash
sleep 5 &
sleep 3 &
wait -n
echo "Az első háttérfolyamat befejeződött."
```

## Tippek
- Használj `wait`-et, ha szkriptekben több háttérfolyamatot indítasz, és biztosítani szeretnéd, hogy a következő lépések csak a folyamatok befejeződése után történjenek.
- A PID tárolásával könnyen nyomon követheted, hogy melyik folyamatra vársz, így rugalmasabbá teheted a szkriptedet.
- Ha nem adsz meg PID-t, a `wait` az összes háttérfolyamat befejeződésére vár.