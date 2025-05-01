#

Torna all'[indice](../toc.md)

---

### Il programma minimo

Scrivere programmi in C richiede qualche attenzione in più rispetto al Python.
Per cominciare non si può semplicemente digitare una sequenza di istruzioni,
ma è necessario fare come segue:

```c
int main(void)
{
    // inserire qui le istruzioni
}
```

Al momento basta sapere solo alcune cose:

- Le istruzioni vanno inserite dopo la partentesi graffa aperta che segue `main()`
- Le istruzioni C terminano con il carattere `;`
- La sequenza di caratteri `//` inizia un commento che termina con la fine della linea

Nel codice precedente non c'è alcuna istruzione.

### Stampare una stringa

Le stringhe in C sono delimitate da virgolette doppie. Per stampare una stringa a
video si può usare la funzione `printf()` (attenzione alla f finale).

Quando si utilizza una funzione in C bisogna sempre accertarsi di aver incluso il
corrispondente _file di intestazione_. Nel caso della funzione `printf()` tale file si chiama
`stdio.h` (abbreviazione di standard input output).

Per farla breve, se si fa uso della funzione `printf()` bisogna inserire la riga:

```c
#include <stdio.h>
```

### Hello, World!

<script src="https://gist.github.com/FabioZTessitore/6c39070772280c27c51fdd4b591567e3.js"></script>

Il simbolo `\n` si legge _newline_ e ordina a `printf()` di andare a capo dopo aver stampato il messaggio `"Hello, World!"`.

Il linguaggio C non è interpretato come il Python, ma compilato. Questo significa che il
codice sorgente deve subire delle trasformazioni prima di diventare _eseguibile_ dalla macchina.
Il compilatore (`gcc`) esegue tutta una serie di passaggi, ma per i nostri scopi basteranno due comandi:

Compilazione (opzione `-c`) del file `hello.c` in codice oggetto;
ottiene come output (opzione `-o`) il file `hello.o`. Utilizza lo standard c11 del linguaggio.

```bash
$ gcc -std=c11 -c hello.c -o hello.o
```

Link (collegamento) della libreria standard C (quella che contiene il codice della funzione `printf()`);
ottiene come output l'eseguibile `hello`

```bash
$ gcc hello.o -o hello
```

A questo punto, se non ci sono stati errori, abbiamo ottenuto il file eseguibile `hello`
e possiamo mandarlo in esecuzione.

```bash
$ ./hello
Hello, World!
```

Notiamo quali permessi ha il file eseguibile:

```bash
$ ls -l hello
-rwxr-xr-x 1 fabio fabio 15960 mag 5 18:10 hello
```

Non stupirà vedere il permesso di esecuzione attivo, vero?

---

Torna all'[indice](../toc.md)
