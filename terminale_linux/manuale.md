# Le pagine del manuale

Torna all'[indice](../toc.md)

---

La shell di Linux è uno strumento molto potente e non è semplice ricordare tutto a memoria. Ci vengono in aiuto le _pagine del manuale_.

Immaginiamo di voler stampare la data corrente nel formato `gg/mm/aaaa`. Per iniziare proviamo a richiamare il comando `date`:

```bash
$ date

mer  9 nov 2016, 21.43.59, CET
```

`date` fa il suo lavoro, ma il formato in cui viene stampata la data non è quello desiderato. Proviamo, allora, a consultare le pagine del manuale:

```bash
$ man date

DATE(1)

NAME
    date - print or set the system date and time

SYNOPSIS
    date [OPTION]... [+FORMAT]
    date [-u|--utc|--universal] [MMDDhhmm[[CC]YY][.ss]]

DESCRIPTION
    Display the current time in the given FORMAT, ...
```

Nella parte alta si legge come usare il comando. In questo caso

`date [OPTION]... [+FORMAT]`

Le parentesi quadre indicano argomenti ed opzioni facoltative. Scorrendo la pagina troviamo la lista dei possibili formati di stampa della data.

Mettendo insieme otteniamo:

```bash
$ date +%x

09/11/2016
```

Si riporta un altro esempio per maggiore chiarezza. Stampa giorno, mese e anno separati da un trattino:

```bash
$ date +%d-%m-%Y

09-11-2016
```

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 3: Using the Shell

---

Torna all'[indice](../toc.md)
