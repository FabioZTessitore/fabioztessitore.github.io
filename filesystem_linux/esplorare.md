# Esplorare il filesystem

Torna all'[indice](../toc.md)

---

I comandi principali per esplorare il filesystem sono:

- `ls` per chiedere la lista degli oggetti presenti nella directory corrente;
- `pwd` per conoscere il nome della directory corrente;
- `cd` per spostarsi tra le directory.

Iniziamo spostandoci nella directory root `/` per mostrarne il contenuto:

```bash
$ cd /
$ ls

bin  boot  dev  etc  home  lib  lib64  root
sbin  tmp  usr  ...
```

Chiediamo conferma della directory corrente:

```bash
$ pwd

/
```

Proviamo un altro spostamento, questa volta nella directory `/etc`:

```bash
$ cd /etc

$ pwd
/etc

$ ls

...
```

### La directory home

Per tornare nella propria directory personale esistono vari modi, quindi andiamo per gradi.

La directory personale ha nome pari al nome utente (`fabio` nel mio caso) e si trova all'interno della directory `/home`.

```bash
$ cd /home
$ ls

... fabio ...

$ cd fabio
```

#### Percorsi assoluti e relativi

Nell'ultimo comando, `cd fabio`, non c'è il simbolo `/` prima del nome della directory. Infatti la directory `fabio` non si trova all'interno della root `/`, ma all'interno della `/home` (in cui già ci troviamo).

In altre parole, il percorso `/home/fabio` è un _percorso assoluto_ (parte da `/`), mentre `fabio` è un _percorso relativo_ (relativo alla directory corrente, `home`, in cui ci troviamo).

Siccome tornare alla propria home è un'operazione piuttosto comune esistono delle scorciatoie.

Innanzitutto si può fare riferimento alla directory personale mediante il simbolo `~` (tilde).

```bash
$ cd ~
$ pwd

/home/fabio
```

La tilde è comodissima per riferirsi a directory presenti nella propria home senza dover scrivere percorsi assoluti. Ad esempio, per spostarsi nella propria directory `Documenti`:

```bash
$ cd ~/Documenti
$ pwd

/home/fabio/Documenti
```

Si può anche lanciare il comando `cd` senza argomenti ottenendo lo stesso effetto di `cd ~`.

```bash
$ cd
$ pwd

/home/fabio
```

Un altro utilizzo molto comune e molto utile di `cd` è quello che permette di tornare alla directory precedente.

```bash
$ cd
$ cd Documenti/progetti/javascript/modelli/src  # facciamo finta di essere in una cartella molto profonda
$ cd    ### OPS! così torniamo alla home
$ cd -  # nessun problema, torniamo in src
```

### Directory speciali

Quando si esegue il comando `ls -a` vengono mostrati due simboli speciali, `.` e `..`.

```bash
$ cd
$ pwd

/home/fabio

$ ls -a

. .. .bashrc Documenti Immagini Modelli
Scaricati Scrivania
```

- `.` rappresenta la directory corrente;
- `..` rappresenta la directory genitore.

Ad esempio, trovandosi in `/etc`:

- `.` rappresenta `/etc` stessa;
- `..` rappresenta `/` (la directory che contiene `etc`).

Di conseguenza, `..` può essere utilizzato per uscire dalla directory corrente:

```bash
$ cd /etc
$ pwd

/etc

$ cd ..
$ pwd

/
```

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 4: Moving Around the Filesystem

---

Torna all'[indice](../toc.md)
