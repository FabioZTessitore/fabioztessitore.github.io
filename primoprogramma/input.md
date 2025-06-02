# Input da tastiera

Torna all'[indice](../toc.md)

---

### La funzione `input()`

Per fare qualche programmino utile, anche se ancora molto semplice,
bisogna essere in grado di ottenere dei valori dall'utente mediante tastiera.

<script src="https://gist.github.com/FabioZTessitore/a2b78a2570a71562a570e00fd49f177f.js"></script>

La riga chiave è la 6, quella contenente `input()`. Si tratta di una _funzione_ messa a disposizione
dal linguaggio Python. Quando l'interprete la incontra, ferma l'esecuzione del programma e resta in
attesa che l'utente digiti qualcosa tramite tastiera. Tutto ciò che viene digitato (una stringa)
viene quindi etichettato con `name` (creazione della variabile) e può essere stampato con `print()`.

Nell'esempio è mostrato anche come eseguire una stampa formattata!

```bash
$ python3 name.py
Come ti chiami?
Marco
Ciao Marco
```

#### `input()` e il prompt

Prima di chiedere input all'utente è sempre buona norma stampare un messaggio
per specificare cosa il programma si aspetta. Tale messaggio è detto anche
_prompt_ (come il prompt dei comandi). Siccome aggiungere un prompt è un'operazione comune,
la funzione `input()` può anche essere invocata come in questo altro esempio:

<script src="https://gist.github.com/FabioZTessitore/1a1dfe90bfcf959ad395e8d1580032f3.js"></script>

---

Torna all'[indice](../toc.md)
