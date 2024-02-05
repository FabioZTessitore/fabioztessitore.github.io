# Espansione delle variabili, delle espressioni aritmetiche, dei comandi

Torna all'[indice](../toc.md)

---

### Espansione delle variabili

La shell di Linux mette a disposizione dell'utente una serie di variabili contenenti svariate informazioni. Ad esempio, la variabile `BASH` contiene il percorso dell'eseguibile della shell in uso. Per visualizzarne il contenuto:

```bash
$ echo $BASH

/bin/bash
```

Controlliamo:

```bash
$ ls -l $BASH

-rwxr-xr-x 1 root root 1099016 nov 15 19:49 /bin/bash
```

Memorizzando il percorso della shell in una variabile, tutti i file di configurazione, e l'utente stesso, possono far riferimento a `$BASH` senza preoccuparsi di sapere qual è il file attualmente in uso.

Sono definite molte altre variabili. Visualizziamo il contenuto di `HOME` e `USER`. La shell sa un sacco di cose!

### Espansione delle espressioni aritmetiche

La shell di Linux è uno strumento estremamente versatile. Permette anche di fare operazioni aritmetiche.

```bash
$ echo "I am $[2017-1979] years old!"

I am 38 years old!
```

### Espansione dei comandi

Il comando precedente sarebbe più utile se l'anno non fosse scritto, bensì calcolato. Conosciamo già un comando in grado di dire qual è l'anno in corso, `date`.

```bash
$ date +%Y
```

A questo punto non resta altro da fare che inserire un comando all'interno di un altro comando. A tal proposito esistono gli operatori `$()` oppure gli apici inversi.

```bash
$ echo "I am $[$(date +%Y)-1979] years old!"

... # il risultato dipende dall'anno in corso!
```

Un altro esempio:

```bash
$ echo "There are $(ls | wc -w) files in this directory."

There are 15 files in this directory.
```

Viene prima eseguito il comando `ls`, poi la pipe con `wc` (word count) che conta le parole (opzione `-w`). Infine avviene la stampa con `echo` del numero di file nella directory (il numero di parole contato da `wc -w`).

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 3: Using the Shell

---

Torna all'[indice](../toc.md)
