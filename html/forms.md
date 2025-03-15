# I Form

Torna all'[indice](../toc.md)

---

I form, o moduli, sono utilizzati per raccogliere dati dagli utenti. Un esempio di utilizzo classico è quello
di creare interfacce per le applicazioni web. Importante premessa da fare, al momento non saranno molto utili
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

Per l'attributo `type` abbiamo a disposizione i valori: `text`, `password`, `checkbox`, `radio`, `submit`.

Altri elementi importanti sono `textbox` per creare caselle di testo multilinea e `select` per creare
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

### Letture

<!-- > [!TIP]
> C. Musciano, B. Kennedy, _HTML & XHTML, The Definitive Guide_, O'Reilly, 2006, 6th ed
>
> - Chap 4: Text Basics
> - Chap 5: Rules, Images, and Multimedia -->

> [!TIP] > _HTML Dog_, [www.htmldog.com](https://www.htmldog.com/)
>
> HTML Tutorial
>
> - [Forms](https://www.htmldog.com/guides/html/beginner/forms/)

---

Torna all'[indice](../toc.md)
