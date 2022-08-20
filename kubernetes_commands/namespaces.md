# Namespaces

## Create / Delete namespaces

```
kubectl create namespace <namespce-name>

kubectl delete namespace <namespce-name>
```

## View all namespaces

```
kubectl get ns

kubectl get namespaces
```

## Switch between namespaces

```
kubectl config use-context <context-name>
```

## View all pods / deployments / services from a specific namespaces

```
kubectl -n <namespce-name> get pods

kubectl --namespace <namespce-name> get pods

kubectl -n <namespce-name> get svc

kubectl -n <namespce-name> get deployments
```