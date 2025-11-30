# Dove sono i comandi

Torna all'[indice](../../toc.md)

---

Per mandare in esecuzione un qualunque programma, che sia fatto da noi o che sia
un comando di sistema, bisogna conoscerne il percorso (_path_) completo. Ad esempio,
il comando `date` si trova in `/bin`, quindi, per mandarlo in esecuzione, dovremmo scrivere:

```bash
$ /bin/date
```

ma la cosa non è conveniente! Affinché la shell possa capire che scrivendo `date`
intendiamo `/bin/date`, i comandi vengono memorizzati in particolari directory e
i nomi di queste directory vengono aggiunti alla variabile `PATH`.

```bash
$ echo $PATH

/usr/local/bin:/usr/bin:/bin
```

In `PATH` è memorizzata una lista di directory, separate dal simbolo `:`.
Tali directory verranno controllate sequenzialmente alla ricerca del comando
invocato. È importante notare come in `PATH` non sia presente il simbolo `.`,
per cui è necessario usare la sintassi `./nomefile` quando si vuole eseguire
un programma presente nella directory corrente.

> [!WARNING]
> È una buona prassi lasciare le cose come stanno e non aggiungere `.` a `PATH`.
> Infatti, quando invochiamo un comando di sistema vogliamo essere sicuri
> che sia quello originale e non un omonimo programma creato da noi o da qualche malintenzionato.

Un'altra cosa. Non tutto ciò che viene invocato dalla shell ha un file
corrispondente nel filesystem. Finora abbiamo parlato di comandi e abbiamo
detto che ogni comando è un file eseguibile presente in una particolare
directory, ma questa cosa non è sempre vera.

La shell cerca i comandi in un ordine ben preciso:

1. alias
1. parole riservate della shell
1. funzioni definite nella shell
1. comandi interni (built-in)
1. comandi nel filesystem (PATH)

Dato un comando, per capire di che si tratta si usa `type`:

```bash
$ type bash

bash e' /bin/bash

$ type date

date e' /bin/date

$ type ll

ll ha "ls -l" come alias

$ type ls

ls ha "ls --color=auto" come alias
```

Nell'ultimo caso `ls` è un alias per `ls --color=auto`, ma sappiamo che esiste
davvero il comando `ls` nel filesystem. Allora possiamo usare l'attributo
`-a` di `type` per mostrare tutte le occorrenze:

```bash
$ type -a ls

ls ha "ls --color=auto" come alias
ls e' /bin/ls
```

---

Torna all'[indice](../../toc.md)
