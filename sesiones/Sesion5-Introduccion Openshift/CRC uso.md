## Usando CLI CRC
Estado: crc status
Start: crc start

Configuration:
crc config --help
crc config get memorty


Acceder
crc oc-enc

crc console --credentials
(COnfigurar oc command con environment)

oc login -u kubeadmin -p 5jwwD-m7sJ6-ak7PI-rorww

Crear un project
  oc new-project my-example
    oc new-app django-psql-example
    oc logs -f bc/django-psql-example

Comprabar images:
oc get images

Acceder a la imagen, rutas, etc

Explicar cosas