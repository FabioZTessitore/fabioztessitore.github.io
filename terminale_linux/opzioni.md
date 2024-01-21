# Le opzioni dei comandi

Torna all'[indice](../toc.md)

---

A volte è necessario cambiare il comportamento dei comandi per ottenere il risultato voluto. Tale variazione si ottiene attraverso le _opzioni_. Per esempio, il comando `ls` permette di ottenere la lista degli oggetti presenti nella directory corrente. Aggiungendo l'opzione `-l` si possono ottenere molte informazioni in più.

```
$ ls -l

totale 36
drwxr-xr-x  2 fabio fabio  4096 set 22 19:14 Documenti
drwxr-xr-x  2 fabio fabio  4096 giu  3 17:18 Immagini
drwxr-xr-x  2 fabio fabio  4096 ago 26 20:15 Modelli
drwxr-xr-x  4 fabio fabio 12288 ott 27 14:13 Scaricati
drwxr-xr-x 25 fabio fabio  4096 ott 30 20:30 Scrivania
drwxr-xr-x  2 fabio fabio  4096 set 18 20:21 Wallpapers
drwxr-xr-x 25 fabio fabio  4096 ago 31 17:23 work
```

> Non è questo il momento di approfondire il significato di tutte queste informazioni. Si tenga presente, invece, il modo in cui sono state ottenute: attraverso un'opzione (`-l`) data ad un comando (`ls`).

Proviamo qualche altra opzione:

```
$ ls -a

.              .gimp-2.8     Wallpapers
..             .gitconfig    work
.atom          .gnome
.bash_history  .gnome2
.bash_logout   Immagini
.bashrc        Modelli
.config        Scaricati
.cups          Scrivania
Documenti      .vim
```

L'opzione `-a` mostra tutti i file, anche quelli nascosti (hanno il nome che inizia con un puntino).

```
$ ls -t

Scrivania  Scaricati  Documenti  Wallpapers  work  Immagini
Modelli
```

L'opzione `-t` riordina in base alla data di modifica.

### Raggruppare le opzioni

Si possono fornire più opzioni ad un comando contemporaneamente:

```
$ ls -l -t

...
```

ma è più comodo raggrupparle:

```
$ ls -lt

drwxr-xr-x 25 fabio fabio  4096 ott 30 20:30 Scrivania
drwxr-xr-x  4 fabio fabio 12288 ott 27 14:13 Scaricati
drwxr-xr-x  2 fabio fabio  4096 set 22 19:14 Documenti
drwxr-xr-x  2 fabio fabio  4096 set 18 20:21 Wallpapers
drwxr-xr-x 25 fabio fabio  4096 ago 31 17:23 work
drwxr-xr-x  2 fabio fabio  4096 giu  3 17:18 Immagini
drwxr-xr-x  2 fabio fabio  4096 ago 26 20:15 Modelli
```

### Opzioni con nomi lunghi

Alcune opzioni hanno nomi composti da più di una lettera. Per evitare ambiguità si usa il doppio trattino `--`.

```
$ ls --help

Uso: ls [OPZIONE]... [FILE]...
List information about the FILEs
(the current directory by default).
...
```

Il doppio trattino `--` fa in modo che la parola `help` sia considerata nella sua interezza e non come una lista di opzioni separate.

### Letture

> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 3: Using the Shell

---

Torna all'[indice](../toc.md)
