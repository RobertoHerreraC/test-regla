# Git
## Agrega un archivo para un commit.
>Agregar al limbo los archivos que van a recibir un `commit`
```
  git add [nombreArchivo] 
```
>Para sacar el archivo en el estado de preparacion para un eventual `commit`
```
  git reset [nombreArchivo]
```
>Para borrar un archivo de **proyecto**. (Comando de bash)
```
  rm [nombreArchivo]
```
>Para borrarlo del repositorio. Es necesario en el caso se borre un archivo en la carpeta del proyecto.
```
  git rm [nombreArchivo] 
```
## Commit
>Especificar los guardados de los archivos en los estados de preparacion del repositorio.
```
  git commit 
```
Se abre un editor para escribir la descripcion del `commit`
>Para hacerlo de manera corrida.
```
  git commit -m '[aqui va la descripcion]'
```
>Para deshacer el ultimo `commit`
```
  git reset --soft HEAD~1
```
## Banch
>Agrega una rama en el proyecto.


#GitHub


