# Struttura di una pagina HTML

Torna all'[indice](../toc.md)

---

Con la nascita e lo sviluppo di Internet è nata la necessità di scambiarsi documenti in rete. Nasceva così, nei laboratori del CERN,
il linguaggio HTML e con esso il Web. Per visualizzare un documento HTML utilizziamo programmi chiamati browser.
I browser parlano con i server web tramite Internet per accedere e rendere visibili i documenti.

L'HTML definisce la sintassi di elementi particolari che non verranno visualizzati dal browser, ma indicheranno come mostrare il contenuto.
Quindi la prima cosa da capire e su cui sperimentare è che una pagina HTML non è niente altro che un file di testo semplice.

Proviamo, allora, a creare una semplice pagina Web. Apriamo un editor di testi e digitiamo come nell'esempio:

```html
<!-- index.html -->

Benvenuto nella mia Home Page Qui puoi trovare tutte le informazioni che cerchi
...
```

Salviamo il file con il nome `index.html` e apriamo la pagina con un browser. Ci sono differenze tra quello che abbiamo scritto e quello che viene visualizzato?

### I tag

Il browser visualizza il testo, ma non rispetta gli spazi e gli a capo. Infatti, l'`HTML` è un linguaggio di _markup_, il che significa che il contenuto delle pagine viene _etichettato_ per ottenere _elementi_.
Un elemento è composto da un _tag di apertura_, dal contenuto e da un _tag di chiusura_.

Per esempio, per creare un paragrafo, si usa il tag `p`. Il tag di apertura sarà `<p>`, quello di chiusura `</p>`.

```html
<p>Un paragrafo</p>
```

Si possono anche inserire commenti: `<!-- questo e' un commento -->`.

Modifichiamo, quindi, il file `index.html` in questo modo:

```html
<!-- index.html -->

<!-- la mia prima pagina Web -->

<p>Benvenuto nella mia Home Page</p>

<p>Qui puoi trovare tutte le informazioni che cerchi ...</p>
```

Adesso il browser visualizzerà correttamente.

### Nidificare i tag

Un elemento può essere incluso all'interno di un altro elemento prestando attenzione a chiudere prima quello interno e poi quello esterno.
Ad esempio, `em` serve a mettere in evidenza una porzione di testo e può naturalmente essere utilizzato all'interno di un paragrafo.

```html
<p>Il linguaggio HTML <em>non</em> sembra difficile.</p>
```

### Gli attributi

Spesso i tag sono completati da _attributi_ che ne specificano il comportamento o il significato. Si inseriscono all'interno del tag di apertura nella forma `attributo="valore"`. Per esempio, l'attributo `name`, come si può ben immaginare, permette di assegnare un nome all'elemento.

```html
<p name="traduttore">Tradotto da ...</p>
```

### Una pagina completa

Anche se è semplice iniziare a scrivere pagine Web, per creare correttamente un file HTML bisogna aggiungere alcuni elementi. Innanzitutto la pagina deve essere racchiusa all'interno del tag `<html>`,
il quale a sua volta specifica in quale lingua è scritto il documento mediante l'attributo `lang`.

```html
<html lang="it">
  <!-- pagina qui -->
</html>
```

All'interno di `<html>` troviamo due parti: `<head>` e `<body>`.

`head` contiene informazioni _riguardanti_ il documento.

`body` contiene _il documento_ stesso.

```html
<html lang="it">
  <head>
    <!-- informazioni riguardanti il documento -->
  </head>

  <body>
    <!-- il documento stesso -->
  </body>
</html>
```

Una cosa molto importante è iniziare il documento con il `doctype`. Non è un tag, serve ad indicare al browser la versione di HTML utilizzata. Per il Web moderno, utilizzando l'_HTML5_, scriveremo:

```html
<!DOCTYPE html>
```

Ecco la pagina completa:

```html
<!DOCTYPE html>

<!-- La pagina e' composta da un unico elemento html -->
<html lang="it">
  <!-- Ogni pagina e' composta da due sezioni: head e body
    
        In head trovano posto le informazioni riguardanti il documento.
        In body trova posto il documento stesso.
    -->

  <head>
    <!-- indica al browser il set di caratteri -->
    <meta charset="utf-8" />

    <!-- titolo del documento -->
    <title>La mia prima pagina completa</title>
  </head>

  <body>
    <p>Benvenuto nella mia Home Page</p>

    <p>Qui puoi trovare tutte le informazioni che cerchi ...</p>
  </body>
</html>
```

### Suggerimenti

Quando si scrivono pagine di esempio si avrà bisogno di inserire testo e immagini di prova. Per non lavorare di fantasia esistono strumenti e siti web che aiutano a semplificare il lavoro.

Lavorando con Visual Studio Code, quando si digita la parola _lorem_ viene generato un paragrafo di testo senza senso. In alternativa si può accedere al sito [Lorem Ipsum](http://it.lipsum.com/). Bisogna solo selezionare quanti paragrafi vogliamo e verrà generato il testo. Un copia e incolla e avremo siti pieni di contenuto (fasullo!).

L'altro sito, [Lorem Picsum](https://picsum.photos/), riguarda invece le immagini. Non c'è neanche bisogno di accedere al sito stesso, basterà mettere l'indirizzo al posto della URL dell'immagine e il gioco è fatto. Se, per esempio, si ha bisogno di un'immagine di 320x200 pixel si può scrivere una cosa del tipo:

```html
<img src="https://picsum.photos/320/200" />
```

### Letture

> [!TIP]
> C. Musciano, B. Kennedy, _HTML & XHTML, The Definitive Guide_, O'Reilly, 2006, 6th ed
>
> - Chap 1: HTML, XHTML, and the World Wide Web
> - Chap 2: Quick Start
> - Chap 3: Anatomy of an HTML Document

---

Torna all'[indice](../toc.md)
