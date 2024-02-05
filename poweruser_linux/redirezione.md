# La redirezione

Torna all'[indice](../toc.md)

---

Alcuni metacaratteri _redirigono_ (dirigono altrove) l'input e l'output da e verso i file.

### Redirezione dello standard input

Abbiamo già detto che alcuni comandi accettano un file come argomento. Il seguente comando mostra il contenuto del file `/etc/passwd`.

```bash
$ cat /etc/passwd

...
```

In effetti quello che stiamo facendo è chiedere che il contenuto del file `/etc/passwd` sia **rediretto** verso il comando `cat` (che poi a sua volta lo invierà al terminale). Questa cosa si può esplicitare con il carattere `<` (da immaginare come una freccia):

```bash
$ cat < /etc/passwd # come prima, ma esplicitando la redirezione
```

Siccome redirigere il contenuto di un file verso un comando è un'operazione molto comune, il simbolo `<` è spesso opzionale e quindi omesso.

### Redirezione dello standard output

Al contrario, il simbolo `>` (anche questo da immaginare come una freccia), redirige l'output di un comando verso un file, mentre normalmente l'output dei comandi finirebbe sullo schermo.

> [!CAUTION]
> Se il file indicato esiste già, verrà sovrascritto senza preavviso

```bash
$ cd
$ cat /etc/passwd > copia_password
$ ls

... copia_password ...
```

`cat /etc/passwd` mostrerebbe sullo schermo il contenuto del file `/etc/passwd`, ma, grazie alla redirezione, il tutto finisce nel file `copia_password`. In altre parole abbiamo fatto una copia del file.

> [!TIP]
> Con la redirezione dell'output qualunque cosa possa essere stampata a video può essere copiata in un file

### Redirezione dello standard error

A volte, quando si esegue un comando, possono comparire degli errori. Tali errori vengono stampati sullo _standard error_, generalmente lo schermo, come per l'output. Se vogliamo raccoglierli per mostrarli a qualcuno, possiamo farlo con la redirezione dello standard error:

```bash
$ touch /prova 2> errore_salvato # accesso negato
```

Per salvare sia l'output normale che gli errori c'è `&>`.

### Aggiungere testo in coda (_append_)

A volte si ha la necessità di _aggiungere_ del testo ad un file non vuoto. La redirezione dell'output lo sovrascriverebbe facendoci perdere il vecchio contenuto. In questi casi possiamo usare `>>`:

```bash
$ cat /etc/group >> copia_password # Aggiunge il contenuto di /etc/group a copia_password
```

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 4: Moving Around the Filesystem

---

Torna all'[indice](../toc.md)
