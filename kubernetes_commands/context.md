# Kubernetes Contexts

## View all contexts

```
kubectl config get-contexts
```

## View kubernetes config view

```
kubectl config-view
```

## Create a new context

```
kubectl config set-context ${CONTEXT_NAME} --namespace=${NAMESPACE_NAME} --user=${USER_NAME} --cluster=${CLUSTER_NAME}
```

## Switch between contexts

```
kubectl config use-context ${CONTEXT_NAME}
```

## Check current context

```
kubectl config current-context
```
