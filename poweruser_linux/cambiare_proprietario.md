# Cambiare il proprietario

Torna all'[indice](../toc.md)

---

Per cambiare proprietario (o gruppo proprietario o entrambi) a un file si
usa il comando `chown`. Per ovvie ragioni un utente normale non può cambiare
il proprietario di un file che non gli appartiene. In altre parole non può
intestarsi la proprietà dei file altrui. Questa operazione può essere
eseguita solo dall'utente `root` oppure da un utente che abbia permessi di amministratore.

Facciamo un esempio:

```bash
$ touch test
$ ls -l test

-rw-r--r-- 1 fabio fabio 0 dic  8 16:33 test

$ sudo chown root test    # cambia il proprietario in root
$ ls -l test

-rw-r--r-- 1 root fabio 0 dic  8 16:33 test

$ sudo chown root:root test  # cambia proprietario e gruppo in root

$ ls -l test

-rw-r--r-- 1 root root 0 dic  8 16:33 test
```

### Letture

> [!TIP]
> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 4: Moving Around the Filesystem

---

Torna all'[indice](../toc.md)
