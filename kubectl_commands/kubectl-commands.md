# kubectl Commands

## Troubleshooting

### Basic command

```bash
kubectl get all

kubectl get all -o wide

kubectl get nodes
```

## Deploy and Debuging Pods

Deploy and Scale pods

> Deploy pods

```bash
kubectl run deploy ${POD_NAME} --image ${IMAGE_NAME}

kubectl run deploy ${POD_NAME} --image ${IMAGE_NAME} --replicas 2
```

> Scale Deployments/Pods

```bash
kubectl scale deploy ${POD_NAME} --replicas 2
```

> Create a service to expose deployment/pods

```bash
kubectl expose deploy ${POD/DEPLOY_NAME} --type NodePort --port ${PORT_NUMBER}
```

> Generate yaml file from running deployment and services

```bash
kubectl get deploy ${DEPLOYMENT_NAME} -o yaml > /tmp/${FILE_NAME}.yaml

kubectl get svc ${SERVICE_NAME} -o yaml > /tmp/${FILE_NAME}.yaml
```

> Create/Delete deployment and service from yaml file

```base
kubectl create -f ${FILE_PATH}.yaml

kubectl delete -f ${FILE_PATH}.yaml
```

```bash
kubectl get pods

kubectl describe pods ${POD_NAME}

```

Viewing logs of a pod

```bash
kubectl logs ${POD_NAME}
```

## Debuging Replication Controllers

Ref: https://kubernetes.io/docs/tasks/debug/debug-application/debug-pods/#debugging-replication-controllers

```bash
kubectl describe rc ${CONTROLLER_NAME}
```

## Debuging Servicex

```bash
kubectl get endpoints ${SERVICE_NAME}
```