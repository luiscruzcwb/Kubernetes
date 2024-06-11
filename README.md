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


### Minikube

- Criado para aprendizado;
- Local Kubernetes Cluster;


### Instalação Kubectl & Minikube

- **kubectl**

- Open download folder

    ```$ cd Download```

- Download kubectl

    ```$ curl -LO https://dl.k8s.io/release/v1.24.2/bin/linux/amd64/kubectl```

- Install kubectl

    ```$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl```

- Check installation

    ```$ kubectl version --client --output=yaml``` 

- **minikube**  (Local Kubernetes cluster)

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

 **Comando**

  -  ```minikube stop```
 
