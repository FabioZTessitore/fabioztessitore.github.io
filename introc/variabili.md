# Le variabili

Torna all'[indice](../toc.md)

---

Abbiamo già visto cosa sono e come si usano le variabili in Python.
In C, prima di poter utilizzare una variabile, bisogna _dichiararla_. Una dichiarazione
di variabile è una riga del tipo:

```c
int numero; // dichiarazione di una variabile intera
```

Come si può vedere è necessario specificare il tipo e il nome della variabile nella dichiarazione.

Da questo momento in poi si può utilizzare la variabile `numero`:

```c
numero = 42;
```

Una buona abitudine è quella di dichiarare e contemporaneamente inizializzare una variabile:

```c
int numero = 42;
```

### I tipi fondamentali

Oltre alle variabili intere ci sono quelle in virgola mobile (floating point).
In C ne esistono due tipi: `float` (singola precisione) e `double` (doppia precisione).
Per il momento si consiglia di usare variabili `double`.

### Stampare una variabile

Per stampare il valore di una variabile bisogna usare `printf()`, ma la cosa non è intuitiva.
Si deve, infatti, utilizzare la _specifica di stampa_: un codice che dipende dal _tipo_
della variabile da stampare. Ad esempio, per stampare variabili intere la specifica di
stampa è `%d` e la `printf()` si usa in questo modo:

```c
printf("La variabile numero vale %d\n", numero);
```

Avevamo già visto un esempio del genere quando abbiamo stampato
un saluto. In quel caso il valore da stampare era una stringa
e la specifica di stampa `%s`.

```c
printf("%s\n", "Hello, World!");
```

### Esempio completo

<script src="https://gist.github.com/FabioZTessitore/2bca0e092b5f5565fe9b9cf883a8e6e6.js"></script>

### Dimensione di una variabile (operatore `sizeof`)

Il linguaggio C è certamente più complesso del Python, ma permette un punto di vista
_più vicino alla macchina_. L'operatore `sizeof`, ad esempio, restituisce la dimensione,
in _byte_, di una variabile o tipo:

<script src="https://gist.github.com/FabioZTessitore/9a24b6617c0ac7edfa3352938e68d361.js"></script>

> [!WARNING]
> Ogni macchina (insieme di hardware, sistema operativo e compilatore)
> ha le sue caratteristiche e per questa ragione bisogna fare attenzione.
> Se sulla nostra macchina gli interi hanno lunghezza 4 byte, non possiamo pretendere
> che il programma funzioni correttamente su una macchina con interi a 2 byte.

Nel file di intestazione `limits.h` trovi i valori minimo e massimo ammissibili.

<script src="https://gist.github.com/FabioZTessitore/6830ff40d4ae3ab5c02ebde2a5146cbf.js"></script>

### Indirizzo di una variabile (operatore `&`)

Il C permette di ottenere l'indirizzo in memoria di una variabile in maniera semplice.
Non bisogna fare altro che far precedere il nome della variabile stessa dal simbolo `&`.
Poi nella stampa si usa la specifica di stampa `%p`.

<script src="https://gist.github.com/FabioZTessitore/bac593d439850bca04ef7f89d468da19.js"></script>

---

Torna all'[indice](../toc.md)
