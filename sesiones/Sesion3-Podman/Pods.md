## Create POds
podman pod create --name demo-pod
podman ps 

podman run -dt --pod demo-pod  nginx
podman ps -a --pod (ver infracontainer)

# PArar contenedores en in pod
podman start <continer-id>
podman stop <continer-id>
podman rm <continer-id>

# Operaciones POd
podman pod stop <podname>
podman pod start <podname>


podman run -dt --pod new:webserver -p 8080:80 nginx

podman generate kube webserver

podman play kube webserver.yaml


# Crear una applicatrion
Wordpress pod con MariaDB y wordpress
1. Crear POD
2. Crear bcontainer maria DB (no visible fuera del Pod)
3. Crear WordPress

podman pod create --name wordpress-pod -p 8080:80

podman run -dt --restart=always --pod=wordpress-pod -e MYSQL_ROOT_PASSWORD="db_pass" -e MYSQL_DATABASE="wp" -e MYSQL_USER="wordpress" -e MYSQL_PASSWORD="wppass" --name=wp-db mariadb

# como ver ENV values?
podman exec -it (id) /bin/bash
podman run -d --restart=always --pod=wordpress-pod -e WORDPRESS_DB_NAME="wp" -e WORDPRESS_DB_USER="wordpress" -e WORDPRESS_DB_PASSWORD="wppass" -e WORDPRESS_DB_HOST="127.0.0.1" --name wp-web wordpress

curl -s http://localhost:8080
echo $?

Restart. Por que es persistente?

# Generar un fichero Kubernetes
podman generate kube
podman play kube.yml

