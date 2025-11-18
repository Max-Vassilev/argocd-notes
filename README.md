# argocd-notes

```bash
brew install minikube
```

```bash
minikube start --driver=docker
```

```bash
kubectl create namespace argocd
```

```bash
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

```bash
kubectl get all -n argocd
```

```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```
```bash
kubectl port-forward service/argocd-server -n argocd 8080:443
```


***Gallery***

<img width="1500" height="800" alt="image" src="https://github.com/user-attachments/assets/a32f78d9-017a-454a-87c7-e2fe6ab84783" />

<img width="1500" height="800" alt="image" src="https://github.com/user-attachments/assets/e1a01951-d01f-49ab-9e03-50587d8e0705" />



***Links***

https://www.youtube.com/watch?v=JLrR9RV9AFA&t=412s

https://github.com/devopsjourney1/argo-examples

https://github.com/Max-Vassilev/argo-examples

