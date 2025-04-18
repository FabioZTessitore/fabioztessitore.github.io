# I permessi

Torna all'[indice](../toc.md)

---

Tra le altre cose, quando si esegue il comando `ls -l`, vengono mostrati i _permessi_.

```bash
$ ls -l

totale 68
-rw-r--r-- 1 fabio fabio 1272 gen 12 2016 404.html
-rw-r--r-- 1 fabio fabio 3959 gen 12 2016 apple-touch-icon.png
-rw-r--r-- 1 fabio fabio 417 gen 12 2016 browserconfig.xml
-rw-r--r-- 1 fabio fabio 611 gen 12 2016 crossdomain.xml
drwxr-xr-x 2 fabio fabio 4096 nov 26 18:35 css
drwx------ 2 fabio fabio 4096 nov 26 18:35 doc
-rw-r--r-- 1 fabio fabio 766 gen 12 2016 favicon.ico
-rw-r--r-- 1 fabio fabio 229 gen 12 2016 humans.txt
drwx------ 2 fabio fabio 4096 nov 26 18:35 img
-rw-r--r-- 1 fabio fabio 2502 nov 27 16:23 index.html
drwxr-xr-x 3 fabio fabio 4096 nov 26 18:35 js
-rw-r--r-- 1 fabio fabio 1056 gen 12 2016 LICENSE.txt
-rw-r--r-- 1 fabio fabio 564 nov 26 19:16 listaeventi.php
-rw-r--r-- 1 fabio fabio 22 nov 26 19:23 README.md
-rw-r--r-- 1 fabio fabio 78 gen 12 2016 robots.txt
-rw-r--r-- 1 fabio fabio 3482 gen 12 2016 tile.png
-rw-r--r-- 1 fabio fabio 1854 gen 12 2016 tile-wide.png
```

Essi indicano quali operazioni possono (o non possono) effettuare gli utenti
del sistema su quei particolari file e directory.

La prima cosa da sapere è che per utilizzare un sistema Linux bisogna creare
un utente. Il nome utente viene generalmente stampato all'interno del prompt.
Ogni utente può appartenere ad uno o più _gruppi_. In molti sistemi, quando
si crea un utente si crea anche un gruppo con lo stesso nome, e si inserisce l'utente in quel gruppo.

Nella stampa precedente la seconda e la terza colonna riportano il nome `fabio`.
La prima volta è il nome del _proprietario_ del file (l'utente), la seconda
volta è il nome del _gruppo proprietario_ del file.

Per capire il senso di tutto ciò bisogna parlare dei permessi. I permessi
vengono divisi in tre gruppi. Il primo gruppo si riferisce ai _permessi dell'utente
proprietario_ del file. Il secondo si riferisce ai _permessi del gruppo proprietario_,
e infine il terzo si riferisce a _tutti gli altri_.

### Permessi e file

Consideriamo, ad esempio, il file `robots.txt`:

```bash
$ ls -l robots.txt

-rw-r--r-- 1 fabio fabio 78 gen 12 2016 robots.txt
```

Il primo carattere `-` indica che si tratta di un file regolare (non una directory
o altro). Poi ci sono altri nove caratteri: `rw-r--r--`, che vanno letti a tre a tre.
I primi tre `rw-` sono i permessi del proprietario del file (utente `fabio`).
I secondi tre `r--` sono i permessi del gruppo proprietario del file (gruppo `fabio`).
Gli ultimi tre `r--` sono i permessi degli altri utenti (non il proprietario e
non gli utenti che appartengono al gruppo proprietario).

Il proprietario `fabio` può leggere il contenuto del file (lo può aprire) perché
c'è la `r` (_read_). Inoltre può scrivere nel file (salvare delle modifiche)
perché c'è la `w` (_write_). Il terzo carattere è un segno `-` che significa _assenza_
del corrispondente permesso. In questo caso il permesso mancante è quello di
esecuzione `x` (semplificando, il file non può essere lanciato come un comando).

Il secondo gruppo di permessi `r--` si riferisce al gruppo proprietario
(più precisamente agli utenti appartenenti al gruppo). È presente solo il
permesso di lettura, mancano invece quello di scrittura e quello di esecuzione.
Quindi, un altro utente, diciamo `claudio`, appartenente al gruppo `fabio`,
può solo leggere il contenuto di `robots.txt`, ma non effettuare delle modifiche.

Inoltre anche tutti gli altri utenti potranno leggere il contenuto del file
perché anche tra gli ultimi tre caratteri c'è il permesso di lettura `r--`.

### Permessi e directory

Nella stampa in alto ci sono anche delle directory, come ad esempio, `css`:

```bash
$ ls -l css
drwxr-xr-x 2 fabio fabio 4096 nov 26 18:35 css
```

Da notare, innanzitutto, che il primo carattere è una `d`.

Riguardo ai permessi lo schema non cambia, ci sono sempre tre gruppi da tre caratteri
relativi a proprietario, gruppo proprietario e altri. Quello che cambia è il
significato dei simboli:

- `r`, permesso di lettura, indica la possibilità di leggere la lista dei file contenuti;
- `w`, permesso di scrittura, indica la possibilità di aggiungere, cancellare
  o modificare file (ad esempio cambiarne il nome);
- `x`, permesso di accedere e attraversare la directory.

Quindi, nel caso dell'esempio, l'utente `fabio` può fare tutto: leggere
il contenuto della directory, modificarlo (creando file ecc.), e accedere
ad essa. Resta da chiarire cosa significa attraversare una directory.
Immaginiamo che nella directory `css` sia presente un'altra directory,
chiamiamola `base`. Si potrebbe voler effettuare l'operazione `cd css/base`
per _attraversare_ `css` in modo da raggiungere `base`.

---

Torna all'[indice](../toc.md)
