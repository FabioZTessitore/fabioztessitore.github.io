# Espressioni

Torna all'[indice](../toc.md)

---

Proviamo a creare delle espressioni in Python.

```bash
$ python3
```

```py
>>> 3 + 2
5
```

C'è una risposta, quindi l'interprete è riuscito a capire ciò che gli è stato chiesto. Proviamo con un'altra operazione:

```py
>>> 3 / 2
1.5
```

> [!WARNING]
> Nota bene: usando la versione 2 del linguaggio, l'operazione precedente avrebbe restituito `1` come risultato invece di `1.5`. Il motivo è che veniva eseguita un'operazione tra numeri interi ottenendo come risultato un intero a sua volta. Per ottenere il risultato esatto avremmo dovuto scrivere `3.0 / 2.0` in modo da effettuare un'operazione tra float.

> [!TIP]
> Ottenere un float quando si effettua una divisione tra interi non è un comportamento comune. Altri linguaggi molto popolari come C, C++ e Java restituiscono un numero intero.

> [!TIP]
> Sia quando scriviamo `3 / 2` che quando scriviamo `3.0 / 2.0`, il simbolo della divisione è sempre lo stesso.
> In altre parole il _significato_ del simbolo `/` _dipende dal tipo degli operandi_.

Un altro esempio, una "somma" tra stringhe, anche detta _concatenazione_:

```py
>>> 'a' + 'b'
'ab'
```

### Errori

Vediamo come reagisce l'interprete quando si commettono degli errori:

Errore di sintassi, manca l'operatore:

```py
>>> 3 2
...
Syntax Error: invalid syntax
```

Errore di grammatica:

```py
>>> 'a' + 3
...
TypeError: can only concatenate str (not "int") to str
```

---

Torna all'[indice](../toc.md)
