# Microk8s

To follow official documentation and guide please visi <https://microk8s.io/docs/getting-started>

## Requirements

This process is tested and worked on Linux Ubuntu Operating system. and make sure you running bellow commands as root user.

## Install microk8s

Make sure you have snap store installed in your machine. microk8s is available in snapsote

```bash
snap install microk8s --classic
```

This command will install and create a single node kubernetes cluster automatically.

## Some basic command to monitor and inspect the kubernetes cluster

### To get list of node

```bash
microk8s kubectl get nodes
```

### To get list of pods

```bash
microk8s kubectl get pods
```

### To get running sevices

```bash
microk8s kubectl get services
```

### Get list of all nodes, pods and services

```bash
microk8s kubectl get all
```

```bash
microk8s kubectl get all -o wide
```

### Deploy an demo app

We will deploy a basic nginx demo application to our kubernetes cluster using microk8s. To do so run bellow command. and it will pull anginx image and deploy for you.

```bash
microk8s kubectl create deployment nginx --image=nginx
```

### Scale the nginx pod

We are going to scale up our nginx deployment into 2 replicas.

```bash
microk8s kubectl scale deploy nginx --replicas=2
```

## Status of services

```bash
microk8s inspect
```

### Start and Stop microk8s

```bash
microk8s start

microk8s stop
```