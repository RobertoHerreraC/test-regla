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
Se omite el `git add .`
```
  git commit -am '[aqui va la descripcion]'
```
>Para deshacer el ultimo `commit`
```
  git reset --soft HEAD~1
```
>Para corregir el ultimo `commit`
```
  git commit --amend
```
Tener cuidado de hacer este `commit` puede generar conflicto con el repositorio que tiene otras personas.
## Remote
>Es un servidor remoto para conectar con el repositorio.
>Agrega un remoto asociado a una URL de github
```
  git remote add [nombre-remoto] [url-github]
```
>Ver los remotos
```
  git remote 
```
>Ver los remotos con las url
```
  git remote -v
```
>Eliminar un remoto asociado a una URL de github
```
  git remote rm [nombre-remoto]
```
## Clonar
Obtener un proyecto desde un repositorio remoto
```
  git clone [url-remoto]
```
Obtener un proyecto desde un repositorio remoto de una rama especifica
```
  git clone -b [nom_branch] [url-remoto]
```
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
>Muestra el historial del repositorio con alguna info
```
  git log --decorate
```
>Muestra el historial del repositorio con grafico, con alguna info
```
  git log --graph --decorate
```
>Muestra el historial del repositorio con grafico, con info y en una linea
```
  git log --graph --decorate --oneline -all
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
>Para crear y cambiar de rama
```
  git checkout -b [nombre-rama]
```
>Eliminar rama que ha sido mezclada
```
  git branch -d [nombre-rama]
```
>Eliminar rama si importar que la rama no este merge con la rama actual
```
  git branch -D [nombre-rama]
```
Se pierde archivo o modificaciones de la rama a borrar.
## Fusion de ramas
Junta las ramas
```
   git merge [rama-destino]
```
>Aborta la fusion en un estado de conflicto
```
  git merge --abort
```
Los rama donde se esta, se ve aplicada a la rama de desctino.
---
>Para limpiar los historiales basura del repositorio
```
  git gc
```
# GitHub


