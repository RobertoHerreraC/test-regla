# Git

## Flujo de Git
- Archivos y carpetas
- Stage o escenario
- Commits

## Comandos de configuarcion
> Mostrar y setear el valor de la informacion del usuario
```
  git config --global user.name [usuario]
  git config --global user.email [email]
```
> Crear alias para acortar de comandos
```
  git config --global alias.[nombrealias] "[comando expceto git]"
```

## Iniciar un repositorio local
>Crear un repositorio
```
  git init
```

## Verificacion de los estados del flujo del Git
Muestra el estado de los archivos
```
  git status
```
Variaciones:
- Muestra los archivos sin ninguna recomendacion y de manera comprimida
```
  git status -s
```
- Muestra los archivos sin ninguna recomendacion, de manera comprimida y con la rama actual
```
  git status -s -b
```

## Agrega un archivo para un commit o Stage.
>Agregar al limbo los archivos que van a recibir un `commit`
```
  git add [nombreArchivo] 
```
Variaciones:
- Agrega todos los archivos al Stage
```
  git add . 
```

>Para sacar el archivo en el estado de preparacion para un eventual `commit`
```
  git reset [nombreArchivo]
```
Variaciones:
> Quita todos los archivos del estado de preparación
```
  git reset .
```
```
  git reset HEAD .
```
-> HEAD es el punto donde se encuentra
>Para borrar un archivo de **proyecto local**. (Comando de bash)
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
  git commit -m "[aqui va la descripcion]"
```
>Para agregar todo los archivos al estado de preparacion y establecer un `commit` a la vez.
Se omite el `git add .`
```
  git commit -am "[aqui va la descripcion]"
```
>Para deshacer el ultimo `commit`, dejandolo en el estado stage y con los cambios guardados
```
  git reset --soft HEAD~1
```
>Para deshacer el ultimo `commit`, dejandolo en el estado de directorio y con los cambios actuales no guardados.
```
  git reset HEAD^
```

>Para corregir el ultimo `commit`
```
  git commit --amend -m "[contenido arreglado]"
```
Tener cuidado de hacer este `commit` puede generar conflicto con el repositorio que tiene otras personas.

## Etiquetar Commit
> Crear el tag en el proyecto, lo asigna al ultimo commit
```
  git tag [nombre_tag]
```
Variaciones:
- Agregar una etiqueta con descripcion
```
  git tag -a [nombre_tag] -m "[descripcion]"
```
- Agregar una etiqueta a un commit especifico
```
  git tag -a [nombre_tag] [idHash] -m "[descripcion]"
```
> Eliminar el tag
```
  git tag -d [nombre_tag]
```
> Mostrar informacion del tag
```
  git show [nombre_tag]
```
## Diferencias
Revisar diferencias entre versiones.

Entre el actual y el commit del hash asignado
```
  git diff [hash]
```
Entre el estado actual de archivo o directorio(no en el estado Stage) y el ultimo commit
```
  git diff
```
Eliminar cambios en el estado de archivo (en el ultimo commit)
```
  git checkout -- [archivo.ext]
```

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
> Numero de linea que se editaron, cuales fueron los cambios a nivel de archivo
```
  git log --stat 
```
> Muestra los cambios y cuales fueron los cambios a nivel de código
```
  git log -p 
```
Agrupa los commits que ha realizado cada usuario
```
  git shortlog
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


