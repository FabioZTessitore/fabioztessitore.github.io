# Effettuare modifiche

Torna all'[indice](../toc.md)

---

Una volta all'interno della directory `test` si può modificare il contenuto del
file `README.md` aggiungendo una piccola descrizione:

```bash
$ vim README.md # qualunque editor va bene
```

A questo punto entra in gioco git. Affinché il sistema tenga traccia delle
modifiche effettuate i comandi da eseguire sono i seguenti:

```bash
$ git status
$ git add README.md
$ git status
$ git commit -m "descrizione della modifica"
$ git push origin main
```

> [!WARNING]
> GitHub non accetta più la password come metodo di autenticazione nella fase di push.
> Al posto della password bisogna utilizzare un _token_ il quale può essere generato sul
> sito GitHub.com nella sezione _Settings_, sottosezione _Developer settings_,
> _Personal access tokens_. Dopo aver cliccato su _Generate new token_ bisogna
> compilare il campo _Note_ introducendo una descrizione del token e soprattutto bisogna spuntare _Repo_

> [!DANGER]
> Il token generato da GitHub va conservato con cura e non potrà più essere recuperato
> dal sito. In caso di smarrimento (oppure alla scadenza) bisogna generarne uno nuovo

Se tutto è andato per il verso giusto sul sito dovrà comparire la versione modificata del file `README.md`.

### Spiegazione dei comandi

I comandi di `git` possono sembrare complessi a prima vista. Per poter ricordare
meglio i passi da eseguire bisogna capire qual è lo scopo di ognuno di essi:

1. l'operazione `git status` serve per capire qual è la situazione attuale nella directory;
1. l’operazione `git add` può essere immaginata come il posizionare i file in posa
   davanti a una _macchina fotografica_. Si tenga presente che si potrebbero modificare
   più file ma volerne "fotografare" solo alcuni;
1. l’operazione `git commit` rappresenta lo scatto della foto che quindi immortala
   lo stato dei file in quell'istante;
1. l’operazione `git push` invia la nuova foto ai server di GitHub.

### Letture

> [!TIP] > _Getting Git Right_, [www.atlassian.com/git](https://www.atlassian.com/git)
>
> - [Saving Changes](https://www.atlassian.com/git/tutorials/saving-changes)

---

Torna all'[indice](../toc.md)
