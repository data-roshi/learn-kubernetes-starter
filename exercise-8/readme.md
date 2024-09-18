## storage

```shell
kubectl logs <pod_name>
```

up until the logs command

```shell
kubectl logs -f <pod_name>
```

follows the logs

```shell
kubectl apply -f crawler-deployment.yml -f crawler-configmap.yml 
```

```shell
kubectl logs <podname> --all-containers
```