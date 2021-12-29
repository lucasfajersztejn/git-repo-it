# Clase 02 - GIT

## GIT LOG

### Muestra los commits
```sh
git log
```
**NOTA:** Para salir es con la letra **q**


### Muestra los commits en forma abreviada
```sh
git log --oneline
```
### Por fecha

```sh
git log --since="2021-12-20" 
git log --after="2021-12-20" 
git log --before="2021-12-27"
git log --after="2021-12-20" --before="2021-12-27"
```
### Muestra la cantidad de commits elegidos. 

Ejemplo: 2 commits

```sh
git log -2 # cantidad de commits que va a mostrar el git log
```

```sh
git log --oneline --decorate --all --graph
```

### GIT IGNORE
Sirve para ignorar archivos que no quiero seguir.

Creo el archivo **.gitignore** en el directorio raíz y dentro coloco el nombre del arhivo o la carpeta que no quiero seguir. 


### GIT KEEP
Me permite seguir una carpeta vacia.

Creo un archivo llamado **.gitkeep** que lo hace es tener en cuenta la carpeta vacia

### IMPORTANTE: Forma corta de hacer un git add y un git commit.
**NOTA:** Tengo que tener todos los archivos seguidos. Si tengo alguno untracked, esos archivos no se van commitear

```sh
git commit -am "mensaje commit"
```

### REMOTE

#### Lista alias de remotos
```sh
git remote
```
#### Lista alias de remotos y urls
```sh
git remote -v
```

#### Agrego remoto a mi REPO
```sh
git remote add <nombre-alias> <url-repo>
```

#### Renombra el alias de la URL del remoto
```sh
git remote rename <nombre-antiguo> <nombre-nuevo>
```

#### Borrar remoto
```sh
git remote rm <alias-del-remoto>
```

Ej:

```sh
git remote rm origin
```

#### Forma corta de hacer un status y ver los cambios en WD (Working Directory)

```sh
git status --short
```

## RAMAS (BRACHES)

### Para listar las ramas
```sh
git branch
```
### Para crear una rama
```sh
git branch <nombre-rama>
```

### Para cambiar de rama
```sh
git switch <nombre-rama>
```

### Para borrar una rama
```sh
git branch -d <nombre-rama>
```

### Para forzar el borrado de una rama que no haya sido unificada con otra

```sh
git branch -D <nombre-rama>
```

### Para crear una nueva y moverme a esa rama
```sh
git checkout -b <nombre-rama>
```