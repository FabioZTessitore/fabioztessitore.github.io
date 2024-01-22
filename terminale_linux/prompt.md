# Il prompt dei comandi

Torna all'[indice](../toc.md)

---

Una volta aperto un terminale, molto probabilmente vedrai un testo simile a questo:

```
fabio@ubuntu ~ $
```

È il _prompt_. Il terminale informa che il nome utente è **fabio**, che il nome del computer su cui si sta lavorando è **ubuntu**, che ci si trova nella directory personale, indicata con **~** (tilde), e che l'utente è non amministratore (simbolo **$**). Inoltre il terminale è in attesa di ricevere comandi.

### I primi comandi

Per eseguire un comando basta scriverne il nome e battere `INVIO`.

> Tieni presente che in questa fase non è importante comprendere il significato dell'output stampato sul terminale.

Per cominciare chiediamo data e ora:

```
$ date

dom 30 ott 2016, 20.55.33, CET
```

Continuiamo chiedendo qual è il nome del computer:

```
$ hostname

ubuntu
```

Oppure qual è la directory di lavoro:

```
$ pwd

/home/fabio
```

Infine chiediamo la lista di file e directory presenti nella directory corrente:

```
$ ls

Documenti Immagini Modelli Scaricati
Scrivania Wallpapers work
```

### Letture

> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 3: Using the Shell

---

Torna all'[indice](../toc.md)
