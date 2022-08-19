# Config utility

## The connection to the server localhost:8080 was refused - did you specify the right host or port?

> local setting

```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```

> copy settings from another machine

```
kdir -p $HOME/.kube
sudo scp  kmaster.example.com:/etc/kubernetes/admin.conf $HOME/.kube/config
```