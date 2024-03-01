# Un semplice modello di collaborazione

Torna all'[indice](../toc.md)

---

Se è stato aggiunto qualche collaboratore esperto alla repository, anche questi potrà effettuare modifiche ai file. Per questa ragione può accadere che i file locali non siano aggiornati. In altre parole, prima di iniziare ad effettuare modifiche bisogna sempre scaricare la versione aggiornata con:

```bash
$ cd ~/test # assicuriamoci di essere nella directory giusta
$ git pull origin main
```

Quindi lo schema di lavoro diventa:

---

| Passo | Nome Operazione   | Comando                                |
| :---: | ----------------- | -------------------------------------- |
|   1   | pull              | `git pull origin main`                 |
|   2   | modifica dei file | `vim ...`                              |
|   3   | stage dei file    | `git add lista_dei_file_modificati`    |
|   4   | commit            | `git commit -m "descrizione modifica"` |
|   5   | push              | `git push origin main`                 |

---

Torna all'[indice](../toc.md)
