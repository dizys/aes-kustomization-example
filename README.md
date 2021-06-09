# ambassador-kustomization-example

Kubernetes kustomization example for setting up ambassador gateway (AES), basic auth and more...

## Getting started

All the Kubernetes resources are described in this repository and managed with a single Kustomization entry `kustromization.yaml`.

### Apply kustomization

```bash
$ kubectl apply -k ./
```

### Check out pods

Under all namespaces:

```bash
$ kubectl get pods --all-namespaces
```

or under `ambassador` namespace:

```bash
$ kubectl get pods --namespace ambassador
```

### Delete deployments

```bash
$ kubectl delete -k ./
```

### Tunnel when using minikube

When using [minikube](https://minikube.sigs.k8s.io/docs/start/), use the following command to tunnel 80 and 443 ports in order to make gateway accessible from host:

```bash
$ minikube tunnel
```

Then visit http://127.0.0.1/backend/get-quote/

## License

MIT
