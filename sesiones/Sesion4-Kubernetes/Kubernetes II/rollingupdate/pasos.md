## Rolling Update
Ver version de wordpress
Modificar YAML
kubectl rollout status deployment.v1.apps/fake-service --record # record mantiene la historia del deployment
# Probar con una version que no existe
kubectl rollout status deployment.v1.apps/fake-service
kubectl rollout undo  deployment.v1.apps/fake-service

#ver errores y elimnar deployment
# usar "fix"
