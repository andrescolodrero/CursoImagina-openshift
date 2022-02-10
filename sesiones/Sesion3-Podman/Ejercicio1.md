# Podman. 1

COnfiguracion: /etc/containers
// repositorio localq:wq
comandos:
podman image
podman inspect
podman login
podman pull/push
podman rmi
podman search
podman tag/untag

- Comenzar con contenedores!
- Chequear el registro

podman search ubi:latest
podman pull registry.access.redhat.com/ubi7/ubi-minimal

podman images
podman inspect registry.access.redhat.com/ubi7/ubi-minimal

podman tag ubi:latest registry.access.redhat.com/ubi7/ubi-minimal

Trabajo: Crear un repositorio local:
- Buscar imagen registry de docker.io
- ejecutar imagen en puerto 5000
(crea un local repo)
Ejecutar applicacion
podman run -dt -p 8080:80/tcp docker.io/library/httpd

/home/andres# podman inspect 9608975ad9e5 | grep "IPAddress"

Ejercicio:
Ejecutar dos contenedores (httpd o nginx)
Verificar IP 
Conectar contenedor 1 y verificar conexion con contenedor 2.


podman exec -it 900244468ff1 /bin/bash


(wget)
NOMAD
