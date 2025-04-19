# L'ambiente della shell

Torna all'[indice](../toc.md)

---

### I file di configurazione della shell

Quando abbiamo provato a creare alias, riavviando il computer abbiamo fatto
la spiacevole scoperta di averli persi. La shell, per poter svolgere i propri
compiti, utilizza alcuni file di configurazione. Quel che è successo è che non
abbiamo salvato i nuovi alias all'interno di questi file. Utilizzando la shell
`bash`, una delle più comuni, ci sono cinque file di configurazione
(non necessariamente devono essere tutti presenti).

| File            | Descrizione                                             | Istante in cui viene eseguito    |
| --------------- | ------------------------------------------------------- | -------------------------------- |
| /etc/profile    | configurazione generale di tutti gli utenti             | al login                         |
| /etc/bashrc     | configurazione generale di tutti gli utenti, shell bash | all'apertura di ogni nuova shell |
| ~/.bash_profile | configurazione specifica per ogni utente                | al login                         |
| ~/.bashrc       | configurazione specifica per ogni utente, shell bash    | al login e per ogni nuova shell  |
| ~/.bash_logout  |                                                         | all'uscita                       |

`/etc/profile` e `/etc/bashrc` non possono essere toccati, servono i permessi di
amministratore. `~/.bash_profile` spesso non è presente. `~/.bash_logout` non fa
altro che pulire lo schermo all'uscita. L'unico interessante è `~/.bashrc`
(attenzione al fatto che è un file nascosto, il nome inizia con il `.`).

### Alias permanenti

A questo punto possiamo creare un alias che sia sempre presente nel sistema.
Va definito all'interno del file `~/.bashrc`. Apriamo il file e alla fine aggiungiamo la riga:

```bash
alias d='date +%D'
```

Infine salviamo ed usciamo dall'editor.

Non bisogna dimenticare che il file `.bashrc` viene eseguito al login o
quando si apre una nuova shell. Per forzarne la rilettura senza
effettuare un logout e successivo login:

```bash
$ source $HOME/.bashrc
$ d

...
```

### Modificare il prompt dei comandi

Sempre nel file `.bashrc` troveremo la definizione di una variabile chiamata `PS1`.
Essa determina come verrà visualizzato il prompt dei comandi.

> [!WARNING]
> È consigliabile fare una copia di backup del file prima di iniziare a effettuare
> modifiche. Linux permette l'accesso ai file di configurazione, ma chi rompe si tiene i cocci.

### Creazione di altre variabili d'ambiente

Così come viene definita `PS1`, possiamo creare anche altre variabili in base
alle esigenze. Immaginiamo di avere una directory con i nostri progetti
annidata all'interno di molte altre directory. Una cosa del tipo
`~/projects/work/javascript/models/`. Invece di scrivere ogni volta:

```bash
$ cd ~/projects/work/javascript/models
```

possiamo creare una variabile, `P`, sempre in `.bashrc`, contenente il percorso di nostro interesse:

```bash
P=$HOME/projects/work/javascript/models/
```

e quindi scrivere:

```bash
$ cd $P
```

per raggiungere la directory.

---

Torna all'[indice](../toc.md)
