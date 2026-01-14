# Tag semantici

Torna all'[indice](../toc.md)

---

Quando si struttura un documento, le intestazioni permettono di creare nuove sezioni
e fanno bene il loro lavoro. Esse, però, suddividono il documento in parti, ma non
raggruppano le stesse. Si immagini, ad esempio, il caso in cui più paragrafi o un'intera
sezione debbano avere un certo colore di sfondo. Si potrebbero utilizzare degli
elementi `div` (e spesso faremo così), ma volendo esistono altri elementi che sono
più ricchi di significato.

Un `article` è un elemento che contiene una sezione del documento a se stante.

Una `section` è una parte più generale del documento. Può servire per dividere un
articolo in più parti ad esempio.

Al contrario dei `div`, questi elementi possono essere utilizzati anche se non è necessario
avere più stili. Permettono di strutturare meglio il nostro documento a prescindere
dalla visualizzazione grafica.

Altri elementi semantici sono `header` e `footer` specializzati per intestazione e pie' di pagina.

`aside` permette l'inserimento di una parte che in qualche modo è correlata al resto
del documento senza farne necessariamente parte.

Altri due tag semantici molto importanti sono `figure` (insieme a `figcaption`) e `nav`.
Il primo permette di inserire un'immagine con didascalia, il secondo un menu di
navigazione. Essendo elementi che ricorrono spesso se ne riporta un esempio:

```html
<figure>
  <img src="nomefile.jpg" />
  <figcaption>Didascalia dell'immagine</figcaption>
</figure>
```

```html
<nav>
  <ul>
    <li><a href="/home">Home</a></li>
    <li><a href="/tutorial">Tutorial</a></li>
    <li><a href="/about">About</a></li>
  </ul>
</nav>
```

---

Torna all'[indice](../toc.md)
