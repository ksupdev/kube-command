# kubectl command

## get information
- `kubectl get ns`  => get kube namespace
- `kubectl get service -n sync-service`  => get service under namespace
- `kubectl get service`  => get service not specific namespace
- `kubectl -n sync-service describe service sync-units2sf`
- `kubectl get pod`
- `kubectl get pod -n sync-service`
- `kubectl -n sync-service describe pod sync-units2sf-69879fb4fc-b8hq2`

## view logs
- `kubectl logs sync-units2sf-69879fb4fc-b8hq2 -n sync-service` ==> kubectl logs [pod-name] -n [namespace]

## How to access to pod inside
```powershell
## Get pod under the namespace
kubectl get pod -n sync-service

## access to this pod
kubectl -n sync-service  exec --stdin --tty sync-units2sf-69879fb4fc-b8hq2 -- sh
```

## get deployment file
- `kubectl get deployment -n sync-service`
- `kubectl get deployment sync-units2sf -n sync-service`
- `kubectl get deployment sync-units2sf -o yaml -n sync-service`
- `kubectl get deploy fill-deployment-name -o yaml`

## get ingress
- `kubectl get ingress -A`
- `kubectl describe ingress -A`
- `kubectl get ingress -A -o json`

## delete command

- `kubectl delete deployment adc-syn-units2sf -n sync-service`
- `kubectl delete pods <pod>`
- `kubectl delete service sync-units2sf -n sync-service`
- `kubectl delete pods adc-syn-units2sf-857c768d7c-lj4pf -n sync-service`





