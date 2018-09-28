# Ejercicio Docker
# Respuesta pregunta 04:
docker build --tag swosortiz/orbis-training-docker:0.1.0 .
# Visualizar imagen creada
docker images
# Pushear imagen creada a DockerHub
docker push swosortiz/orbis-training-docker 
# Al pusher mostro error:  denied: requested access to the resource is denied
# Debemos agregar el usuario de DockerHub y hacer un login para poder recién pushear:
export DOCKER_ID_USER="swosortiz"
docker login
docker push swosortiz/orbis-training-docker
# Cambiar el tag en Docker:
docker tag swosortiz/orbis-training-docker:0.1.0 swosortiz/orbis-training-docker:0.2.0
# Subir a DockerHub:
docker push swosortiz/orbis-training-docker 
# Se visualiza en DockerHub los tags generados:
https://hub.docker.com/r/swosortiz/orbis-training-docker/tags/


# Respuestas parte 04:
1. ¿Qué importancia tiene los tags en un proyecto?
Solo es una cadena arbitraria que apunta a un commit específico y es usado para tener identificado hitos en la linea de desarrollo de un proyecto como releases. 

2. ¿Cuál es la diferencia entre un tag normal y un tag anotado en git?
- Tag normal es una cadena arbitraria en un commit especifico.
- Tag anotado es un tag mas completo, guarda informacion del taggeador, email, fecha, tag message y puede ser verificado con el GNU Privacy Guard(GPG).

3. ¿Cómo se sube todos los tags de git que hay en mi local?
-> git push --tags

4. ¿Es necesario loguearse cada vez que subo una imagen a dockerhub?
-> Solo es necesario logearse una vez.

5. ¿Qué es y para qué sirve docker?
Es una plataforma Open Source que brinda un estándar para desarrollar, implementar y ejecutar aplicaciones dentro de contenedores. Nos ayuda a empaquetar nuestras aplicaciones con todas las partes necesarias, poder compartirlas y transportarlas facilmente.

6. ¿Cuál es la diferencia entre docker y VirtualBox (virtualización)?
Docker usa un kernel(docker engine) para conectarse con el SO del host. VirtualBox crea un nuevo sistema operativo que se conecta por medio de hypervisor con el SO del host. 

En resumen Docker puede activar el ambiente de una aplicación para su funcionamiento con solo lo necesario mientras que en un Virtual Machine se requiere instalar todo un sistema operativo completo que incluye servicios que tal vez la aplicación no la necesita.

7. ¿Es necesario depender de una imagen de docker base al crear una imagen nueva?
No porque se puede crear una imagen base desde cero usando la instruccion FROM scratch en el Dockerfile.

8. ¿Porqué debo anteponer el nombre de usuario en una imagen docker nueva?
Porque ese nombre es usado por el registry (docker hub) como una forma de identificación.

9. ¿Que pasa si creo una imagen sin especificar una versión o tag, con qué versión se crea?
Se crea con la version lastest.