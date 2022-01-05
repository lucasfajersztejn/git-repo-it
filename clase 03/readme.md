# Clase 03 - GIT

## Repaso de Branch

### Listo ramas

```sh
git branch
```

### Creo una rama

```sh
git branch <nombreRama>
```

### Cambio entre ramas

```sh
git switch <nombreRama>
```

### Subir rama local al remoto

```sh
git push origin <nombreRama>
```

Ej:

```sh
git push origin clase03
```

## Git Merge

### Tipos de Merge

Fast-Forward (No hay ningun cambio que se solape con lo que esta en la otra rama)

Fast-Forward - Unión automáticas (No hay ningun cambio que se solape con lo que esta en la otra rama)

Recursiva -  Uniones automáticas (No hay colisiones de cambios)

Manual - Conflictos (ocure cuando hay modificaciones en las mismas líneas)

### Abortar Merge

```sh
git merge --abort
```
### TAREAS: Agrego cosas que quiero tener en consideración.

* Tener en cuenta subir una rama al remoto
* Ver Clone
* Ver Fork

## ALIAS

### ¿Cómo creo un alias?

```sh
git config alias.lg "log --oneline --decorate --all --graph"
git config alias.l "log --oneline"
git config alias.s "status --short"
```

### Para editar el archivo de configuración de GIT

```sh
git config -e
```

### Para eliminar un alias

```sh
git config --unset alias.s
```

# Git Clone
Me permite clonar cualquier repositorio que exista en GitHub, GitLab, etc

## Lo clona en la carpeta con el nombre react

```shh
git clone https://github.com/facebook/react.git
```

## Clona en una carpeta en especifico

```shh
git clone https://github.com/facebook/react.git <nombreCarpeta>
```

# GIT PULL
Trae todos los cambios que hubieran surgido durante el día

```sh
git pull
```


# Fork
Me permite crear un repo en mi cuenta de cualquier proyecto de Github

1. Vamos al repo que queremos hacer el fork. Presionamos el botón.
2. Se crear el repo en mi cuenta.
3. Puedo clonar ese repo y empezar a trabajar.


# Para actualizar un Fork
Necesito el remoto original. Del remoto del repo al cual le hice el fork

## Agrego el remoto del repositorio original

```sh
git remote add upstream <urlRemotoOriginal>
```

## Me traigo los últimos commit de el repo original

```sh
git pull upstream <urlRemotoOriginal>
```

# TAREA

1. Hacen un fork de nuestro repo. https://github.com/mlapeducacionit/git-repo-it.git
2. Clonan su fork que está en su cuenta. https://github.com/<repoUstedes>/git-repo-it.git

```sh
git clone https://github.com/<usuario>/git-repo-it.git
```

3. Hacen commit, trabajan con el repo localmente. Suben commit. Y luego hacen el Pull Request.

# GIT STASH
Es una pila de almacenamiento que provee GIT. Permite registrar temporalmente los cambios del WORKING DIRECTORY para seguir trabajando. Cuando hacemos un stash se reestrablece el proyecto al último commit.
## Crea el stash
Guarda los cambios que están en el WD, en un area temporal. 
```sh
git stash
```
## Listo los stash

```sh
git stash list
```

## Para recuperar el stash
Lo que hace este comando es recuperar el último stash y si no hay conflicto borra el stash
```sh
git stash pop
```
## Para recuperar el stash sin borrarlo
```sh
git stash apply stash@{1}
```

## Para borrar el stash
```sh
git stash drop stash@{1}
```
