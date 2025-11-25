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
***Port-forward the application***
```bash
kubectl port-forward service/myhelmapp -n argocd 8888:80 -n dev
```

***Gallery***

<img width="1500" height="800" alt="image" src="https://github.com/user-attachments/assets/a32f78d9-017a-454a-87c7-e2fe6ab84783" />

<img width="1500" height="800" alt="image" src="https://github.com/user-attachments/assets/6abbc066-a0d3-4a30-8df7-cf7bb738b11c" />

<img width="1500" height="800" alt="image" src="https://github.com/user-attachments/assets/06a01f59-3208-4d78-a047-c3afff77068e" />

***In the following example I have set the app to auto-sync, also I have decreased the number of replicas down to 2, so the Argo catches the change and deletes 3 of the pods:***
<img width="1500" height="800" alt="image" src="https://github.com/user-attachments/assets/24e093f5-c69b-4dc2-be3d-664204852c61" />


***Links***

https://www.youtube.com/watch?v=JLrR9RV9AFA&t=412s

https://github.com/devopsjourney1/argo-examples

https://github.com/Max-Vassilev/argo-examples

