# La conoscenza

Torna all'[indice](../toc.md)

---

La conoscenza si divide in due grosse categorie: _dichiarativa_ e _imperativa_.

### La conoscenza dichiarativa

Probabilmente è nota la seguente definizione:

> `y` è la radice di `x` se `y * y = x`

Se, ad esempio, `x` vale 25 e `y` vale 5, sappiamo che `y` è radice di `x` perché `5 * 5 = 25`.

Questo tipo di conoscenza è utile per fare dei controlli, ma non ci aiuta a trovare la soluzione al problema. Se non conosciamo la radice di un numero, come facciamo a trovarla?

### La conoscenza imperativa

Carta e penna alla mano, proviamo a fare queste operazioni (con `x = 25` ad esempio):

1. scegliamo un numero `g` a caso (diverso da 0);
1. calcoliamo `g * g` e se il risultato non è "abbastanza vicino" a `x` andiamo al prossimo punto;
1. calcoliamo `g = (g + x/g) / 2`;
1. torniamo al punto 2.

Quello che abbiamo eseguito è un _algoritmo_ per il calcolo della radice quadrata di un numero.

Approfittando del fatto che i computer sono molto bravi a fare calcoli velocemente, possiamo usare gli algoritmi per avere risposte alle nostre domande.

Alcune caratteristiche degli algoritmi sono:

- devono convergere (arrivare ad un risultato);
- sono composti da istruzioni;
- e da controlli sul flusso delle istruzioni ("se ... allora ...");
- hanno una condizione di terminazione ("se abbastanza vicino").

> [!DANGER]
> Bisogna fare molta attenzione quando si scrivono algoritmi, o codice in generale. Il bello, e il brutto, della programmazione è che un computer fa **esattamente** quello che gli viene chiesto di fare!

---

Torna all'[indice](../toc.md)
