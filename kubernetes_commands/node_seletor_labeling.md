# Node Selector / Node Labeling

https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/

### Label to a node

```
kubectl label node ${NODE} ${LABEL}
```

eg: ```kubectl label node kworker2 demoserver=true```


### Show all labels of a node

```
kubectl get node ${NODE} --show-labels
```

### Update pod 'foo' with the label 'unhealthy' and the value 'true'.

```
kubectl label pods foo unhealthy=true
```

### Update pod 'foo' with the label 'status' and the value 'unhealthy', overwriting any existing value.

```
kubectl label --overwrite pods foo status=unhealthy
```

### Update all pods in the namespace

```
kubectl label pods --all status=unhealthy
```

### Update a pod identified by the type and name in "pod.json"

```
kubectl label -f pod.json status=unhealthy
```

### Update pod 'foo' only if the resource is unchanged from version 1.

```
kubectl label pods foo status=unhealthy --resource-version=1
```

### Update pod 'foo' by removing a label named 'bar' if it exists. Does not require the --overwrite flag.

```
kubectl label pods foo bar-
```