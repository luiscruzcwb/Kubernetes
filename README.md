# Kubernetes

### História do Kubernetes
   <img src="https://download.logo.wine/logo/Kubernetes/Kubernetes-Logo.wine.png" width="200" height="150">

 - [From Google to the world: The Kubernetes origin story](https://cloud.google.com/blog/products/containers-kubernetes/from-google-to-the-world-the-kubernetes-origin-story)
 - Google Borg Container
 - Kubernetes - 2014
 - Cloud Native Computing Foundation 
 - **Kubernetes - Significado do nome**
    - Alusão a um navio cargueiro;
    - Kubernetes ("Kuvernetes" - em Grego) Timoneiro, aquele que conduz o navio.

- **Logotipo K8s**
    - Logotipo com 7 malaguetas;
    - Project Seven of Nine: Homenagem a personagem da série Star Trek: Voyager;
    - Borg: Organismos ciberneticos de Star Trek;

- **O que é Kubernetes?**
    - Open-Source System;
    - Container Orchestration System;
    - Automação de Processos: Deplyment, Scaling e Gerenciamento; 
    - DevOps (Importante Ferramenta);
    - K8S - Acronimo

- **Caracteristicas Kubernetes**
    - Imutabilidade;
    - Substituição;
    - Segurança contra indisponibilidade;
    - Configuraçõa Declaração;
    - Self-Healing System;
    - Autoscale Up / Down
    - Automação (DevOps Tool);
    - Fault Protection;
    - YAML / JSON Manifest files;
    - Escala Declarativa;
    - Cluster Scale Support;
    - Service-based decoupling for teams;
    - Separation of Responsibilities concept;

- **Infraestrutura Kubernetes**
    - Cloud Abstraction;
    - Bare Metal (Servidores Fisicos);
    - Virtual Machines;
    - Kind [Tool](https://kind.sigs.k8s.io/)
    - Raspberry Pi;
    - AKS,GKE,AZURE; e etc ...; 
    
- **Cluster Kubernetes**

Um cluster Kubernetes consiste em um conjunto de servidores de processamento, chamados nós, que executam aplicações containerizadas. Todo cluster possui ao menos um servidor de processamento (worker node).

O(s) servidor(es) de processamento hospeda(m) os Pods (), que são componentes de uma aplicação. A camada de gerenciamento gerencia os nós de processamento e os Pods no cluster. Em ambientes de produção, a camada de gerenciamento geralmente executa em múltiplos computadores e um cluster geralmente executa múltiplos nós, fornecendo tolerância a falhas e alta disponibilidade.

    - Master
    - Node
        - Pod

![Exemplo K8S Cluster](https://miro.medium.com/v2/resize:fit:700/1*WHXv2Z0bBfC7GW4egoIwTw.png)

![Componentes K8S Cluster](https://kubernetes.io/images/docs/components-of-kubernetes.svg)


### Componentes da camada de gerenciamento

 - kube-apiserver
 - etcd (banco de dados - chave x valor)
 - kube-scheduler
 - kube-controller-manager
 - cloud-controller-manager (Opcional)
 
 ### Componentes do nó

  - kubelet 
  - kube-proxy (Comunicação de rede)
  - Agente de execução de contêiner (runtime)

 ### Documentacao Kubernetes

[Documentacão Oficial](https://kubernetes.io/pt-br/docs/concepts/overview/components/)  
[Kubernetes Deployments - The Ultimate Guide](https://semaphoreci.com/blog/kubernetes-deployment)

### Orquestrador de Containers (Gerenciamento)

- Implantação
- Provisionameto
- Networking
- Dimensionamento
- Disponibilidade

**Orquestradores Populares**

- Kubernetes
- Docker Swarm
- Red Hat OpenShift
- Apache Mesos
- AWS ECS
- GCP GKE

### Minikube

- Criado para aprendizado;
- Local Kubernetes Cluster;


### Instalação Kubectl & Minikube

**kubectl**

- Open download folder

    ```$ cd Download```

- Download kubectl

    ```$ curl -LO https://dl.k8s.io/release/v1.24.2/bin/linux/amd64/kubectl```

- Install kubectl

    ```$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl```

- Check installation

    ```$ kubectl version --client --output=yaml``` 

**minikube (Local Kubernetes cluster)** 

- Open download folder 
    ```$ cd Download```

- Download minikube
    ```$ curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.26.0/minikube-linux-amd64```

- Set permission
    ```$ chmod +x minikube```

- Install minikube
    ```$ sudo install minikube /usr/local/bin/```

- Configure user group
    ```$ sudo usermod -aG docker $USER```

- Reboot Linux
    ```$ sudo reboot```

- Initialization
    ```$ minikube delete```
    ```$ minikube start```

 **Minikube / Cli**

- ```minikube start```
- ```minikube stop```
- ```minikube status```

 **Kubectl / Cli**

- ```kubectl get all```
- ```kubectl get pods -o wide```
- ```kubectl get replicasets```
- ```kubectl apply -f nome-do_arquivo.yaml```
- ```kubect create -f nome-do_arquivo.yaml```
- ```kubectl get pods --all-namespaces```
- ```kubectl delete pods "nome-do-pod"```
- ```kubectl delete pods "nome-do-arquivo.yml"```
- ```kubectl delete --all pods```
- ```watch kubectl get pods```
- ```kubectl rollout status```
- ```kubectl rollout history```
- ```kubectl rollout undo```
- ```kubectl rollout pause```
- ```kubectl rollout resume```
- ```kubectl describe```


## Forma Imperativa

- 

## Deployments
- Faz a implantacao da aplicacao
- Rolling Updates (Rolling Release)
- Recreate Deployment (Risco alto de indisponibilidade)
- Rollback
- **Blue / green deployment**
    ![Exemplo K8S Cluster](https://semaphoreci.com/wp-content/uploads/2019/07/Blue-green-deployment@2x.png)
- **Canary deployment**
    ![Exemplo K8S Cluster](https://semaphoreci.com/wp-content/uploads/2019/07/Canary-deployment@2x.png)






