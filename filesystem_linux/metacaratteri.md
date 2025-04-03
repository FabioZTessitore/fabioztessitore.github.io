# I metacaratteri

Torna all'[indice](../toc.md)

---

La shell di Linux accetta vari caratteri speciali. Quando si opera sui file,
ad esempio, questi caratteri possono aiutare a lavorare con maggiore efficienza.
I _metacaratteri_, in particolare, permettono di selezionare più file
contemporaneamente senza doverne scrivere il nome per esteso.

- `*` significa qualunque sequenza di caratteri (anche nessuno);
- `?` significa un carattere qualsiasi (però solo e soltanto uno);
- `[abcxyz]` significa un carattere qualsiasi tra quelli elencati tra parentesi.

Ecco qualche esempio di utilizzo:

```bash
$ cd
$ mkdir words
$ cd words
$ touch ape bici grappolo ghepardo garage
```

Ora supponiamo di voler cercare un file, ma di ricordare solo che il nome
inizia per `'a'`. Si può chiedere alla shell di mostrare i file che hanno
questa caratteristica:

```bash
$ ls a*

ape
```

Oppure solo quelli che iniziano per `'g'`:

```bash
$ ls g*

grappolo ghepardo garage
```

Oppure quelli che iniziano per `'g'` ma terminano in `'e'`:

```bash
$ ls g*e

garage
```

> [!TIP]
> Un eventuale file di nome `ge` sarebbe stato mostrato perché `*` significa **zero o più** caratteri.

Allo stesso modo si può chiedere la lista dei file che hanno una `'e'` nel nome, in posizione qualsiasi:

```bash
$ ls *e*

ape ghepardo garage
```

Il carattere `?` significa, invece, **solo e soltanto un** carattere. Quindi
`'?p*'` significa che la `'p'` è la seconda lettera seguita da qualunque cosa,
mentre `'???p*'` significa che la `'p'` è la quarta lettera.

```bash
$ ls ?p*

ape

$ ls ???p*

grappolo ghepardo
```

Riguardo alle parentesi quadre `[...]`, esse sono utilissime. Immaginiamo di
non essere sicuri che il file cercato inizi per `'a'`, ma abbiamo il dubbio
che possa iniziare con `'b'`. Con `[ab]*` chiediamo proprio questo, un file
che inizia per `'a'` **oppure** per `'b'`. In altre parole il primo carattere
può essere uno qualsiasi tra quelli elencati.

```bash
$ ls [ab]*

ape bici

$ ls [ag]*[ei]

ape garage
```

Le parentesi `[]` diventano ancora più utili quando viene specificato un intervallo:

```bash
$ ls [a-g]* # lettera iniziale compresa tra 'a' e 'g'

ape bici grappolo ghepardo garage
```

---

Torna all'[indice](../toc.md)
