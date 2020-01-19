# Kubernetes Install


You can run gosense with kubernetes. you need prepare kubernetes first.

install gosense by kubernetes very simple.

Rename `config.toml.dist` to `vol/config.toml`, remember change configs.

then run
```
kubectl create -f db.yml
kubectl create -f k8s.yml
```

Then get svc expose address
```
kubectl get svc
```

open browser, visit http://ip.address:port


for me, it serve at http://10.100.171.88:8080

