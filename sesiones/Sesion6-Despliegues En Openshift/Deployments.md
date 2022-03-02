oc apply -f .\deploymentk8s.yaml 

# Crear aplicacion desde 

imagen docker: oc new-app mysql

registro: oc new-app myregistry:5000/example/myimage

Plantilla: 
oc new-app -f plantilla.json
oc new-app ruby-helloworld-sample

# Quotas
oc/kubetcl create -f <file> - n <namespaCE>
oc get quota -n

# Multiple projetos
oc create clusterquote 

oc create clusterresourcequota for-name \
    --project-label-selector=name=frontend \
    --hard=pods=10 --hard=secrets=20

# Prune: Eliminar viejas aplicaciones u objetos
oc adm prune <objet-type> --confirm / --blacklist // --whitelist / --sync-config

oc adm prune deployments

