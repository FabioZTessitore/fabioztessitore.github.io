# Le parentesi graffe

Torna all'[indice](../toc.md)

---

Grazie alle parentesi graffe si possono ottenere risultati sorprendenti con poco sforzo. Ad esempio, per creare i file `test1`, `test2`, `test3`, `test4` e `test5`, non è necessario ripetere la parola `"test"` ogni volta:

```bash
$ cd
$ touch test{1,2,3,4,5}
$ ls test*

test1 test2 test3 test4 test5
```

Ora immaginiamo di voler creare delle directory per i nostri progetti in `C`, in `Python` e in `JavaScript`, sia per l'utente `fabio` che per l'utente `claudio`. Potremmo creare le directory una alla volta:

```bash
$ mkdir fabio_c fabio_python ... # ma che noia!
```

Oppure potremmo sfruttare le parentesi graffe:

```bash
$ mkdir {fabio,claudio}_{c,python,js}
$ ls

fabio_c fabio_python fabio_js claudio_c claudio_python claudio_js
```

Ovviamente possiamo cancellarle allo stesso modo:

```bash
$ rmdir {fabio,claudio}_{c,python,js}
```

Il doppio punto `..` serve per specificare intervalli:

```bash
$ touch {a..f}-{1..5}
$ ls
a1 a2 a3 a4 a5 b1 b2 b3 ... f4 f5
```

### Letture

> C. Negus, _Linux Bible_, Indianapolis, Wiley &amp; Sons, 2020, 10th ed
>
> - Chap 4: Moving Around the Filesystem

---

Torna all'[indice](../toc.md)
