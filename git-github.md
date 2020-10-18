Notas sobre el curso de GIT <br>
Recomendacioon de un curso - https://miriadax.net/web/gitmooc<br>
=============================

## descripcion

# Comandos

## Comandos

### Comandos

\*Tenga en cuenta que estos comandos por lo general se escriben en una sola linea

| Comando \*                                    | Que significa | Que hace                                                                   | ejemplo \*                            | Notas                                                          |
| --------------------------------------------- | ------------- | -------------------------------------------------------------------------- | ------------------------------------- | -------------------------------------------------------------- |
| git init                                      |               | Inicializa git                                                             | cd "ruta/que/queremos/abrir" git init | Create an empty Git repository or reinitialize an existing one |
| git config                                    |               | ver la configuración actual de git                                         |                                       |                                                                |
| git config --global user.email "tu@email.com" |               | Configurar tu email                                                        |                                       |                                                                |
| git config --global user.name "Tu Nombre"     |               | Configura tu nombre de usuario                                             |                                       |                                                                |
| git status                                    |               | Muestra el estado acual de la base de datos                                |                                       |                                                                |
| git add \_myfile.txt                          |               | Agrega el archivo en Staging                                               |                                       |                                                                |
| git add .                                     |               | Sube todo los archivos de la carpeta actual                                |                                       |                                                                |
| git rm -- cached \_myfile.txt                 |               | Elimina el archivo de la RAM sin eliminarlo de la carpeta                  |                                       |                                                                |
| git commit -m "Primer commit de este archivo" |               | Sube el archivo al repositorio                                             |                                       |                                                                |
| git log \_my file.txt                         |               | Puede ver todas las modificaciones del archivo asi como ver quien las hizo |                                       |                                                                |
| git log --stat                                |               | Puede ver todas las modificaciones detalladas                              |                                       |                                                                |
| git diff #old #actual                         |               | valida los cambios entre dos commits para un mismo archivo                 |                                       |                                                                |
| git reset #old --hard                         |               | Regresa a una version anterior del #old                                    |                                       |                                                                |

```
  <!-- Este codigo solo se imprime, la sintaxis ruby no es evaluada cuando utilizamos las etiquetas '<%  %>' -->
  <% [1,2,3,4].each do |number| %>
    <p>Número: <%= number %></p>
  <% end %>

  <br>
  <!-- Este codigo se evalua, la sintaxis ruby es evaluada cuando utilizamos las etiquetas '<%=  %>'-->
  <%= [1,2,3,4].each do |number| %>
    <p>Número: <%= number %></p>
  <% end %>
```

## Instalar git

-   sudo apt update && sudo apt upgrade
-   sudo apt install git
-   git --version

## Configuracion git

-   git config --global user.name "vifrac"
-   git config --global user.email "vifrac@gmail.com"
-   git config --global color.ui true
-   git config --global core.editor “atom --wait”
-   git config --global core.editor “‘c:/program files/sublime text 3/sublimetext.exe’ -w”
-   git config --list

-   git config --global core.excludesfile ~/.gitignore_global

-   https://www.toptal.com/developers/gitignore

## init git

-   mkdir git prueba
-   -   mkdir seguido del nombre que elijas crea una carpeta con dicho nombre
-   cd
-   -   con este comando mas el nombre de la carpeta creada te posiciona dentro de dicha carpeta
-   git init
-   -   Este comando se usa para crear un nuevo repertorio. Se utiliza solo una vez para la creacion del nuevo repositorio
-   verificar archivos
-   touch index.html
    -   touch sirve para crear archivos desde la consola, se coloca el nombre mas la extencion luego del comando touch
-   nano index.html
-   -   en este caso editamos el archivo index con el editor de texto nano. Se podria usar vim u otro.
-   git status
    -   El comando git status muestra el estado del directorio de trabajo. Permite ver los cambios que se han preparado, los que no y los archivos en los que Git no va a realizar el seguimiento
-   git add index.html
    -   este comando toma una foto del archivo tipeado con sus modificaciones, en este caso va a ver los camambios realizados en index.html antes de guardarlos en el proyecto. Tambien se puede usar el comando git add . con el punto le indico que tome una instantanea de todos los archivos tanto creados como modificados
-   git status
-   git rm index.html
    -   rm se utiliza para remover archivos, lo borra del area de trabajo.
-   list files
    -   lista archivos o carpetas
-   rm index.html
    -   borra el archivo index
-   nano index.html
    -   editamos con nano el archivo index
-   git add index.html
-   git commit -m 'first commit'
    -   se envian los cambio al repositorio es importante ser lo mas descritivo posible enla descripcion que va entre " "
-   modificar html
-   git add .
-   git commit
-   git log
    -   muestra el historial del repositorio sirve para buscar una version en concreto.
-   git log index
-   git show index
-   git diff
    -   muestra las diferencias entre los archivos anteriores y los que se han añadido al area de trabajo

## integrar cambios github

-   crear el repo en github
-   clonar el repo con hhtp
    -   git remote add origin hhtps
-   git push origin master
-   git pull origin master
-   git pull origin master --allow-unrelated--histories
-   list files
-   git status
-   git push origin master

## llaves ssh

-   ssh-keygen -t rsa -b 4096 -C “tu_email@gmail.com”
    -   nos pedira una ruta donde gusrdad
    -   nos pedira un password - confirmar password
    -   nos genera en la ruta por defecto dos archivos
        -   llave privada (id_rsa)
        -   llave publica (id_rsa.pub)
    -   validar creacion de archivos
    -   verificamos que el agente ssh este eneble
        -   eval \$(ssh-agent -s)
    -   agregamos la llave privada a git (pide password)
        -   ssh-add ~/.ssh/id_rsa
    -   copiamos el contenido de la llave publica a en el apartado de seguridad de git
        -   cat ~/.ssh/id_rsa.pub
        -   https://github.com/settings/keys
            -   new ssh key
            -   title (ALGO QUE IDENTIFIQUE EL dominio o server o equipo que se usa)
            -   key
    -   clonamos un rep con ssh
    -   verificamos los remotos
        -   git remote -v
    -   setear los origenes del repo
        -   git remote set-url origin

## Lessons

-   Lesson 05 - Cómo realizar una petición REST e interpretar sus resultados
-   Conceptos extraídos de:
    -   https://code.tutsplus.com/es/tutorials/a-beginners-guide-to-http-and-rest--net-16340
