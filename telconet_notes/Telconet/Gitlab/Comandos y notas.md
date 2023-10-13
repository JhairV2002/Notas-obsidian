Las ramas solamente son **punteros** lo que en verdad se ramifica son los commits
![[Pasted image 20231011125953.png]]

para  ver las bifurcaciones de los commits esta el comando :

```bash
git log --all --oneline --graph
```

para posicionarnos en una nueva rama se utiliza

```bash
git checkout <rama>
```

para **mover** una rama (puntero) a cualquier punto de la historia (commit):

```bash
git reset --hard <id del commit o nombre de la rama>
```

antes de moverse con una rama a un commit se tiene que **guardar el id commit** anterior de donde apuntaba la rama o dejar una rama apuntando ahi estaticamente con (se tiene que estar en el commit de la rama):

```bash
git branch <Nombre de la rama>
```

**nota**: el head (puntero) tiene que estar en la rama que deseamos mover o bifurcar en todo momento 

para actualizar el repositorio local con el remoto 

```bash
git fetch origin
```

Push rama local al repositorio remoto 

```bash
git push -f origin <rama-local>:<rama-remota>
```

formato de los commits para ramas remotas

```bash
git commit -m ""
```

para quedarse con el ultimo commit hecho 

```bash
git reset soft
```