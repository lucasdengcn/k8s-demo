# K8s Startup

## Components

* AntiAffinity and Affinity
* NodeSelector
* Resource Limits
* Readiness Probe
* Liveness Probe
* Health Check
* Ingress
* ConfigMap
* Secrets
* Persistent Volume Claim
* Deployment
* Service
* Horizontal Pod Autoscaler
* Ingress Controller
* Persistent Volume
* Storage Class

## Port Forwarding

```shell
kubectl port-forward service/zt-nginx-svc 3080:80

kubectl port-forward service/myapp-stable-service -n myapp-ns 3080:80

kubectl port-forward --namespace=ingress-nginx service/ingress-nginx-controller 8080:80
```

## Logging

```shell
kubectl get pods -n ingress-nginx -l app.kubernetes.io/name=ingress-nginx

kubectl logs ingress-nginx-controller-7d4db76476-lqj2z -n ingress-nginx
```

## Testing

```shell

curl "http://myapp.localdev.me:8080/"

curl -H "X-Canary: v1" "http://myapp.localdev.me:8080/"
```
