# Comandi in background

Torna all'[indice](../toc.md)

---

A volte, dopo aver lanciato un comando, il terminale non è più disponibile
per un certo tempo. Può succedere perché il comando impiega tempo per portare
a termine il proprio lavoro oppure perché apre una finestra. In tutti questi
casi la shell resta occupata e non è possibile lanciare altri comandi.
L'operatore `&` permette di lanciare un comando in _background_ così da
avere sempre la shell libera. Proviamo:

```bash
$ gnome-text-edit &
```

Per far ritornare in primo piano (_foreground_) il comando lanciato precedentemente in background si usa `fg`.

```bash
$ fg
```

---

Torna all'[indice](../toc.md)
