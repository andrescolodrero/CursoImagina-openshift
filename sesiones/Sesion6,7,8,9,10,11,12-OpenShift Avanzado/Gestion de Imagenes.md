# Imagenes
oc get images
oc tag imagen:2 imagen:3
oc delete tag

# imagaPullPollycy Pull
alway/ifnotpresent/never

# Ejemplo: Permitir Pods en Projectoa, referenciar imagenes  en ProjecttoB
oc policy add-role-to-user system:image-puller system:serviceaccounts:projectA:Default --namespace=projectB

# Templates
oc create -f plantilla1

# Practica. COnfigurar ImageStream
oc get is
oc tag
oc get images

# Desplegar Ingress
# Desplegar Statefull-app. Por que Falla?
