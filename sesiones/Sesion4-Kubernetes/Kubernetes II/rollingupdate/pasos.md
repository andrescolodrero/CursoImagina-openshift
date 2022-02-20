## Rolling Update
Ver version de wordpress
Modificar YAML
kubectl rollout status deployment.v1.apps/wordpress --record # record mantiene la historia del deployment
# Probar con una version que no existe
kubectl rollout status deployment.v1.apps/wordpress 
kubectl rollout undo  deployment.v1.apps/wordpress 

#ver errores y elimnar deployment
# usar "fix"
