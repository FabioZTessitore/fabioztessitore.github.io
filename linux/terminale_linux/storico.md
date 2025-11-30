# Lo storico dei comandi

Torna all'[indice](../../toc.md)

---

### Tasti freccia

La shell di Linux è uno strumento molto potente, ma a volte le operazioni
risultano ripetitive. Esistono, però, diversi modi per semplificare e
velocizzare il lavoro. La shell, infatti, memorizza i comandi eseguiti
e permette di richiamarli in maniera facile e veloce premendo i tasti
`FRECCIA SU` e `FRECCIA GIÙ`. Quando si trova quello che si stava
cercando non bisogna fare altro che premere `INVIO` come al solito.

### Il comando `history`

Usare i tasti freccia semplifica il lavoro, soprattutto quando bisogna
digitare comandi lunghi e complessi, ma resta il problema che bisogna
continuare a premere `FRECCIA SU` finché non si trova quanto cercato
e se il comando desiderato non veniva digitato da molto tempo la
ricerca sarà lenta e noiosa. Si può, allora, utilizzare il comando
`history` il quale mostra la lista dei comandi digitati insieme ad un comodo indice.

```bash
$ history

...
43 ls
44 tail -n 2 /etc/passwd
...
```

Per lanciare il comando `tail`, che ha indice `44`:

```bash
$ !44
```

Se prima di richiamare il comando si vogliono fare delle modifiche
c'è `fc`. Si aprirà l'editor di testi predefinito dove si potrà modificare
il comando a piacere. Una volta finito basta salvare ed uscire
dall'editor e il comando andrà in esecuzione.

```bash
$ fc 44
```

### Ricerca all'indietro

La shell di Linux mette a disposizione strumenti diversi per eseguire
le stesse operazioni. In questo modo ognuno troverà quello che più si
addice alle proprie esigenze.

Digitiamo, ad esempio, la combinazione di tasti `CTRL R`. Da questo
momento in poi, ogni volta che si digita un carattere, il terminale
effettuerà una ricerca all'indietro (dal più recente al meno) mostrando
il comando corrispondente trovato.

### Completamento automatico

Quando si digitano i comandi, i nomi di file e directory ecc.,
il tasto `TAB` è di grande aiuto. Permette il completamento automatico
facendo risparmiare tempo e fatica ed evitando, al contempo, anche errori di battitura.

---

Torna all'[indice](../../toc.md)
