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

