```shell
minikube start --extra-config "apiserver.cors-allowed-origins=["http://boot.dev"]"
```

```shell
minikube dashboard --port=63840
```

```shell
minikube stop
```

```shell
minikube delete
```

```shell
minikube addons enable ingress
```

In production, once you have an ingress configured and have pointed your domain name to it (and perhaps its load balancer), you can access your application from anywhere in the world. The trouble is, we're using Minikube and the cluster is running on our local machine, and not only that, it's running in an isolated virtual machine.

The tunnel should expose the ingress controller's load balancer to your local machine on 127.0.0.1:80 (not the case other ip tunnel?), which we mapped to the synchat.internal and synchatapi.internal domains in the previous exercise (exercise 7).

While the tunnel is open, navigate to http://synchat.internal in your browser. You should see the web app! The JSON API should also be available at http://synchatapi.internal (the root of the API should return a 404, but /healthz should return a 200).
```shell
minikube tunnel -c
```