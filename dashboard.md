

### Deploy dashboard

```shell

# 添加 kubernetes-dashboard 仓库
helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
# 使用 kubernetes-dashboard Chart 部署名为 `kubernetes-dashboard` 的 Helm Release
helm upgrade --install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard --create-namespace --namespace kubernetes-dashboard

```

### Access

```shell

kubectl proxy


```

```shell

kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard-kong-proxy 8443:443

```


### Remove

```shell

helm uninstall kubernetes-dashboard --namespace kubernetes-dashboard

```