### Comandos deployment
---

###### Aplicando deployment (arquivo.yaml)
``` bash
kubectl apply -f 'deployment.yaml'
```

###### Get deployment
``` bash
kubectl get deployments -l 'app=nginx-deployment'
```

###### Pods do deployment
``` bash
kubectl get pods -l 'app=nginx-deployment'
```

###### Get ReplicaSet do deployment
``` bash
kubectl get replicasets -l 'app=nginx-deployment'
```

*Obs: `ReplicaSet` é o que faz a replica do pod, deployment gerencia replicasSets.*

*Obs: O template do pod foi criado manualmente, o deployment é feito com o comando.*
<br>

###### Detalhes do deployment
``` bash
kubectl describe deployment 'nginx-deployment'
```

###### Atualizar deployment (depois de mudar o yaml)
``` bash
kubectl apply -f 'deployment.yaml'
```

###### Deletar um deploymente
``` bash
kubectl delete deployment 'deploymente.yaml'
```