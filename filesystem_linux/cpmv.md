# Copiare, spostare, rinominare

Torna all'[indice](../toc.md)

---

Per concludere questa sezione vediamo come copiare, spostare e rinominare file e directory.

### Copiare

Iniziamo creando un file nella home:

```bash
$ cd
$ touch test
$ ls

... test ...
```

Proviamo a farne una copia con `cp`:

```bash
$ cp test test2
$ ls

... test test2 ...
```

### Spostare e Rinominare

Per rinominare un file si usa `mv`:

```bash
$ mv test test_nuovo
$ ls

... test2 test_nuovo ...
```

Il comando `mv` serve anche a spostare un file.

```bash
$ mkdir prog
$ touch esercizio.c    # OOOPS doveva andare in prog
$ mv esercizio.c prog/
```

### Copiare directory

Per copiare una directory si usa sempre `cp`, ma bisogna aggiungere l'opzione `-r`
affinché la copia sia ricorsiva. Creiamo una directory `progetti` e inseriamo
al suo interno vari file e directory. Infine proviamo a copiarla:

```bash
$ cp -r progetti progetti_backup_2016_11_27
```

> [!TIP]
> Per spostare o rinominare una directory (comando `mv`) non è necessaria l'opzione `-r`.
> Infatti in questi casi si sta modificando il nome e/o la posizione della directory,
> ma non il suo contenuto. Se, invece, la si vuole copiare, bisogna fare una copia di
> tutto ciò che contiene e quindi si deve usare l'opzione `-r` per effettuare un'operazione ricorsiva.

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 4: Moving Around the Filesystem

---

Torna all'[indice](../toc.md)
