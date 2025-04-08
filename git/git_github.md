# git e github.com

Torna all'[indice](../toc.md)

---

### GitHub

[GitHub.com](https://github.com) è un servizio online creato per facilitare
la collaborazione tra sviluppatori. Prima di iniziare a usarlo bisogna registrarsi.

Una volta effettuato il primo accesso non sarà difficile capire come creare una nuova _repository_.

> [!INFO]
> Una repository non è altro che una directory ospitata sui server di GitHub.com

Alla creazione di una nuova repository, necessariamente `public` per ora,
si consiglia vivamente di mettere la
spunta su "creazione di un file README". Così facendo, quando la repository
remota verrà clonata sul proprio computer (e a breve vedremo come fare), non ci
saranno problemi di autenticazione e sarà
già presente il file `README.md` su cui effettueremo le prime operazioni.

> [!WARNING]
> Inoltre, nei _Settings_ della repository, si possono aggiungere dei collaboratori.
> A dispetto del nome non è il metodo migliore per collaborare, ma sarà molto utile
> in queste fasi iniziali, nel caso si abbia bisogno di aiuto da parte di qualcuno più esperto.

### git

Una delle operazioni fondamentali quando si scrive codice è la gestione delle modifiche
al codice stesso. Questa operazione prende il nome di _controllo delle versioni_.

`git` è un sistema di _controllo delle versioni_ creato da Linus Torvalds, il padre
di Linux, che si sposa molto bene con il servizio GitHub.com (ma può essere utilizzato
anche solo in locale o in congiunzione con altri servizi).

Dopo aver installato `git` sul proprio sistema, prima di poterlo utilizzare,
è necessario effettuare una configurazione. In particolare, le informazioni minime
da fornire sono il proprio nome e la propria email. Questi dettagli verranno
associati ai _commit_ creati in seguito.

```bash
$ git config --global user.name "YOUR NAME HERE"
$ git config --global user.email "YOUR EMAIL HERE"
```

Assicuriamoci che tutto sia andato bene: dovrebbe essere stato creato un file (nascosto) `~/.gitconfig`.

```bash
$ cd
$ ls -a

... .gitconfig ...

$ cat .gitconfig

[user]
    email = YOUR@EMAIL
    name = YOUR NAME
```

---

Torna all'[indice](../toc.md)
