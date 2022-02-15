# Imagenes
oc get images
oc tag imagen:2 imagen:3
oc delete tag

# Pull
alway/ifnotpresent/never

oc policy add-role-to-user system:image-puller system:serviceaccounts:projectA:Default --namespace=projectB

Usar oc create secret # para repositorios con Login

# Practica. COnfigurar ImageStream
oc get is
oc tag
oc get images
