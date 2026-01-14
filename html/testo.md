# Gestione del testo

Torna all'[indice](../toc.md)

---

### Suddividere il testo in sezioni

Sappiamo già che se vogliamo strutturare il testo in paragrafi dobbiamo utilizzare
il tag `p`. Più paragrafi in relazione tra loro possono essere raggruppati mediante
il tag `div`. Inizialmente nato come strumento per organizzare il testo in sezioni
distinte, può essere utile per impostare alcune proprietà che i vari paragrafi hanno in
comune, come, ad esempio, il colore, l'allineamento e così via.

```html
<!-- alcuni paragrafi correlati tra loro -->
<div>
  <p>
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Expedita aut nam
    maxime, blanditiis officia quisquam quidem? Sapiente excepturi reiciendis
    dicta dolores quae officiis ipsam, optio fugiat? Quisquam quae unde fugiat.
  </p>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque nostrum
    libero velit. Reprehenderit, distinctio culpa asperiores possimus unde,
    blanditiis aliquid sapiente voluptate odit qui, cupiditate illum animi
    dolorum sequi molestias!
  </p>
</div>
```

### Le intestazioni

Per spezzare un lungo testo in sezioni più piccole esistono sei livelli di
intestazione, corrispondenti ai tag `h1`, `h2`, `h3`, `h4`, `h5`, `h6`.

```html
<h1>Intestazione di primo livello</h1>

<h2>Intestazione di secondo livello</h2>
<p>Testo</p>

<h2>Un'altra intestazione di secondo livello</h2>
<p>Altro testo</p>
```

---

Torna all'[indice](../toc.md)
