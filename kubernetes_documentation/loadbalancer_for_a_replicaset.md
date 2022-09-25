# Exposing a Replicaset / Exposing an External IP address to access an Application in cluster

The documentation will be available in this link

```
https://kubernetes.io/docs/tutorials/stateless-application/expose-external-ip-address/
```

## Create a deployment with 5 replicas

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  labels:
    app.kubernetes.io/name: load-balancer-example
  name: hello-world
spec:
  replicas: 5
  selector:
    matchLabels:
      app.kubernetes.io/name: load-balancer-example
  template:
    metadata:
      labels:
        app.kubernetes.io/name: load-balancer-example
    spec:
      containers:
      - image: gcr.io/google-samples/node-hello:1.0
        name: hello-world
        ports:
        - containerPort: 8080
   
```

Now create your deployment usingbellow command 

```bash
kubectl create -f <your_file_name>.yaml
```
### Debug and inspect your pods/deployments 

```bash
kubectl get deployment <deployment_name>

kubectl describe deployment <deployment_name>

kubectl get replicasets

kubectl describe replicasets

```

## Now create the service/loadbalancer object that exposes the deployment to outside world

```bash
kubectl expose deployment <deployment_name> --type=LoadBalancer --name=<service_name>
```

### Debug and display informations of services

```bash
kubectl get services <service_name>

kubectl describe service <service_name>
```

### To view internal ip addreses of nodes in a replicaset

```bash
kubectl get nodes --output=wide
```

