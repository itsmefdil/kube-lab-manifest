### Autoscale with HPA

```bash
kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10
```

### Check HPA

```bash
kubectl get hpa
```

### Check HPA with more detail

```bash
kubectl describe hpa
```

### Check HPA with more detail

```bash
kubectl get hpa -o wide
```

### Add sakura
```bash
kubectl run -it --rm load-generator --image=busybox /bin/sh

Hit enter for command prompt

while true; do wget -q -O- http://php-apache; done
```