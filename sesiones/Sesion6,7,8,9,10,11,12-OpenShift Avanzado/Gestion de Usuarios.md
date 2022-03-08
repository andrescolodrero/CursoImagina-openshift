# Gestion de usuarios
oc get users

oc delete users -> cuidado, prune los objetos antes

# COnfigurar http-pass
oc get secret -n openshift-config

# en una sesion linux:
htpasswd -c -B -v users.htpasswd admin doubletap

# Grupos
oc adm groups new desarrolladores
oc adm groups add-user <usuario>
oc get groups
oc adm policy who can
# Roles a usuarios
oc adm policy add-role-to-user
oc adm policy remove-role-from-user
# Roles
oc adm policy add-role-to-group
oc adm policy remove-role-from-group

# Cluster roles
oc describe clusterrole.rbac
oc describe clusterolebinding,rbac

# Service Accounts
oc get sa
oc create sa
oc policy add-role-to-user view system:serviceaccount:top-secret:robot