### Comandos básicos
---

###### Verificando namespace e pods
``` bash
kubectl get namespaces
```

###### Lista pods de um namespace
```bash
kubectl get pod -n 'kube-system'
```

###### Criando pod padrão
```bash
kubectl run nginx --image nginx
```

###### Deletar pod padrão
```bash
kubectl delete pod nginx
```

###### Gets padrão
```bash
kubectl get all

kubectl get pod,service

kubectl get pod,svc
```