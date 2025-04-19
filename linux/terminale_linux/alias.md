# Gli alias

Torna all'[indice](../toc.md)

---

Quando si creano comandi personalizzati, ad esempio mediante pipe oppure includendo
un comando all'interno di un altro comando, si può _salvare_ il comando ottenuto
in modo da poterlo riutilizzare in seguito senza dover riscrivere tutto. In altre
parole si può creare un _alias_. La shell mette a disposizione la possibilità di
creare sinonimi (alias, appunto) per comandi singoli o in gruppo. Iniziamo
visualizzando gli alias già impostati sulla macchina:

```bash
$ alias

alias ls='ls --color=auto'
...
```

In questo caso il comando `ls` viene interpretato come `ls --color=auto` e questo
permette di vedere file e directory colorate.

Proviamo ad impostare un nuovo alias:

```bash
$ alias rm='rm -i'
```

D'ora in avanti il comando `rm` sarà interpretato come `rm -i` e prima di rimuovere qualche
file verrà chiesto il consenso a procedere.

Proviamo con un gruppo di comandi ricordando che per lanciare comandi in sequenza si usa il `;`.

```bash
$ alias p='pwd; ls -CF'
```

`pwd` mostra la directory corrente. `ls` il suo contenuto utilizzando una visualizzazione a colonne.

Per rimuovere un alias esiste il comando `unalias`:

```bash
$ unalias p
```

---

Torna all'[indice](../toc.md)
