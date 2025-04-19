# Regole dei linguaggi di programmazione

Torna all'[indice](../toc.md)

---

Per programmare abbiamo bisogno di un _linguaggio di programmazione_, ma prima di iniziare a studiarne qualcuno vediamo quali sono le regole generali che li caratterizzano.

Tutti i linguaggi sono composti da un _alfabeto_ `a b c ... + - * / % { } [ ] ...` (i simboli utilizzabili) e da _regole_ su come combinare i vari elementi.

Le regole si dividono in:

1. Sintassi;
1. Grammatica;
1. Semantica.

### Sintassi

La sintassi di un linguaggio di programmazione ci dice se una sequenza di caratteri e simboli è valida oppure no. Ad es.:

```py
3 + 4 # OK
3 4 + # NO!
```

### Grammatica

Non tutte le sequenze, anche se corrette dal punto di vista della sintassi, hanno senso. La grammatica ci dà proprio questa informazione.

```py
3 / 4     # OK
3 / 'abc' # NO! (pero' la sintassi e' corretta)
```

La sintassi della seconda istruzione è corretta perché c'è un valore, il numero `3`, seguito dall'operatore `/`, seguito ancora da un altro valore, la _stringa_ `'abc'`. La sequenza `valore operatore valore` va bene, ma chiaramente non ha senso dividere il numero `3` per la stringa `abc`.

### Semantica

La semantica ci dice cosa significa quello che scriviamo.

> [!WARNING]
> Un programma potrebbe essere corretto dal punto di vista della sintassi e della grammatica, ma fare qualcosa di diverso da quello che ci aspettavamo!

---

Torna all'[indice](../toc.md)
