### Comandos deployment: ReplicaSet e DaemonSet
---

###### Visualizar o replicaSet do deployment
``` bash
kubectl get replicasets
```

###### Visualizar o DaemonSet
``` bash
kubectl get daemonset
```

###### Visualizar pods que o DaemonSet gerencia
``` bash
kubectl get pods -l 'app=node-exporter'
```

###### Visualizar detalhes do DaemonSet
``` bash
kubectl describe daemonset 'node-exporter'
```

###### Visualizar se o DaemonSet criou um pod em cada nó existente
``` bash
kubectl get pods -o wide -l 'app=node-exporter'
```

###### Verificar se o DaemonSet está gerenciando os pods
``` bash
kubectl describe daemonset 'node-exporter'
```

###### Removendo DaemonSet
``` bash
kubectl delete daemonset 'node-exporter'
```

---
### Aumentando o número de Nós do Cluster

###### Adicionar nó pelo minikube
``` bash
minikube node add

minikube node add --nodes 3
```
---