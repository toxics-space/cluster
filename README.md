# Kube cluster on k3s

[Quick start](https://docs.k3s.io/quick-start)

## Repo setup
```
git secret reveal
```


## Server
```
ssh root@v1325129.hosted-by-vdsina.ru
```

The value to use for K3S_TOKEN is stored at /var/lib/rancher/k3s/server/node-token on your server node.

```
/etc/rancher/k3s/k3s.yaml
10.11.1.33


curl -sfL https://get.k3s.io | K3S_URL=https://10.11.1.33:6443 K3S_TOKEN=... sh -
```

## Workers
```
10.11.1.33
```

## Confs
```
kconf add <cluster config yaml>
kconf use <..> - switching between different contests(clusters)
```

## Commands
```
kubectl get all -n default - show all from namespace
kubectl get all -n infra   


docker pull nginx
docker tag nginx reg.toxics.space/nginx
docker image push reg.toxics.space/nginx
docker image pull reg.toxics.space/nginx

kubectl rollout restart  deployment/landing-app -n staging


kubectl patch pv <PV_TO_RELEASE> -p '{"spec":{"claimRef": null}}'
```

## Notes

Address of another service:
```
service.namespace.svc.cluster.local
```

Services:
```
reg.ru
vdsina.ru
```

Utils
```
kconf
kubectl
helm

git-secret
GnuPG
```

Top resource usage
```
kubectl top pod -A 
```

