# ambassador-kustomization-example

Kubernetes kustomization example for setting up ambassador basic auth and more...

## Getting-started

### Apply kustomization

```bash
$ kubectl apply -k ./
```

### Check out pods

Under all namespaces

```bash
$ kubectl get pods --all-namespaces
```

or under `ambassador` namespace

```bash
$ kubectl get pods --namespace ambassador
```

### Delete deployments

```bash
$ kubectl delete -k ./
```

### Tunnel when using `minikube`

When using [minikube](https://minikube.sigs.k8s.io/docs/start/), use the following command to tunnel the 80 and 443 ports to make gateway accessible from host:

```bash
$ minikube tunnel
```

## License

MIT
