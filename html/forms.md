# I Form

Torna all'[indice](../toc.md)

---

I form, o moduli, sono utilizzati per raccogliere dati dagli utenti. Un esempio di utilizzo classico è quello
della creazione di interfacce per le applicazioni web. Importante premessa da fare: al momento non saranno molto utili
perché per poter funzionare devono essere integrati con un linguaggio di programmazione che possa elaborare
le informazioni.

Per creare un form si utilizza l'apposito tag `form`.

```html
<form action="" method="">
  <!-- elementi del form qui -->
</form>
```

L'elemento più importante che può essere aggiunto in un form è certamente l'elemento `input` nella forma:

```html
<input type="" name="" value="" />
```

Per l'attributo `type` abbiamo a disposizione, tra gli altri, i valori: `text`, `password`, `checkbox`, `radio`, `submit`.

Altri elementi importanti sono `textarea` per creare caselle di testo multilinea e `select` per creare
caselle a discesa.

```html
<textarea name="">
    Contenuto qui
</textarea>

<select name="">
  <option value="">...</option>
  <option value="">...</option>
  <option value="">...</option>
  <option value="">...</option>
  ...
</select>
```

---

Torna all'[indice](../toc.md)
