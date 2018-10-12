# Ejercicio 1
Capacitación: Git, bash y docker
Integrantes:
- [Steven William Ortiz Sáenz]
- [Marcos Choque Asto]
- [Steven William Ortiz Sáenz]

1. ¿Qué es y para qué sirve GIT?
GIT es un sistema de control de versiones distribuido y sirve para versionar nuestros archivos y controlar el historial de cambios que podrían tener.

2. ¿Que es Github o bitbucket?
Son servicios de alojamiento web para proyectos que utilizan GIT y Mercurial.

3. ¿Qué es y para qué sirve el SSH?
Es un protocolo de comunicación segura entre 2 sistemas con arquitectura cliente / servidor y que permite a los usuarios conectarse a un host remotamente.

4. ¿Que pasa si cambio de PC? ¿Tendré que generar el SSH nuevamente?¿Por qué?
Si cambio de PC deberé generar una nueva clave SSH debido es único para cada computadora.

5. ¿Qué es markdown? ¿Para qué sirve?
Es un lenguaje de marcado ligero que sirve para crear documentación basado en conseguir la máxima legibilidad y facilidad de publicación como texto plano.

6. ¿Cómo inicializo y configuro un proyecto de git?
Se debe ejecutar el comando "git init" en la carpeta donde se desea almacenar el nuevo repositorio. Para configurar el repositorio se debe ejecutar el comando "git config" el cual nos permite registrar el correo, usuario y otros.

# Ejercicio 2
1. ¿Para qué ayuda el `git stash`?
Para guardar las modificaciones de archivos y almacenarlos de forma temporal sin agregarlos a la rama y sin generar un commit.

2. ¿Cuál es la diferencia entre `git stash pop` y `git stash apply`?
"Git stash" pop jala el último stash y lo borra de la pila de stash.
En el caso de "stash apply" también jala el último stash pero lo mantiene en la pila de stash.

3. ¿Qué significa el modo interactivo del `git rebase`?
Permite revisar, editar, cambiar commits antes del reordenamiento.

4. ¿Cual es la diferencia entre la shell y la terminal?
Shell es un interprete de linea de comandos que se usan para enviar ordenes al computador (ejemplos: bash, zsh, etc).
Terminal es el medio de entrada donde el usuario interactua para ingresar comandos.

5. ¿Que hace estos comandos? `git clone`, `git status`, `git add`, `git commit`, `git push`, `git checkout`, `git stash`, `git rebase`, `git merge`, `git branch`, `git push`,
git clone: copia un repositorio remoto
git status: muestra los archivos sin y con seguimiento
git add: permite que los archivos se versionen.
git commit: agrega un cambio a la rama. Solo los archivos con seguimiento.
git push: sube los commit locales al repositorio remoto
git checkout: mueve el puntero HEAD entre commits y ramas
git stash: guarda los cambios en memoria(stash)
git rebase: mueve los commits de una rama y los posiciona sobre otra la rama objetivo
git merge: fusiona una rama con otra.
git branch: lista las ramas locales. Tiene otros argumentos para crear y borrar.
git push: envia los cambios de una rama local al repositorio remoto


# Respuestas parte 05:
1. Listar las carpetas que hay dentro de la imagen. Para esto es necesario ejecutar el comando bash al hacer docker run, con la imagen<nombre-usuario>/orbis-training-docker:0.2.0 y con solo la bandera -it

docker run -it swosortiz/orbis-training-docker:0.2.0 bash
ls

- ¿Porqué es necesario crear un contenedor con esta bandera -it ? ¿Qué pasa si no le pongo -it? ¿Para qué sirve ejecutar el comando bash al eejcutar una imagen?

-> -it es un atajo para --interactive y --tty con ese argumento se puede ir hasta dentro del contenedor.
-> Si no consideramos "-it", el contenedor se ejecutará con su COMMAND definido en la imagen y finalizará sin ejecutar otro comando.

2. ¿Cuál es la diferencia entre docker ps y docker ps -a?
 Docker ps lista los contenedores activos. 
 Docker ps -a muestra todos los contenedores tanto activos como otros.

3. Copiar el archivo preguntas.md en la imagen

Usar la imagen <nombre-usuario>/orbis-training-docker:0.2.0
Dentro de la imagen se debe crear una carpeta llamada app en la ruta base / yluego copiar el archivo preguntas.md en dicha carpeta.
Finalmente se debe contruir la imagen

---- 
4. ¿Cuál es la diferencia entre una imagen y un contenedor? 
Una imagen es una definicion que opupa un espacion en el disco, un contenedor la instanciacion en memoria.

5. ¿Cómo listo las imágenes que hay en mi computadora? 

docker images

6. ¿Cómo salgo de un contenedor de docker? 

exit o ctrl+c

7. ¿Se elimina el contenedor al salir de ella? 

docker run --rm -it <image_name>

8. ¿Cómo elimino un contenedor?

docker rm <container_id>

9. ¿Para qué es necesario el flag -i, -t, --rm?

-i: modo interactivo
-t: salida tty(terminal)
--rm: remove after run

10. ¿Cómo verifico que el archivo creado se encuentra en la imagen?

ls -l

11. ¿Cómo se comenta una linea de código en Dockerfile?

Anteponiendo en la linea el caracter:   #

