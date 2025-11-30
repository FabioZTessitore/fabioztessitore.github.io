# Rimuovere file e directory

Torna all'[indice](../../toc.md)

---

La shell permette anche di rimuovere file e directory. Per iniziare creiamo un file
di nome `primo.c` nella home.

```bash
$ cd
$ touch primo.c
$ ls

... primo.c ...
```

### Rimuovere un file

Per rimuoverlo, il comando è `rm`:

```bash
$ rm primo.c
$ ls

...
```

### Rimuovere una directory _vuota_

Per le directory bisogna fare più attenzione. Se la directory da eliminare è vuota si può usare `rmdir`:

```bash
$ mkdir test_dir
$ ls

... test_dir ...

$ rmdir test_dir
$ ls

...
```

Se, invece, c'è anche solo un file all'interno, `rmdir` fallirà. Per poter utilizzare
`rmdir`, prima di eliminare la directory stessa, vanno cancellati i file presenti al suo interno.

### Rimuovere una directory

Se, però, immaginiamo una situazione comune in cui all'interno della directory in questione
ci sono non solo file, ma anche altre directory, ognuna delle quali potrebbe contenere
file e directory a sua volta ... insomma non è consigliabile proseguire su questa strada.
Per fortuna il comando `rm` (quello usato per rimuovere i file) possiede l'opzione `-r`
che permette di eliminare _ricorsivamente_ tutto ciò che si trova all'interno di una directory:

```bash
$ cd
$ mkdir -p progetti/python/helloworld
$ touch progetti/python/helloworld/hello.py   # TAB ...
$ rm -r progetti    # ATTENZIONE, cancella tutto il contenuto di progetti
```

---

Torna all'[indice](../../toc.md)
