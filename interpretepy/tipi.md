# Tipi elementari

Torna all'[indice](../toc.md)

---

Il primo linguaggio in cui scriveremo sarà il _Python_.

> [!INFO]
> D'ora in avanti, salvo diversamente specificato, ci si riferirà alla versione 3 del linguaggio

Si tratta di un linguaggio _interpretato_. In altre parole esiste un programma, chiamato _interprete_, che legge le istruzioni e cerca di eseguirle.

Da terminale lanciamo l'interprete:

```bash
$ python3
```

Proviamo a scrivere un numero:

```py
>>> 3
3
```

L'interprete legge il carattere che abbiamo digitato, il `3`, lo interpreta e risponde con il **valore** `3`.

Di che tipo è tale valore?

```py
>>> type(3)
<class 'int'>
```

L'interprete ci dice di che **tipo** è il **valore** `3`. Risponde che si tratta di un `int`, un _valore intero_.

Tentiamo qualcosa di diverso:

```py
>>> type(3.2)
<class 'float'>
```

`3.2`, invece, viene considerato `float`, un valore in _virgola mobile_ (_floating point_).

```py
>>> type(3.0)
<class 'float'>
```

Da notare che `3` e `3.0` sono diversi!

Il tipo booleano (Vero o Falso, **True** o **False**):

```py
>>> type(True)
<class 'bool'>

>>> type(False)
<class 'bool'>
```

Il tipo stringa:

```py
>>> type('a')
<class 'str'>

>>> type('123')
<class 'str'>
```

Il tipo nullo:

```py
>>> type(None)
<class 'NoneType'>
```

### Conversioni di tipo (_cast_)

Molto più spesso di quanto si possa immaginare sarà necessario convertire valori da un tipo ad un altro. Tale operazione prende il nome di _cast_.

Converte il numero intero `3` in una stringa:

```py
>>> str(3)
'3'
```

Converte la stringa `'3'` nel numero intero `3`:

```py
>>> int('3')
3
```

Ma non tutto è possibile. Nell'esempio seguente l'interprete non sa come effettuare la conversione e restituisce un errore:

```py
>>> int('2.1')
...
ValueError: invalid literal for int() with base 10: '2.1'
```

Ora invece si!

```py
>>> float('2.1')
2.1
```

Infine, per uscire dall'interprete, premere `CTRL D`.

---

Torna all'[indice](../toc.md)
