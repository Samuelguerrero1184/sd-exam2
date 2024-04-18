# Examen parcial 2
Samuel Guerrero
A00365567
# Pasos 
## 1.
Abrir docker y empezar cluster de minikube
```
minikube start --nodes 3 -p "Nombre del cluster"
```

## 2.
Creamos el namespace
```
kubectl create namespace sd-exam2
```

## 3.
Desplegamos con el siguiente comando
```
helm install nginx-app ./nginx-app --namespace sd-exam2
```
## 4. 
Creamos el pod Ubuntu
```
kubectl run ubuntu-test --image=ubuntu --restart=Never --namespace=sd-exam2 -- sleep infinity
```
## 5.
Verficar que se haga la peticion cada 15 segundos