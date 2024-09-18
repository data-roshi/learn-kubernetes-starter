```shell
kubectl apply -f filename.yml 
```

```shell
kubectl get services 
```

```shell
kubectl get svc
```

```shell
kubectl port-forward service/web-service 8080:80
```

forward the service port 80 to 8080 on local machine

```shell
kubectl get svc web-service -o yaml
```