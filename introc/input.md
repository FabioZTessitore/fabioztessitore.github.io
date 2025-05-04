# Input da tastiera

Torna all'[indice](../toc.md)

---

Per ottenere input da tastiera utilizziamo la funzione `scanf()`.

<script src="https://gist.github.com/FabioZTessitore/8ae25c2eb4af2d3e1a03d2979a4d0b9f.js"></script>

Potrebbe sembrare strano che, per avere input da tastiera chiamando la funzione `scanf()`,
si debba passarle una stringa con la specifica di stampa. In effetti, pensandoci bene,
stiamo dicendo cosa ci si aspetta in input. Mettendo `%d` diciamo che ci aspettiamo un intero.

Come sappiamo `&` serve a ottenere l'indirizzo di una variabile.
Negli esempi con `printf()` abbiamo effettuato delle stampe di questi valori; qui, invece,
l'indirizzo di `age` viene usato dalla funzione `scanf()` per sapere
dove memorizzare il valore letto in input.

---

Torna all'[indice](../toc.md)
