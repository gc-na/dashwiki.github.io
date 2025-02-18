# [Svenska] Debian Almquist Shell (dash) umask användning: Ställer in standardbehörigheter för nya filer

## Översikt
`umask` är ett kommando som används för att ställa in standardbehörigheter för nya filer och kataloger som skapas i ett Unix-liknande operativsystem. Det definierar vilka behörigheter som ska tas bort från de standardbehörigheter som tilldelas av systemet.

## Användning
Den grundläggande syntaxen för kommandot `umask` är:

```sh
umask [alternativ] [argument]
```

## Vanliga alternativ
- `-S`: Visar umask-värdet i symbolisk form.
- `-p`: Visar det aktuella umask-värdet för den aktuella sessionen.

## Vanliga exempel
Här är några praktiska exempel på hur `umask` kan användas:

### Visa nuvarande umask-värde
För att se det aktuella umask-värdet kan du använda:

```sh
umask
```

### Ställ in umask-värde
För att ställa in umask-värdet till `022`, vilket ger skrivbehörighet för ägaren och läs-/exekveringsbehörighet för grupp och andra, använd:

```sh
umask 022
```

### Visa umask i symbolisk form
För att visa umask-värdet i symbolisk form, använd:

```sh
umask -S
```

### Ställ in umask-värde till `077`
För att ställa in umask-värdet till `077`, vilket ger fullständig behörighet för ägaren och inga behörigheter för grupp och andra, använd:

```sh
umask 077
```

## Tips
- Kom ihåg att umask-värdet påverkar endast nya filer och kataloger som skapas efter att kommandot har körts.
- Det kan vara bra att kontrollera umask-värdet innan du skapar känsliga filer för att säkerställa att de har rätt behörigheter.
- Du kan lägga till `umask`-kommandot i din shell-konfigurationsfil (t.ex. `.bashrc` eller `.profile`) för att ställa in ett standardvärde varje gång du loggar in.