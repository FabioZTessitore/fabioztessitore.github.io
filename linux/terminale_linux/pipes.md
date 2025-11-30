# Connettere i comandi

Torna all'[indice](../../toc.md)

---

Uno dei principi alla base della progettazione dei comandi della shell di Linux
è _fai una sola cosa, ma falla bene_. Ma, allora, se ogni comando esegue una
singola operazione elementare, come si possono soddisfare tutte le esigenze
di gestione e amministrazione di un sistema? La risposta sta nel _combinare_
i comandi tra loro in modo da ottenere le funzionalità necessarie.

### Comandi sequenziali

Il modo più semplice per combinare comandi è quello di mandarli in esecuzione
uno dopo l'altro _in sequenza_. In questo caso si usa l'operatore `;`.
Immaginiamo di voler stampare la data corrente e la directory in uso.
Si lanciano i comandi `date` e `pwd` in sequenza in questo modo:

```bash
$ date; pwd

lun 26 dic 2016, 19.57.32, CET
/home/fabio/Documenti/laboratorio
```

### Pipe

Un altro strumento per connettere comandi, molto più potente del primo,
è la _pipe_. Una pipe (operatore `|`) permette di redirigere l'output di
un comando verso l'input di un altro.
Il comando successivo può fare delle operazioni sull'output del comando
precedente in modo da ottenere il risultato voluto.

```bash
$ cat /etc/passwd | sort
```

Il comando `cat /etc/passwd` **non** mostra il contenuto del file `/etc/passwd`
perché c'è una pipe con il comando `sort`. Quest'ultimo riceve il contenuto
di `/etc/passwd`, lo riordina e solo dopo avviene la stampa.

Lo stesso esempio, ma stampa in ordine inverso:

```bash
$ cat /etc/passwd | sort -r
```

Proviamo questi comandi come esercitazione (`du` (disk usage), mostra la dimensione dei file):

```bash
$ du /bin/*
```

Come prima, ma stavolta riordina (numericamente, non alfabeticamente)

```bash
$ du /bin/* | sort -nr
```

Come prima, ma mostra solo i primi dieci elementi grazie a `head`
(in altre parole i dieci file più grandi di `/bin`).

```bash
$ du /bin/* | sort -nr | head
```

---

Torna all'[indice](../../toc.md)
