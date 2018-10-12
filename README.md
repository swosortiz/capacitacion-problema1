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


#PARTE 6 comando ejecutar container sh docker run -d -p "1080:80" swosortiz/orbis-training-docker:1.0.0

```
docker exec -it  swosortiz/orbis-training-docker:1.1.0 /bin/sh
```
¿Qué es NGINX?

¿Cómo expongo puertos en docker?

¿Cómo especifico los puertos al levantar un contenedor (docker run)?

¿Cómo hago 'forward' al levantar un contenedor (docker run)?

# PARTE 7:
5. 
a) Usando docker run ejecutar npm install. 
Al volumear se instalará en el contenedor y también en mi host local.

docker run -i -v $(pwd):/app -w /app swosortiz/orbis-training-docker:2.0.0 npm install -rm

b) Visualizar si se instaló npm en el container:

docker run -i -v $(pwd):/app -w /app swosortiz/orbis-training-docker:2.0.0 ls /app

7. Exponer los puertos 3030 y 35729 en la imagen de docker, luego ejecutar npm start usando docker run:

docker run -i -p 3030:3030 -p 35729:35729 -v $(pwd):/app -w /app marcoschoque/orbis-training-docker:2.0.0 npm start




