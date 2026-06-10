# pruebaservidores

comandos de ejecucion 

# 1. Namespace primero (siempre)
kubectl apply -f namespace.yaml

# 2. Secret y almacenamiento
kubectl apply -f secret.yaml
kubectl apply -f persistentmysql.yaml
kubectl apply -f persistent.yaml

# 3. Deployments
kubectl apply -f deployment-mysql.yaml
kubectl apply -f deployment-wordpress.yaml

# 4. Servicios
kubectl apply -f service-mysql.yaml
kubectl apply -f service-wordpress.yaml

# 5. Ingress al final
kubectl apply -f ingress-wordpress.yaml

minikube addons enable ingress -p local-cluster

# Crear todos los archivos primero, luego:
chmod 600 secret.yaml
