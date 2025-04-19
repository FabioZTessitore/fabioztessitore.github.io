# Cercare nei file

Torna all'[indice](../toc.md)

---

A volte c'è bisogno non di cercare un particolare file, ma di cercare del testo
all'interno di un file o di un gruppo di file. A questo scopo si usa il comando `grep`.

```bash
$ grep PS1 ~/.bashrc # Cerca la stringa PS1 in $HOME/.bashrc
```

Ovviamente `grep` può essere usato mediante pipe per fare ricerche sullo standard
output. Immaginiamo, per esempio, un comando che restituisce molto testo e di essere
interessati solo alle linee contenenti certe parole.

```bash
$ history | grep git # Cerca i comandi git nello storico
```

`grep` è corredato di tante opzioni utili:

- `-i` ignora maiuscole e minuscole;
- `-v` mostra solo le righe che _non_ contengono il testo;
- `-r` ricerca ricorsiva nella directory;
- `-l` (usato con -r) mostra solo i nomi dei file in cui è presente il testo;
- `--color` colora le parole cercate.

---

Torna all'[indice](../toc.md)
