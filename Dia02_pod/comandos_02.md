### Comandos básicos
---

###### Cria o Service (expor o pod)
``` bash
kubectl expose pod 'meu-nginx'
```

###### Criando pod padrão
```bash
kubectl run 'giropops' --image=nginx --port=80
```

###### Mostrar pod em .yaml
```bash
kubectl get pods 'giropops' -o yaml
```

###### Mostrar descrição do pod
```bash
kubectl describe pods 'giropops'
```

###### Criando pod personalizado (arquivo.yaml)
```bash
kubectl apply -f 'pod.yaml'
```


*Obs: `apply` e `create` são parecidos, mas o `create` dá erro se já tiver um pod, enquanto o `apply` atualiza o pod atual se for igual.*

*Obs: O template do pod foi criado manualmente, o deployment é feito com o comando.*
<br>

###### Conectar container dentro de um pod
```bash
kubectl attach 'giropops' -c 'strigus'
```

###### Executar comandos dentro do container do pod
```bash
kubectl exec 'giropops' -c 'strigus' -- ls
```

*obs: o comando em questão foi o "ls"*
<br>

###### Criando um processo e conecção (exec faz o papel do attach também)
```bash
kubectl exec 'giropops' -c 'strigus' -it -- 'sh'
```

*Obs: "-it" é o responsavel pelo comportamento*
*Obs: "sh" é o processo criado*