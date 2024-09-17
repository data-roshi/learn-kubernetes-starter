```shell
kubectl get deployment synergychat-web -o yaml > web-deployment.yml
```

```shell
kubectl apply -f web-deployment.yml
```