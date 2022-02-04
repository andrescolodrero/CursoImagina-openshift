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
podman run docker.io/library/registry

podman run -dt -p 5000:5000/tcp docker.io/library/registry