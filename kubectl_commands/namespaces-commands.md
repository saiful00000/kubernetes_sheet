# Namespaces

## Create / Delete namespaces

```
kubectl create namespace ${NAMESPACE_NAME}

kubectl delete namespace ${NAMESPACE_NAME}
```

## View all namespaces

```
kubectl get ns

kubectl get namespaces
```

## Switch between namespaces

```

```

## View all pods / deployments / services from a specific namespaces

```
kubectl -n ${NAMESPACE_NAME} get pods

kubectl --namespace ${NAMESPACE_NAME} get pods

kubectl -n ${NAMESPACE_NAME} get svc

kubectl -n ${NAMESPACE_NAME} get deployments
```