# aes-kustomization-example

Kubernetes kustomization example for setting up Ambassador Edge Stack ([AES](https://www.getambassador.io/docs/edge-stack)), basic auth and more...

## Getting started

All the Kubernetes resources are described in this repository and managed with a single Kustomization entry `kustomization.yaml`.

**1. Apply kustomization**

```bash
$ kubectl apply -k ./
```

**2. Check out pods**

Under all namespaces:

```bash
$ kubectl get pods --all-namespaces
```

or under `ambassador` namespace:

```bash
$ kubectl get pods --namespace ambassador
```

**3. Delete deployments**

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
