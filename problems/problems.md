# Common Problems and Solutions

## Problem 1

```
The connection to the server localhost:8080 was refused - did you specify the right host or port?
```

```bash
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```