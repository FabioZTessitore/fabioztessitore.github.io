# Cambiare i permessi

Torna all'[indice](../toc.md)

---

### Cambiare i permessi con i numeri

Ai vari permessi sono associati dei numeri (come i pesi delle cifre di un numero binario):

- `r` = 4
- `w` = 2
- `x` = 1

Ad es., se sono stati impostati i permessi `r--` il valore corrispondente sarà 4. Invece `rw-` corrisponde a `4 + 2 = 6`. Allo stesso modo `r-x` è equivalente a `4 + 1 = 5` e `rwx` a `4 + 2 + 1 = 7`.

Il comando che permette di cambiare i permessi è `chmod`:

```bash
$ touch file_test
$ chmod 777 file_test
$ ls -l file_test

-rwxrwxrwx 1 fabio fabio 0 dic 8 16:02 file_test

$ chmod 755 file_test
$ ls -l file_test

-rwxr-xr-x 1 fabio fabio 0 dic 8 16:02 file_test

$ chmod 644 file_test
$ ls -l file_test

-rw-r--r-- 1 fabio fabio 0 dic 8 16:02 file_test
```

### Cambiare i permessi con le lettere

I permessi possono essere aggiunti e tolti anche mediante i simboli `+` e `-`; ad es. `+r` aggiunge il permesso di lettura, `-r` lo revoca.

Usando le lettere bisogna specificare a chi si vogliono aggiungere o togliere permessi:

- `u` utente proprietario (user)
- `g` gruppo (group)
- `o` gli altri (others)
- `a` tutti (all)

```bash
$ touch file_test2
$ ls -l file_test2

-rw-r--r-- 1 fabio fabio 0 dic 8 16:12 file_test2
```

Aggiunge il permesso di esecuzione a tutti:

```bash
$ chmod a+x file_test2
$ ls -l file_test2

-rwxr-xr-x 1 fabio fabio 0 dic 8 16:12 file_test2
```

Toglie i permessi di scrittura ed esecuzione a gruppo e altri:

```bash
$ chmod go-wx file_test2
$ ls -l file_test2

-rwxr--r-- 1 fabio fabio 0 dic 8 16:12 file_test2
```

Aggiunge il permesso di esecuzione solo al gruppo:

```bash
$ chmod g+x file_test2
$ ls -l file_test2

-rwxr-xr-- 1 fabio fabio 0 dic 8 16:12 file_test2
```

### Letture

> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 4: Moving Around the Filesystem

---

Torna all'[indice](../toc.md)
