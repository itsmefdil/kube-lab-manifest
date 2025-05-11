### HPA Membutuhkan Metrics Server

#### Cara Install

```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
``

#### Cek Pod Metrics Server

```
kubectl logs -n kube-system deployment/metrics-server
```

Patch kalau error x509
```
kubectl patch deployment metrics-server -n kube-system \
  --type='json' \
  -p='[{"op":"add","path":"/spec/template/spec/containers/0/args/-","value":"--kubelet-insecure-tls"}]'
```

#### Cek top pod

```
kubectl top pods
```
