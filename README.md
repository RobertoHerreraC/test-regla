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
>Para agregar todo los archivos al estado de preparacion y establecer un `commit` a la vez.
```
  git commit -am '[aqui va la descripcion]'
```
>Para deshacer el ultimo `commit`
```
  git reset --soft HEAD~1
```
## Remote
Es un servidor remoto para conectar con el repositorio.
## Push
>Proceso de subir archivo al repositorio.
```
  git push [remote] [rama] 
```
## Pull (sincronizacion)
>Actualizar los archivos locales con el repositorio online.
```
  git pull [remote] [rama]
```
## Historial
>Muestra el historial del repositorio
```
  git log
```
## Banch (ramas)
>Agrega una rama en el repositorio.
>Mostrar lista de ramas.
```
  git branch
```
>Agrega una rama
```
  git branch [nombre-rama]
```
>Cambiar de rama
```
  git checkout [nombre-rama]
```

#GitHub


