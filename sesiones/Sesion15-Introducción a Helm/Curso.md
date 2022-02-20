## Instalar Helm y limpiar kubernetes cluster

Para Windows:

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install kubernetes-helm

# Linux: apt

## Repositorios
helm repo add stable https://charts.helm.sh/stable
helm repo update
helm search repo wordpress
helm install demowp stable/wordpress

mkdir helmrepo
 helm fetch stable/wordpress --untar

 helm repo add
 helm repo list
 helm repo update
 helm repo remove

 ## Releases

 Helm status
 helm upgrae

 ## HELM CHARTS
 helm create demo
 helm install demo ./demo --dry-run
 helm install demo ./demo 

kubectl --namespace default port-forward (podname)) 8080:80 

## Modificar Helm Charts
helm show values demo
helm install demo ./demo --dry-run
# cambiar un valor del chart
helm install demo ./demo --set image.tag=latest --dry-run
# Crear un fichero de valores:
newvaues.yaml
 helm install demo ./demo -f ./demo/newvalues.yaml --dry-run

 ## Lenguaje de Charts

 ## Crear Nuevos Chart
 helm create NOMBRE

 - Buscar un ejemplo de Servicio (ejercicio 1)
 - aplicar Cambios
 - crear directorio template
 - crear: Chart.yaml
 - crear values
 (from root directory)
helm show values blog
 helm install blog blog --dry-run

 # Ejercicio: 
 1. Modificar otros valores como puerto, etc
 2. UPgrade
 
