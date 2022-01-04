# Clase 01 - GIT

## Markdown (archivo.md)

https://www.markdownguide.org/cheat-sheet/

## Saber si tengo git instalado

**Nota:** ` = backtick => ALT + 96 

```sh
git --version
```
### Configuración inicial de GIT

#### Configuro el usuario 

```sh
git config user.name "Maxi"
```

#### Configuro el mail 
```sh
git config user.email "mlapeducacionit@gmail.com"
```

### Listo las configuración del usuario
```sh
git config --get-regexp user
```

## Comando de consola

### Limpio la consola

```sh
clear
```
### Ingreso a un directorio

```sh
cd <directorio>
```

### Retrocedo directorio

```sh
cd ..
```

### Listar archivos en cosola

```sh
ls -la
```

### Para saber lo que está pasando en el WD 
Comparar el WD con el último commit

```sh
git status
```

### Paso del Working Directory (WD) al Index (staged)
**IMPORTANTE:** Cuidado es case sensitive

```sh
git add <nombreArchivo> 
```

Ej:

```sh
git add README.md 
```
### Pasar del WD al INDEX más de un archivo
```sh
git add .
```


### Para pasar del INDEX al REPOSITORIO LOCAL

```sh
git commit -m <mensaje>
```
Ej:

```sh
git commit -m "Agrego el archivo README.md"
```

### GIT LOG

```sh
git log 
```
### 

```sh
git log --online
```

### PASOS para subir mi repo local al remoto

1. git init
2. git add README.md
3. git commit -m "first commit"
4. git remote add origin https://github.com/<tuNombreUsuario>/<tuRepo>
5. git push -u origin master