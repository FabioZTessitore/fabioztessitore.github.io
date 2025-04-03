# Creare file e directory

Torna all'[indice](../toc.md)

---

Per poter creare file e directory direttamente dalla shell bisogna trovarsi
necessariamente all'interno della propria home (o sottodirectory di essa).
In caso contrario non si potrebbe creare o modificare alcunché perché un
utente normale (non amministratore) non ha il permesso di scrivere al di fuori
della propria directory personale.

> Assicuriamoci di essere nella `home`

```bash
$ cd
$ pwd

/home/fabio
```

### Creare un file vuoto

Iniziamo creando un file vuoto. Il comando da utilizzare è `touch`:

```bash
$ touch prova
$ ls

... prova ...
```

### Creare una directory

Per le directory c'è invece `mkdir`:

```bash
$ mkdir provadir
$ ls

... provadir ...
```

#### Esempio

Immaginiamo di voler creare nella home le directory `progetti/javascript/helloworld/`
e di voler inserire il file `hello.js` all'interno di `helloworld/`:

```bash
$ cd # assicuriamoci di essere nella home
$ mkdir progetti   # crea progetti/ ed entra
$ cd progetti
$ mkdir javascript # crea javascript/ ed entra
$ cd javascript
$ mkdir helloworld # crea helloworld/ ed entra
$ cd helloworld
$ touch hello.js   # infine crea il file hello.js
```

Quando bisogna creare tante directory una dentro l'altra si può usare una
scorciatoia: aggiungere l'opzione `-p` a `mkdir`:

> [!CAUTION]
> Attraverso l'interfaccia grafica vanno cancellate le directory create in
> precedenza altrimenti non si potranno ricreare da shell

```bash
$ cd
$ mkdir -p progetti/javascript/helloworld
$ cd progetti/javascript/helloworld # TAB TAB TAB
$ touch hello.js
```

---

Torna all'[indice](../toc.md)
