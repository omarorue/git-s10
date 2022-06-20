# Git Desarrollo Colaborativo

Esto es un guia creada con la finalidad de facilitar el entendimiento y aplicacion de la herramienta conocida como GIT, que se utiliza para el control de versiones de nuestros proyectos. Aqui veremos como configurar la misma, asi como tambien, cada una de sus opciones.

## Configuracion Inicial

Cuando inicializamos un repositorio por primera vez, podemos establecer el nombre de usario y correo electronico, para identificarnos dentro del historial de cambios. 

Cuando queremos definir una configuracion de manera general, debemos utilizar el parametro *--global* para indicar que dicha configuracion debe almacenarce en la carpeta del usuario y no en la carpeta *.git/* del repositorio.

* **git init**: inicializa un repositorio de git.
* **git config --global user.name** 'username': define el nombre del usuario para el control de cambios.
* **git config --globla user.email** 'email': establece el correo electronico para las confirmaciones. 

## Gestion del proyecto

Para sincronizar los cambios realizados en el proyecto, debemos tener en cuenta que si creamos en nuestra computadora el mismo utilizando el comando *git init*, vamos a tener que crearlo tambien en nuestro servidor remoto, como por ejemplo:
[Github] (https://github.com)

En caso que ya exista un repositorio remoto, simplemente debemos descargar el historial del mismo, pero indistintamente de como hayamos empezado, lo principal es estar pendiente de los cambios realizados en dicho repositorio remoto (servidor GIT).

## Acceso por primera vez
Cuando clonamos un repositorio remoto, debemos tener en cuenta que no exista en la ruta actual ninguna carpeta con el mismo nombre que el repositorio, o cualquier nombre que querramos ponerle. Esto se debe a que GIT, por cuestiones de seguridad, evitara sobreescribir archivos existentes.

* **git clone 'remote' 'folder'** : crea una carpeta en donde se descarga el contenido del repositorio.
* **cd 'folder'**: Abre la carpeta creada utilizando el comando git clone.

## Sincronizacion de cambios
Una vez clonado un proyecto, debemos tener en cuenta que sus cambioes no se sincronizaran automaticamente, sino que debemos enviar y descargar los mismos periodicamente, ya que de lo contrario estariamos trabajando en un proyecto que se encuentra desactualizado, y si bien podemos seguir integrando dichos cambios, se dificultaria esta tarea.

* **git fetch 'remote'**: Descarga el historial de cambios del repositorio.
* **git pull 'remote' 'branch'**: Descarga los cambios y los integra a la rama actual.
* **git push 'remote' 'branch'**: Envia los cambios locales al repositorio remoto.
