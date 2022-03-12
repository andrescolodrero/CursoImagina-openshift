# Introducir Kubernetes

- Coreografía y orquestación
- Por que son necesarios
- MInikube / Docker Desktop
- Kubetecl
# Comandos
kubectl get pods --namespace kube-system
kubectl config set-context --current --namespace=NAMESPACE
 kubectl get pod  --all-namespaces
 kubectl create namespace curso

 kubectl delete pod




# Practica
1. Despliegue aplicacion y Servicio.

   Crear un servicio en Kcluster.
   kubectl apply -f .\1Despliege.yaml 
   kubectl get deployments
   kubectl get pods
   kubectl -f \Service.yaml apply
   kubectl get svc

   kubectl exec busybox -- curl -s store-products
   kubectl exec -it busybox-sleep wget -O - store-products
   kubectl exec busybox -- nslookup store-products

2. Tolerancia a fallos
3. Escalabilidad
4. Balance de Carga
5. Rollback
6. Enrutamiento
7. Persistecia de Datos
8. 2 Container por pod
kubectl exec -it two-containers -c nginx-container -- /bin/bash

1. Eliminar mysql y recrearlo
2. Inspecionar los volumenes
3. Get pv / pvc
4. Cambiar version wordpress y mysql












