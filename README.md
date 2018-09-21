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
