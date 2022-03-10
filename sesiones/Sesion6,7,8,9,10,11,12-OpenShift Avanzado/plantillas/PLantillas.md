# Cuando usamos el comando oc new-app, crea aplicaciones con plantillas
# Crear projecto para developer
# Log como developer  y crea tu project "developer-curso"
oc create project
oc adm policy add-role-to-user admin developer

# 1. Crear Applicaciæon desde una imagen
+Add -> Container: quay.io/openshiftroadshow/parksmap:latest
Nombre: workshop
Labels:
app=workshop
component=parksmap
role=frontend

parksmap-developer-curso.apps-crc.testing

# Crear Aplicacion desde Git

+Add  -> From GIt: https://github.com/openshift-roadshow/nationalparks.git
Nombre: workshop
Labels:
app=workshop
component=nationalparks
role=backend

# Crear Mongo DB
# Instalar template (como developer)
oc create -f https://raw.githubusercontent.com/openshift-labs/starter-guides/ocp-4.6/mongodb-template.yaml -n developer-curso
oc get template
Database Service Name:


mongodb-nationalparks
MongoDB Connection Username:


mongodb
MongoDB Connection Password:


mongodb
MongoDB Database Name:


mongodb
MongoDB Admin Password:


mongodb

# Add Secret to 
# Pasar a vista de developer
Instanciar el mongo template y anadir etiquetas
oc label dc/mongodb-nationalparks svc/mongodb-nationalparks app=workshop component=nationalparks role=database --overwrite

# Acceder a "Secrets" para copar mongo-ephemeral-xxxx secrets

 
ASaasdasd


# Crear una ruta
oc new-app  -e MONGODB_USER=mongodb -e MONGODB_PASSWORD=mongodb -e MONGODB_DATABASE=mongodb-nationalparks  -e MONGODB_ADMIN_PASSWORD=mongodb   registry.redhat.io/rhscl/mongodb-26-rhelasdasd7

