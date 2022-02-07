# BAsic Networking

Rootfull: sudo, own ip, access priviliged ports, container network
rootless: non root, dont own ip, cant access privileg ports, no access to container network

# Publicar el puerto del contenedor: -p

podman run -dt --name web1 --publish-all nginx
podman run -dt --pod new:webserver -p 8088:80 nginx

podman port -a

# MOnitor

podman run -dt --name nginx1 --health-cmd 'curl http://localhost || exit 1' --health-interval=0 nginx
podman healthcheck run nginx1

# Ejemplo fallo
podman run -dt --name myubi7 --health-cmd 'grep 8 /etc/redhat-release || exit 1' --health-interval=ö0 ubi7:latest
podman run -dt --name myubi8 --health-cmd 'grep 8 /etc/redhat-release || exit 1' --health-interval=0 ubi8:latest

 podman healthcheck run myubi8
  podman healthcheck run myubi7
