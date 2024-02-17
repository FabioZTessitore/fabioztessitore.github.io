# Cercare file

Torna all'[indice](../toc.md)

---

### Cercare file con `locate`

Esistono vari modi per cercare file. Uno di questi è fornito dal comando `locate`. È un comando molto veloce nell'effettuare ricerche perché non cerca nel filesystem, ma in un database interno. Ovviamente potranno essere trovati solo i file che sono stati aggiunti in precedenza al database stesso. Il database può essere aggiornato solo dall'utente root mediante il comando `updatedb`, anche se spesso questo aggiornamento viene eseguito periodicamente sul sistema senza che gli utenti debbano fare nulla.

Il file `/etc/updatedb.conf` specifica quali directory devono essere tenute sotto controllo.

Proviamo ad effettuare una ricerca:

```bash
$ locate passwd

/etc/passwd
...
```

Per fare ricerche senza tenere conto della differenza tra maiuscole e minuscole c'è l'opzione `-i`.

```bash
$ locate -i bashrc

...
```

### Cercare file con `find`

In alternativa a `locate` c'è `find`. Si tratta di uno strumento molto più potente anche se più lento perché effettua la ricerca nel filesystem stesso. Permette di effettuare ricerche in base a vari criteri: nome del file, proprietà, permessi, dimensioni, data di modifica, ecc. Visto che `find` cerca nel filesystem, si può velocizzare la ricerca limitandola ad alcune parti di esso:

```bash
$ find /etc # mostra tutti i file presenti in /etc
```

Volendo si può ottenere un output più completo con l'opzione `-ls`.

```bash
$ find /etc -ls
```

Ovviamente se non si hanno i permessi per effettuare ricerche in certe directory si otterranno una serie di messaggi di errore. Per evitarne la visualizzazione ricordiamoci di effettuare la redirezione dello standard error.

```bash
$ find /root -ls 2> lista_errori
$ ls

... lista_errori ...
```

In casi come questo non ha molto senso salvare gli errori in un file e basterà scartare quel tipo di output. Quindi, invece di fare la redirezione verso un file, è meglio farla verso `/dev/null`.

```bash
$ find /root -ls 2> /dev/null
```

#### Cercare file per nome

Proviamo a effettuare ricerche in base a vari criteri. Iniziamo cercando per nome. Cerchiamo un file chiamato `passwd` nella directory `/etc`.

```bash
$ find /etc -name passwd
```

Oppure scartando gli eventuali errori dovuti a mancanza di permessi:

```bash
$ find /etc -name passwd 2> /dev/null
```

Per ignorare la differenza tra maiuscole e minuscole si usa `-iname`:

```bash
$ find /etc -iname *passwd*
```

#### Cercare file per dimensione

Oltre che per nome, si possono cercare i file che hanno una determinata dimensione mediante l'attributo `-size`.

```bash
$ find $HOME -size +10M # cerca i file più grandi di 10MB
```

```bash
$ find $HOME -size +3M -size -1G # file più grandi di 3MB ma più piccoli di 1GB
```

#### Cercare file per proprietario

Per cercare file che hanno uno specifico proprietario, `find` mette a disposizione l'attributo `-user`:

```bash
$ find $HOME -user fabio -ls
```

La stessa cosa si può fare per i gruppi:

```bash
$ find $HOME -group fabio -ls
```

Una cosa molto utile potrebbe essere cercare file che _non_ ci appartengono:

```bash
$ find $HOME -not -user $USER -ls
```

#### Cercare file con specifici permessi

La ricerca di file con specifici permessi viene effettuata tramite l'attributo `-perm`.

```bash
$ find /bin -perm 755 -ls
```

Quando il codice numerico fornito a `-perm` non è preceduto da alcun segno (come nell'esempio), tutti i bit devono coincidere. In questo caso, quindi, `find` cercherà i file della directory `/bin` che hanno permessi esattamente pari a `rwxr-xr-x` (codice 755).

Quando, invece, il codice è preceduto dal segno meno, `find` cercherà tutti i file che hanno _almeno_ quei permessi. Cerchiamo i file nella directory `/bin` che hanno permessi uguali o superiori a `rwxr-xr-w`:

```bash
$ find /bin -perm -755 -ls
```

Quando il numero è preceduto dal simbolo `/`, cerca tutti i file in cui almeno uno tra il proprietario, il gruppo e gli altri utenti hanno quei permessi.

Cerchiamo i file nella directory `/bin` in cui almeno uno tra proprietario, gruppo e altri hanno il permesso di scrittura:

```bash
$ find /bin -perm /222 -ls
```

Questa modalità può essere utilizzata, per esempio, per cercare file che hanno il permesso di scrittura aperto agli altri, a prescindere dagli altri permessi:

```bash
$ find /bin -perm /002 -ls
```

#### Cercare per data

`find` permette anche di cercare file che hanno subito variazioni nel tempo. L'attributo `mtime` è utilizzato per cercare variazioni nel _contenuto_ dei file. `ctime` cerca variazioni nel _proprietario_ o nei _permessi_. `atime` cerca variazioni nell'_ultimo accesso_ ai file. Queste variazioni sono conteggiate in giorni. Se si preferisce contare in minuti si possono usare `mmin`, `cmin`, `amin`.

Cerchiamo i file di `/etc` il cui contenuto è cambiato negli ultimi 10 minuti:

```bash
$ find /etc -mmin -10
```

Cerchiamo i file in `/bin`, `/usr/bin`, `/sbin`, `/usr/sbin`, che hanno cambiato proprietario o permessi negli ultimi tre giorni:

```bash
$ find /bin /usr/bin /sbin /usr/sbin -ctime -3
```

Cerchiamo file in `/var/ftp` e `/var/www` che non hanno avuto accesso da più di 300 giorni:

```bash
$ find /var/ftp /var/www -atime +300
```

#### Combinare i criteri di ricerca

Per combinare i criteri di ricerca esistono gli operatori logici `-o` (or), `-and`, `-not`.

```bash
$ find /home -user fabio -o -user claudio -ls
```

```bash
$ find /home -user fabio -not -group fabio -ls
```

#### Eseguire comandi sui risultati di ricerca

Contestualmente alla ricerca è possibile eseguire comandi sui file risultato della ricerca stessa. Esistono, a questo scopo, `-exec` e `-ok`. La differenza tra i due sta nel fatto che quest'ultimo chiede conferma prima di eseguire il comando. Per esempio, eseguiamo il comando `du -sh` sui risultati di ricerca:

```bash
$ find $HOME -size +30M -exec du -sh {} \\;
```

Oppure eseguiamo il comando `du` (senza opzioni) sui risultati di ricerca e poi riordiniamo in ordine decrescente.

```bash
$ find /home -size +5M -exec du {} \\; | sort -nr
```

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 3: Using the Shell
> - Chap 5: Working with Text Files

---

Torna all'[indice](../toc.md)
