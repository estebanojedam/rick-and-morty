## GIT FLOW

git status

# Git
```
Git es un sistema de control de versiones.
Es un sistema que controla (administra) las distintas versiones de un programa. Para controlar los cambios que se van presentando en la evolución de un proyecto. Nos brinda la posibilidad de tener un listado de los cambios que se van realizando, nos permite nuclear (trabajar en un mismo proyecto) con multiples programadores.
Git es un sistema de control distribuido. Con el tenemos el repo local y el repo remoto con sus ramas.
Dentro de un proyecto podemos ir a distintos puntos del tiempo.
Snapshots es Git nos permite obtener capturas de nuestro código en cualquier punto
```
## Estados o áreas
En git tenemos 3 estados:
- Working directory 
  - git add .
```
Es donde trabajo de manera local con mis archivos (repositorio local).
```
- Staging area
  - git commit
```
Luego en este área vamos a preparar todo lo que luego vamos a guardar
```
- Repository
```
Finalmente con el commit se crea la foto de los últimos cambios en nuestro repositorio
```
- git push
```
Y para subir nuestros cambios al repositorio remoto (al servidor) 
```

`Basic commands`
- git init
- git status
- git add \<file>
- git commit -m "message"
- git push
- git pull
- git clone 

`Git pasos para usar git`
- Descarga de Git
- Instalacion de Git
- Abrir consola git bash

`Git version`
```
git --version
```
`Git Todos sus comandos`
```
git config -h
```
`Git Bash`
```
Es una consola pero con mejores funcionalidades. Trae los conceptos de unix (es decir de linux o mac que descienden de unix).
Nos brinda comandos de unix como:

ls  <-- lista de los directorios

pwd <-- dir donde estamos

mv archivoname.js newnamearchivo.js <-- es para cambiar de nombre los archivos

cat namearchivo.js <-- nos muestra el contenido de nuestro archivo

Y la podemos habilitar usar directo desde visual studio code.
```

`git init`

Es para iniciar un proyecto.
Al momento de ejecutar git init se crea una carpeta .git (oculta) que se encarga de administrar todos los cambios. Y desde visual a nuestros archivos se les crea una letra U anexada a su derecha y por consola (terminal) nos envía el mensaje: Initialized empty Git repository in C:/Users/mauuu/OneDrive/Escritorio/proyect name/.git/

ls -a <-- nos muestra los archivos ocultos

`git status`
```
Nos muestra que archivos tenemos en donde estamos trabajando y si hay algún commit (si algún archivo se encuentra agregado al Staging area (mi entorno de trabajo))
```
```
Ejemplo:
git init
git status

On branch master
No commits yet
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.js
        index.html
nothing added to commit but untracked files present (use "git add" to track)
```
`git add`
```
git add .
git status

On branch master
No commits yet  
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   app.js
        new file:   index.html

```
`git add .`
```
Podemos agregar todos los archivos de una vez con git add .
```
`git commit`
```
Ahora 
git commit 
Si es la primera vez debemos configurar nuestro usuario
```
`git config`
```
git config --global user.email "mauuuricio@hotmail.com" 
git config --global user.name "Mauricio776" <-- name user github

Ya si podemos crear nuestro primer Snapshots con:
git commit
(se abre la terminal a moso din donde para poder iniciar insertar debemos tocar la letra i)
--> i (letra i)
--> escape
-->:wq
```
```
nos devuelve
[master (root-commit) a45c2fc] init commit
 2 files changed, 13 insertions(+) <-- inserta
 create mode 100644 app.js
 create mode 100644 index.html <-- crea hash (especie de id) para cada archivo
```
`git commit -m <message>`

`git commit -am <message>`

Git commit –am “mensaje” => Se utiliza para aplicar git add y git commit, pero este comando solo funciona si primero hiciste al menos una vez git add sobre los archivos que estas trabajando

`git log`
```
commit a45c2fc5000abe16cbf7b0bb6af552997abf9757 (HEAD -> master)

Nos dá un hash de ese snapshots (de esa captura (cual punto de partida))
Vemos todos los commits con su hash anexado

Vemos todo el registro (todos los cambios) de nuestro código a lo largo del tiempo

Nos muestra todo nuestro historial 
```
```
Ahora
git status
On branch master
nothing to commit, working tree clean
(nos dice que todos los cambios han sido realizado y que no hay nada por hacer por el momento)
```
`git checkout -- <name file>`
```
Ejemplo: git checkout -- index.html
or 
git checkout -b index.html
Este comando nos da la opción de retroceder al último commit realizado
```

`git diff`
```
Ejemplo: git diff index.html
Nos muestra las diferencias del último commit y los cambios actuales que aún no se han commiteado donde

--- a/index.html
+++ b/index.html
@@ -1,12 +1 @@
-<!DOCTYPE html> <-- la resta es lo que se ha eliminado
-<html lang="en">
-<head>
+TEXTO SOLAMENTE <-- la suma es lo que se ha agregado
```
`git branch`
```
* master <-- nos indica en este caso que se encuentra en la rama master que en este ejemplo es nuestra única línea (rama)

```

`.gitignore`

Usaremos este comando para seleccionar todo aquel archivo que deseamos no se encuentre en nuestro entorno git de trabajo.


## Moverse entre ramas

`git branch <branch name>`
```
git branch newrama
Nos crea una nueva rama de name newrama
```
`git checkout <branch name>`
```
git checkout newrama 
nos brinda poder movernos a dicha rama

git branch
  master
* ramauno
Ahora nos indica que nos movimos a la rama newrama

Bien cabe destacar que cada rama tiene sus propios commits (cambios) y se desarrollan de manera independiente del momento que ha sido creada
```

# GitHub
```
Aquí podremos guardar nuestros repositorios de código 
Repositorios remotos
```
## Crear un repositorio en github
```
Steps
In GitHub
1 new repository
2 name
3 creating repository
4 GitHub nos indica que:
Debemos implementar en nuestra terminal bash los siguientes comandos:
git init <-- de no haber inicializado antes claro
git add README.md or git add .
git commit -m "first commit"

Una de las cosas que github ahora recomienda es cambiar la rama a principal en lugar de maestra.
git branch -M main <-- opcional
```
`git remote`
```
Con este comando seleccionamos nuestro repositorio remoto (servidor remoto)

git remote add origin https://github.com/Mauricio776/git-test.git
git push -u origin main or git push -u origin master
según cual sea nuestra rama principal inicial

Ahora ya tenemos nuestro código subido a nuestro repositorio de código (remoto) en gitHub

```
`git push -u origin`
```
la -u nos crea la rama
origin es el lugar (desde) donde se crea nuestra rama 

Ejemplo:
git push -u origin main
```
```
Nos recomienda tener un readme
git add README.md
para indicar de que trata nuestro código (proyecto)

```

`git merge`
```
Ejemplo:
git branch
* master
ramauno

Estamos parados en la rama master y nos queremos traer todos los cambios de la rama ramauno

git merge ramauno

```

`git push`
```
Es para subir los cambios a nuestro repositorio remoto (servidor)
```

`git pull`
```
Nos traemos los cambios que han realizado los demás desarrolladores

Es para actualizar los cambios del repositorio remoto a nuestro repositorio local

Debemos considerar estar parados en la rama correcta de la cual deseamos actualizarnos
```

## Descargar un código (proyecto) de github

Lo podemos realizar de dos maneras:
```
1 Descargamos el zip
2 Implementamos git clone
```
`git clone`
```
git clone <dirección del repositorio que vamos a descargar (es decir, clonar)>

Ejemplo:
git clone https://github.com/Mauricio776/git-test
```
Recordatorio
Si la terminal bash no corta
Tipear
u <-- la letra u or
:wq <-- write and quit
or
ctrl + c

```
```
### Resumen
```
Pc

git add .
Stage

git commit
Commit

git push
Server (nube)

Cada rama es una versión en sí

Si nos pide contraseña es el token que se encuentra en nuestra cuenta github
--> developer setting 
--> personal access tokens
```



## Git diccionario 

|Comando|Funcionalidad/Definicion|
|---|---|
|`git branch --list`| Muestra una lista de las ramas existentes |
|`git branch` [nombre]| Crea una nueva rama con el ***[nombre]*** indicado |
|`git branch -m/-M`  [nombre]| Renombra a la rama en la que estas parado, y reemplaza el nombre con lo que este en ***[nombre]*** |
|`git branch -d/-D`  [nombre]| Borra la rama indicada en ***[nombre]***|
|`git checkout`| Mostrara una lista con aquellos archivos no subidos a la rama en la que estas ubicado |
|`git checkout` [nombre] | Te posicionará en la rama indicada en ***[nombre]*** |
|`git checkout -b` [nombre]| Creará una rama nueva llamada ***[nombre]*** a partir de en donde estás parado, y te posicionará en la nueva rama |
|`git clone` [url] | clona un repositorio remoto ubicado en la ***[url]*** |
|`git init`| Crea un repositorio Git vacío o reinicializa uno existente |
|`git log`| Muestra todos los commits hechos hasta el momento |
|`git merge` [nombre]| Trae los archivos en la rama ***[nombre]*** y los mezcla con la rama en la que estas ubicado actualmente |
|`git pull` | Traerá todos los cambios que esten conectados a un repositorio, incluyendo ramas creadas, archivos nuevos, y cualquier cambio hecho, sobre la rama en la que estes ubicado |
|`git pull origin` [nombre]| Traerá solo los cambios efectuados en el origen, en la rama especificada en ***[nombre]*** |
|`git push`| Actualiza un repositorio remoto con los ultimos cambios generados |
|`git push origin` [nombre]| Actualiza la rama ***[nombre]*** un repositorio remoto con los ultimos cambios generados en esa rama |
|`git push -u origin` [nombre] | Sube la rama ***[nombre]*** al re |
|`git remote`| Administrar un conjunto de repositorios rastreados |
|`git remote add origin` [url repo]| Conecta tu instancia de Git con un el repositorio remoto ubicado en ***[url repo]*** |
|`git stash`| Reserva los cambios en un directorio "sucio" aparte (recomiendo investigar) |
|`gitk`| El navegador de repositorio de Git |
|``|  |

## npm

| Comando | Función |
|---|---|
|`npm -v`| Devuelve la version de NPM instalada en tu computadora |
|`npm init`| Inicia, en la carpeta que se encuentra, una instancia de npm, creando un archivo package-json, listo para instalarle dependencias|
|`npm i` [paquete]| Instala la libreria especificada en ***[paquete]***  |
|`npx`| herramienta para ejecutar paquetes |
|`npx create-react-app` [nombre]| ejecutará el paquete de React y creara la carpeta ***[nombre]***|
 
## Node

| Comando | Función |
| --- | --- |
|`node -v`| Devuelve la version de Node instalada en tu computadora |
|`node` [nombre].js | ejecutara el archivo que coincida con ese nombre sobre la carpeta en donde este ubicado, con node |
|``|  |

## Bash

| Comando | Función |
| --- | --- |
|`ls`| Muestra los archivo de la carpeta en donde estes ubicado |
|`ls -a`| Muestra ***TODOS*** los archivos en la carpeta donde estes ubicado (incluye ocultos) |
|`pwd`| Muestra la direccion de la carpeta donde estes ubicado |
|`date`| Muestra la fecha y hora actual |
|`clear`| Limpia la consola de todos los comandos ejecutados |
|`mkdir` [nombre]| Crea un nuevo directorio (carpeta) en donde estes ubicado con el ***[nombre]*** indicado |
|`rm` [nombre] | Elimina el archivo ***[nombre]*** que se encuentre donde estes ubicado |
|`rm -f` [nombre] | Elimina el archivo ***[nombre]*** de forma forzada, en caso que no pueda hacerlo |
|`head` [nombre] | Muestra las primeras 10 lineas del archivo ***[nombre]*** |
|`tail` [nombre] | Muestra las ultimas 10 lineas del archivo ***[nombre]*** |
|`mv` [direccion origen] [direccion final] | Mueven el archivo/carpeta que se indique en ***[dirección origen]*** hacia la carpeta ***[dirección final]*** |
|``|  |










## Usando git fetch ​​para obtener cambios y luego fusionarlos usando Commit Hash
Con esto, puede obtener los cambios del repositorio remoto y luego ubicar el hash de el commit que desea fusionar con la base de código local. Puede consultar los siguientes pasos:

Obtenga los últimos cambios en el repositorio
git fetch remote <branch_name>
El comando git fetch ​​obtiene los cambios de <branch_name> especificado.

Visualización del registro de Git para obtener Hash de commit para fusionar
git log
El comando anterior enumera todas los commits, como el hash de commit, el autor de el commit, la fecha de commit y el mensaje de commit.
Puede obtener todas los commits y sus respectivos hashes en una línea usando el indicador --oneline, git log --oneline.

Fusión de el commit deseada utilizando el hash de commit
git merge <commit_hash>
Finalmente, el commit que desea fusionar se puede realizar utilizando el hash de commit con el comando git merge.

Con el método anterior, todas los commits hasta el commit fusionada también se fusionan. Sin embargo, para fusionar los cambios de una soel commit, puede usar git cherry-pick como:

git cherry-pick <commit_hash>
Extraiga el código de commit específica para una nueva rama
Si desea extraer los cambios de el commit y verificar una nueva rama, puede usar un solo comando para lograrlo.

git checkout -b <new_branch_name> <commit_hash>
Podemos recuperar el hash de commit con el comando git log mencionado anteriormente.

Usando git pull con Commit Hash
Este paso es similar al mencionado en el primer método hasta el segundo paso. Después de hacer lo mencionado, el segundo paso (después de ejecutar git fetch ​​y git log para ver el hash de commit).

git pull origin <commit_hash>
Con el uso del comando anterior, puede extraer todos los cambios del hash de los commits mencionadas.

Aquí, git pull combina git fetch ​​y git merge.