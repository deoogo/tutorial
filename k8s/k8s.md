### Instalar um addions de redes

* kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 | tr -d '\n')"
 
 
### Criar um Deployment de teste
```bash
* kubectl create deployment nginx --image nginx
* kubectl expose deployment nginx --type NodePort --port 80
```

### Pegar o token de adição de nós 
```bash
* kubeadm  token create print-join-command
 
* kubeadm reset 
```
### Comandos utéis
```bash
* kubectl (pods|services|) --all-namespaces -> Listar pods ou services

* kubectl logs nomeDoPod -n namespace -> Logs do pods


* kubectl exec -ti my_pod-79d7766cb8-2shml -- bash -> logar no conteiner


* kubectl top pods -n namespace -> Mem/Cpu/disco dos Pods

* kubectl top nodes -n namespace -> Mem/Cpu/disco dos nós


* kubectl get pods -n name 

* kubectl describe pod NomedoPod -n namespace


* kubectl get hpa -n namespace

* kubectl edit hpa  NOMEDOHPA -n namespace -->  Alterar as variaveis target / max e min / current e desired


* kubectl get deployments -n namespace

* kubectl edit deployments NOMEDODEPLOYMENTS -n namespace

* kubectl port-forward service/service-cluster port:port
```

### HELM
```bash
* helm repo list --> Lista seu repo local do HELM

* helm install prometheus prometheus-community/prometheus --> Exemplo pratico de uma instalação 

* helm upgrade nome_realese projeto/helm --set key=value --> Alterar um paramentro do manifesto do k8s

* helm show values projeto/helm > values.yaml --> lista os valores do helm chart

* helm upgrade nome_realese projeto/helm -f values.yaml  --> Aplicando as alterações do values.yaml

* helm uninstall  prometheus --> Desistalar 
```