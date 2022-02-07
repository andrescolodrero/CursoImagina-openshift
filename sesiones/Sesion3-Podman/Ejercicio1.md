# Podman. 1

COnfiguracion: /etc/containers

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
