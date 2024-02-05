# Gli argomenti dei comandi

Torna all'[indice](../toc.md)

---

Molti comandi accettano anche _argomenti_. Un argomento è un'informazione extra come, ad esempio, il nome di un file su cui il comando stesso dovrà agire. Ecco alcuni esempi:

Mostra il contenuto del file `/etc/passwd`:

```bash
$ cat /etc/passwd
```

Mostra solo le ultime due righe di `/etc/passwd`:

```bash
$ tail -n 2 /etc/passwd
```

Nell'esempio appena visto gli argomenti sono due: il numero `2` è argomento dell'opzione `-n`, il file `/etc/passwd` è argomento del comando `tail`.

Anche le opzioni con nomi lunghi possono accettare argomenti, però cambia la sintassi. Spesso in questi casi l'argomento segue il simbolo `=`.

Mostra la lista degli oggetti nella directory corrente, nasconde `Documenti`:

```bash
$ ls --hide=Documenti
```

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 3: Using the Shell

---

Torna all'[indice](../toc.md)
